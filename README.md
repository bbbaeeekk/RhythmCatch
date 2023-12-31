
# 리듬 캣치 (자체제작 컨트롤러와 함께 즐기는 언리얼 엔진 기반 VR 리듬게임)

---

## ✨ 리듬캣치 소개 및 시연 영상 ✨

---

![Image Pasted at 2023-5-15 11-50.png](images/Image_Pasted_at_2023-5-15_11-50.png)

## 🧤Overview

---

2개의 프로젝트에서 습득한 기술들을 총 집약하는 프로젝트!

프로젝트를 거치며 습득한 임베디드 제작기술과 유니티엔진을 통해 게임을 제작한 게임제작기술을 접목시키고

새로운 기술인 VR과 언리얼 엔진을 추가한 프로젝트!

🎁자체제작 컨트롤러와 함께 즐기는 언리얼 엔진 기반 VR 리듬게임🎁

## 🧤리듬캣치 플레이 화면

---

### 로비

![로비.PNG](images/%EB%A1%9C%EB%B9%84.PNG)

## HOW TO

![Howto.png](images/Howto.png)

### 해변맵

![해변.PNG](images/%ED%95%B4%EB%B3%80.PNG)
![배구시연.gif](images/%EB%B0%B0%EA%B5%AC%EC%8B%9C%EC%97%B0.gif)

### 숲맵

![숲.PNG](images/%EC%88%B2.PNG)
![모기시연.gif](images/%EB%AA%A8%EA%B8%B0%EC%8B%9C%EC%97%B0.gif)

### 과일맵

![과일.PNG](images/%EA%B3%BC%EC%9D%BC.PNG)
![과일시연.gif](images/%EA%B3%BC%EC%9D%BC%EC%8B%9C%EC%97%B0.gif)

### 야구맵

![야구.PNG](images/%EC%95%BC%EA%B5%AC.PNG)
![야구.gif](images/%EC%95%BC%EA%B5%AC%EC%8B%9C%EC%97%B0.gif)

### 리믹스맵

![리믹스.PNG](images/%EB%A6%AC%EB%AF%B9%EC%8A%A4.PNG)
![리믹스시연.gif](images/%EB%A6%AC%EB%AF%B9%EC%8A%A4%EC%8B%9C%EC%97%B0.gif)

### 스마트 글러브

![Untitled](images/Untitled.png)

### 스마트 글러브 회로도

![Untitled](images/Untitled%201.png)

## 🎠주요기능

---

- 서비스 설명 : 자체제작 컨트롤러와 함께 즐기는 언리얼 엔진 기반 VR 리듬게임
- 주요기능 :
    - 임베디드 :
        - 다양한 센서
            - 구부러짐의 정도에 따라 저항 값이 달라지는 Flex센서 와 얼마나 세게 눌렸는지를 측정하는 압력 센서를 통해 들어오는 아날로그 신호를 ADC칩을 사용하여 디지털 신호로 가공
            - 손의 위치를 파악하기 위해서 imu센서가 사용되었습니다. IMU센서는 x,y,z축의 가속도와 각속도 총 6축의 데이터를 수집할 수 있는 센서로 이 데이터들을 사용하여 손의 위치를 파악
        - 디바이스 드라이버
            - 센서들의 최적화된 제어가 필수, 필수적인 데이터만 가져올 수 있도록 디바이스 드라이버를 직접 개발
        - 소켓통신
            - 다양한 운영체제와 프로그래밍 언어 사이에서 동일한 인터페이스를 사용하고, 높은 속도로 데이터를 교환하기 때문에 사용함
    - 언리얼 :
        - VR게임 제작
            - VR게임모드로 개발 진행 VR게임 사용자경험을 고려하여 VR에서 최적화된 게임 설계, 기획
            - VR기기로 오큘러스 퀘스트2를 선정
        - TCP소켓 플러그인 제작
            - 플러그인은 일종의 라이브러리, 플러그인 C++ 구성이 되어있는데 이를 블루프린트로 전환하여 맵핑
            - 신호정보에 따른 도구들을 맵핑하여 임베디드에서 오는 통신에 따라 다양한 도구 변환
        - 리듬게임 판정
            - 도구 및 속도에 따른 오브젝트 파괴 판정을 하여 다양한 리듬게임 구성

## 💻개발 환경

---

- 임베디드
    - Linux OS ver. armv7l
    - Linux kernel ver. 6.1.21-v7+
- 언리얼
    - 4.27.2 version
- VR
    - Oculus Quest2

## ⚙협업툴

---

- Git
- Plastic SCM
- Jira
- Notion
- Mattermost

## 👓팀원소개

---

- 팀명 : 박자수호단 (BJS)
- 팀장 : 조유빈
- 팀원 : 고현영
- 팀원 : 박상현
- 팀원 : 백현웅
- 팀원 : 유승규
- 팀원 : 용승민

## 🎪팀원역할

---

- 조유빈 (팀장)
    - 플렉스센서 및 압력센서 데이터 읽기 기능 개발
    - H/W 제작
- 고현영
    - 디바이스 드라이버 개발
    - 사용자 영역 코드 개발
    - H/W 제작
    - 배치 배선도 작성
- 박상현
    - 소켓 통신 용 C++ 서버 개발
    - H/W 제작
    - 센서 데이터 기반 오브젝트 매칭 기능 개발
- 백현웅
    - 숲 맵 배경, 오브젝트 배치, 음악 삽입, 리듬 노트 작업
    - 임베디드와 소켓통신 및 신호에 따른 도구 변환
    - 도구 및 속도에 따른 오브젝트 판정 설정
- 유승규
    - 해변맵 배경, 오브젝트 배치, 음악 삽입, 리듬 노트 작업
    - 야구맵 배경, 오브젝트 배치, 음악 삽입, 리듬 노트 작업
    - 리믹스맵 배경, 오브젝트 배치, 음악 믹싱, 리듬 노트 작업
    - waypoint 블루프린트 사용
    - 리듬노트 속도 판정 블루프린트 작성
- 용승민
    - 과일 맵 배경, 오브젝트 배치, 음악 삽입, 리듬 노트 작업
    - 맵 이동 상호작용
    - MRC 카메라 작업
    - 메인로비 구성
    - 튜토리얼 화면 제작
