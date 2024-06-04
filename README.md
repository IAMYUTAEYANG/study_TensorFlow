# 텐서 플로우 스터디 노트
# study_TensorFlow


#**TensorFlow**란?<br>
- 구글리서치 산하의 딥러닝 팀인 구글브레인 팀[1]이 오픈 소스로 공개한 기계학습 라이브러리.<br>
- 기계학습 분야를 일반인들도 사용하기 쉽도록 다양한 기능들을 제공한다.<br>
- 2016년 알파고와 함께 한국에서도 관심이 높아진 추세이며 관련 컨퍼런스들도 개최되고 있다.<br>
- 고수준 프로그래밍 언어로 알려진 Python을 활용하여 연산처리를 작성할 수 있다.<br>
- 다른 언어들도 대부분 지원하지만 Python 관련 자료가 가장 많다.<br>때문에 공개된 지 그리 오래되지 않았음에도 불구하고 다양한 분야에서 활용되고 있다.<br>

#**특징**
1. 데이터플로 그래프를 통한 풍부한 표현력 <br>
 
2. 아이디어 테스트에서 서비스 단계까지 이용 가능<br>
 
3. 계산 구조와 목표 함수만 정의하면 자동으로 미분 계산을 처리<br>
 
4. Python, C++, Go, Java, R[2]을 지원하며, SWIG를 통해 다양한 언어 지원 가능<br>

#**Keras**란? <br>
- 파이썬으로 작성된 오픈 소스 신경망 라이브러리이다.<br>
- MXNet, Deeplearning4j, 텐서플로, Microsoft Cognitive Toolkit 또는 Theano 위에서 수행할 수 있다.<br>
- 딥 신경망과의 빠른 실험을 가능케 하도록 설계되었으며 최소한의 모듈 방식의 확장 가능성에 초점을 둔다.<br>
- ONEIROS(Open-ended Neuro-Electronic Intelligent Robot Operating System) 프로젝트의 연구적 노력의 일환으로 개발되었으며 주 개발자이자 유지보수자는 구글의 엔지니어 프랑소아 숄레(Francois Chollet)이다.


#**프로그램** 
- 개발환경<br>
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)  <br>
![Vscode](https://img.shields.io/badge/Visual_Studio_Code-0078D4?style=for-the-badge&logo=visual%20studio%20code&logoColor=white) <br>
가상환경: Anaconda
---------------------------------------------------------------------------------------------------------
사용한 프로그램: kerasVer2.py <br>
***
import sys <br>
import cv2 <br>
from PyQt5.QtWidgets import QApplication, QMainWindow, QVBoxLayout, QWidget, QLabel, QPushButton <br>
from PyQt5.QtCore import QTimer, Qt <br>
from PyQt5.QtGui import QImage, QPixmap <br>
from keras.models import load_model <br>
import numpy as np <br>
***
pip install -r requiments.txt
***

##**결과**# <br>
![캡처](https://github.com/IAMYUTAEYANG/study_TensorFlow/assets/165633233/eef2cff8-614a-460a-a2db-6deea1da141b)

