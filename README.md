### 개요
최근 인터넷 방송과 유튜브의 대중화로 개인 미디어 제작이 활성화되면서, 타인의 초상권 침해 문제가 증가하고 있습니다.

컴퓨터 비전을 활용해 실시간으로 얼굴 탐지 및 모자이크 처리를 해주는 방송 애플리케이션을 개발하고자 하였습니다.

이를 통해 콘텐츠 제작자들이 법적으로 안전한 영상을 제작할 수 있도록 하며 시민들의 개인정보와 초상권을 보호할 수 있습니다.
<hr width="800">

### 활용 데이터 (캐글)
- [Face-Detection-Dataset](https://www.kaggle.com/datasets/fareselmenshawii/face-detection-dataset)
  
<img width="710" alt="image" src="https://github.com/user-attachments/assets/17d454aa-5b8d-4962-93f3-f3ee620cc9e7">

- [Human Faces (Object Detection)](https://www.kaggle.com/datasets/sbaghbidi/human-faces-object-detection)
  
<img width="709" alt="image" src="https://github.com/user-attachments/assets/3cf624be-9c19-48d3-bafc-6574d2fb2270">
<hr width="800">

### 주요 기능
- 메인 화면
<img width="1074" alt="image" src="https://github.com/user-attachments/assets/42eb2e5a-5414-403d-a19c-312b8185d586">

- 방송 화면
<img width="1015" alt="image" src="https://github.com/user-attachments/assets/85b09986-ab9f-42ea-9d63-1b1e76879a27">
<hr width="800"> 

### 사용 방법
```bash
# 안드로이드 스튜디오 or Xcode 사전 설치 필요

# React-Native 설치
npm install -g react-native-cli

# 프로젝트 폴더 생성
git clone https://github.com/hwd0ng/KDT_Project3-PIP.git

# 라이브러리 설치
pip install -r requirements.txt

# front_back 폴더로 이동 후 필요 모듈 설치
cd front_back
npm i
(mac사용자만 해당) cd ios && pod install && cd ..

# server 실행
python main.py

# 앱 실행
(ios) npx react-native run-ios
(android) npx react-native run-android
(자동으로 시작되지 않은 경우) npx react-native start
```
<hr width="800"> 

### 활용 툴/모델
* **백엔드**
    - FastAPI

* **프론트엔드**
    - React Native

* **DB**
    - MongoDB(회원가입정보)

* **얼굴감지모델**
    - [YOLOv8](https://github.com/ultralytics/ultralytics)
      - YOLO 이전 버전들의 개선된 형태로 객체 탐지, 인스턴스 분할, 이미지 분류 등의 컴퓨터 비전 작업을 위한 최신 딥러닝 모델
      - 빠른 추론 속도와 높은 정확도 제공, 특히 작은 객체 탐지에서 성능이 개선됨 (얼굴 탐지에 적합하다고 판단)
        
 <details>
    <summary>모델 학습 및 적용코드</summary>
      <img width="1154" alt="image" src="https://github.com/user-attachments/assets/f1c31ce8-46f5-4968-83f6-29eb77da27f1">
  </details>
<hr width="800">

### 맡은 역할
- 영상 또는 이미지에서 얼굴 객체를 탐지할 수 있도록 모델(Yolov8)을 선정하고 캐글에서 얻은 데이터셋을 해당 모델에 학습시켰습니다.
- 학습시킨 모델을 얼굴 객체가 담긴 무작위 사진, 영상에 적용 및 모자이크 처리 테스트를 성공적으로 진행하였습니다.

    <details>
      <summary>모델 적용 결과</summary>
        <img width="1032" alt="image" src="https://github.com/user-attachments/assets/2bf837f0-ad30-4a0d-bd46-81516c59ff1b">
        <img width="990" alt="image" src="https://github.com/user-attachments/assets/d3d5040a-5624-4ceb-b401-e7294215e7ca">
        (모자이크 적용)
        <img width="987" alt="image" src="https://github.com/user-attachments/assets/6942fa3e-7852-4ee4-9af8-4d39ba8bf5b9">
    </details>
- React-Native 환경 내에서 실시간으로 얼굴 탐지를 할 수 있도록 학습시킨 모델을 변환해서 적용하는 작업을 진행하였습니다.
<hr width="800">

### 프로젝트 후기
- 객체를 학습시키는 과정에서 GPU의 성능 한계로 인해 학습 시간이 약 13시간 정도로 오래 걸렸는데 결과가 안 좋게 나온 점이 아쉬웠습니다.
  
- 초기에 두 개의 객체(얼굴, 차량번호판)를 학습시키고자 했었는데 두 개의 독립적인 데이터셋을 합쳐서 학습시키는 방법은 좋지 않다는 것을 알게 되었습니다.
  
- 두 객체가 함께 있는 데이터셋을 활용한다면 더 좋은 모델로 개선될 수 있을 것이라 생각합니다.
  
- 결과적으로 얼굴 객체에 대해서 잘 탐지를 하고 모자이크 처리까지 잘 되어서 프로젝트가 성공적으로 진행된 것 같아 만족스러웠습니다.
  
- 학습시킨 모델을 React-Native 안에서 작동하도록 하는 과정이 쉽게 풀리지 않아 어려웠습니다.
  
- React-Nativ를 처음 다루어 보아서 어려운 부분도 있었지만 이번 프로젝트를 통해 어플이 개발되는 방식에 대해 알게 되어서 의미있는 시간이었습니다.
<hr width="800">
