# Hallym University Capstone Design - MadeByKitten 
캡스톤디자인 - 고양이가만듦  
<br />
## Subject
OpenCV와 Unity를 이용한 레이저 스크린사격   
<br />
## Summary

-  계획 : 총에서 레이저를 발사하여, OpenCV를 통해 좌표 값을 Unity 게임 내로 반환하여 해당 좌표가 일치할 시,
  과녁을 쓰러트려 
점수를 획득하는 방식

- 필요성 : 실내에서 즐길 수 있는 콘텐츠를 만들어 보고자 함  
<br />

## Tech Stack &nbsp;
<img src="https://img.shields.io/badge/Unity-000000?style=flat-square&logo=Unity&logoColor=white"/></a>
<img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=OpenCV&logoColor=white"/></a>
<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=Python&logoColor=white"/></a>
<img src="https://img.shields.io/badge/CSharp-239120?style=flat-square&logo=CSharp&logoColor=white"/></a>
<img src="https://img.shields.io/badge/Arduino-00979D?style=flat-square&logo=Arduino&logoColor=white"/></a>  
<br />

## Contents

1. [소개 : 프로젝트에 대한 간략한 소개 및 목적](#Introduction)

2. [팀 : 팀원소개 및 역할](#Team)

3. [설계 : 아키텍쳐](#Architecture)
 
4. [과정 : 프로젝트 제작 과정](#Process)

5. [결과 : 프로젝트 결과](#Result) 

----  
<br />

## Introduction

코로나로 인하여 외출을 자주 못하는 지금 실내 같은 좁은 공간에서 즐길 수 있는 콘텐츠를 만들어 보고자 이 콘텐츠를 고안했다.
빔프로젝터에 유니티로 만든 게임 화면이 나오면 총으로 타겟을 사격하고, 카메라가 레이저를 감지하면 해당 좌표를 게임으로 전송하는 방식이다.  
<br />

## Team

MadeByKitten

|Name|Department|Part|
|---|---|---|
| Lim Ji Hwan | Hallym Univ |Unity| 
| Jung Ku Hyeon | Hallym univ |Arduino , Unity| 
| Hong Seung Taek | Hallym univ |Unity|
| Lee Woo Yeol | Hallym univ |OpenCV| 

Professor
|Name|Department|Part|
|---|---|---|
| Lee Ju Sung | Hallym Univ(Prof.) | Advise  
<br />

## Architecture

<img src="https://user-images.githubusercontent.com/65859512/144265474-b7304c3e-87ba-4f22-abcc-bb5856d9a634.jpg"
 width="500" height="300"/>  
<br />

## Process  
<br />

### Arduino
- 아두이노 보드(나노)와 레이저 모듈, 스위치를 점퍼케이블로 연결하고, 스위치는 방아쇠가 당겨지는 위치에 있게 한다. 총기의 방아쇠를 당기면 스위치가 켜지면서 레이저가 발사되는 방식으로 제작한다. //이미지 삽입  
<br />

### OpenCV
- 먼저 총기에서 발사되는 레이저를 OpenCV를 통해 레이저의 붉은색을 감지한고,  레이저 포인터의 좌표값을 얻어 Unity에 해당 좌표 값을 반환 및 좌표에 Ray를 쏘는 형식으로 만든다.
##### 레이저 좌표
<img src="https://user-images.githubusercontent.com/65859512/144274413-7cc5fb4e-0346-4356-b61a-84b0d60a712f.PNG"
 width="500" height="300"/>  
 <br />

### Unity
- Unity에서는 게임의 전반적인 씬과 UI를 제작한다. 게임씬은 총 2개로 구성하여 고정되어 있는 과녁을 맞추는 표적사격 씬과, 움직이는 과녁을 맞추는 클레이 씬을 만든다. 기본적으로 시간 제한과 총알의 수를 제한하고, 과녁의 거리에 따라 점수를 달리 매기는 방식으로 구성하며 게임의 재미를 높이기 위해 난이도를 조절하여 게임을 만든다.
게임의 UI적인 요소로는 게임의 시작과 종료, 메뉴에서 원하는 게임을 선택, 게임의 난이도, 게임을 시작하기에 앞서 간단한 설명 등이 들어있다.
##### 표적사격
<img src="https://user-images.githubusercontent.com/65859512/144270094-89a3f37d-7657-4e89-ae2c-fc43464a6304.PNG"
 width="500" height="300"/>
##### 클레이사격
<img src="https://user-images.githubusercontent.com/65859512/144270529-83753c07-3a36-4d8f-9e1f-d678f2b4f4f9.PNG"
 width="500" height="300"/>  
 <br />

## Result
