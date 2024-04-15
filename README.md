# study_TensorFlow
# 텐서 플로우 끄적임 노트

#**TensorFlow**란?
구글리서치 산하의 딥러닝 팀인 구글브레인 팀[1]이 오픈 소스로 공개한 기계학습 라이브러리. 기계학습 분야를 일반인들도 사용하기 쉽도록 다양한 기능들을 제공한다. 2016년 알파고와 함께 한국에서도 관심이 높아진 추세이며 관련 컨퍼런스들도 개최되고 있다.
고수준 프로그래밍 언어로 알려진 Python을 활용하여 연산처리를 작성할 수 있다. 다른 언어들도 대부분 지원하지만 Python 관련 자료가 가장 많다. 때문에 공개된 지 그리 오래되지 않았음에도 불구하고 다양한 분야에서 활용되고 있다.

#**특징**
1. 데이터플로 그래프를 통한 풍부한 표현력
2. 아이디어 테스트에서 서비스 단계까지 이용 가능
3. 계산 구조와 목표 함수만 정의하면 자동으로 미분 계산을 처리
4. Python, C++, Go, Java, R[2]을 지원하며, SWIG를 통해 다양한 언어 지원 가능



------------------------------------------------------------------------------------------
from keras.models import load_model  # TensorFlow is required for Keras to work
from PIL import Image, ImageOps  # Install pillow instead of PIL
import numpy as np
import tensorflow as tf

print("TensorFlow 버전:", tf.__version__)

# Disable scientific notation for clarity
np.set_printoptions(suppress=True)

# Load the model
model = load_model("keras_Model.h5", compile=False)

# Load the labels
class_names = open("labels.txt", "r", encoding="utf-8").readlines()

# Create the array of the right shape to feed into the keras model
# The 'length' or number of images you can put into the array is
# determined by the first position in the shape tuple, in this case 1
data = np.ndarray(shape=(1, 224, 224, 3), dtype=np.float32)

# Replace this with the path to your image
image = Image.open("C:\dataset\TESTSET\DOG11.jpg").convert("RGB")

# resizing the image to be at least 224x224 and then cropping from the center
size = (224, 224)
image = ImageOps.fit(image, size, Image.Resampling.LANCZOS)

# turn the image into a numpy array
image_array = np.asarray(image)

# Normalize the image
normalized_image_array = (image_array.astype(np.float32) / 127.5) - 1

# Load the image into the array
data[0] = normalized_image_array

# Predicts the model
prediction = model.predict(data)
index = np.argmax(prediction)
class_name = class_names[index]
confidence_score = prediction[0][index]

# Print prediction and confidence score
print("Class:", class_name[2:], end="")
print("Confidence Score:", confidence_score)

![캡처](https://github.com/IAMYUTAEYANG/study_TensorFlow/assets/165633233/eef2cff8-614a-460a-a2db-6deea1da141b)

