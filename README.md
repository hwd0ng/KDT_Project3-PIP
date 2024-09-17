### 개요
최근 인터넷 방송과 유튜브의 대중화로 개인 미디어 제작이 활성화되면서, 타인의 초상권 침해 문제가 증가하고 있습니다.

컴퓨터 비전을 활용해 실시간으로 얼굴 탐지 및 모자이크 처리를 해주는 방송 애플리케이션을 개발하고자 하였습니다.

이를 통해 콘텐츠 제작자들이 법적으로 안전한 영상을 제작할 수 있도록 하며 시민들의 개인정보와 초상권을 보호하는 것을 목표로 하였습니다.
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
# 프로젝트 폴더 생성
git clone https://github.com/hwd0ng/KDT_Project2-EPL_Chatbot.git

# 라이브러리 설치
pip install -r requirements.txt

# 챗봇모델링코드.ipynb 차례로 실행 

# 프로젝트 폴더 루트에 fine_tuned_kogpt2 폴더 생성 확인

# 서버 실행(터미널)
pyhton main.py
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
    - <details>
      <summary>모델 학습 및 적용코드</summary>
          <img width="1154" alt="image" src="https://github.com/user-attachments/assets/f1c31ce8-46f5-4968-83f6-29eb77da27f1">
      </details>
<hr width="800">

### 맡은 역할

<hr width="800">

### 프로젝트 후기

<hr width="800">
