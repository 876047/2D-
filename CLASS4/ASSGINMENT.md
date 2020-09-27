# Research topics we covered today

## 컬러스페이스

사람의 뇌는 3가지 종류의 원추세포를 통해 시각적 자극을 색으로 인식한다. 
색 공간이란 좌표 공간을 통해 사람에게 인지될 수 있는(혹은 아날로그/디지털 기기에서 나타낼 수 있는) 색을 표현하는 것이다.
최초로 고안된 색 공간은 먼셀 색 공간이며 현재는 개선된 CIE 색공간(CIE XYZ, CIE LAB)등이 표준으로 사용되고 있다.
색 공간이 표현할 수 있는 색의 범위를 나타낸 것을 개머트(gamut)이라고 한다. 
 CIE XYZ 색공간(CIE 1931)은 1931에 프랑스 국제 조명위원회(Commission internationale de l'éclairage)에 의해 제정되었다.
 표준관찰자가 표준 광량을 기준으로 받아들이는 정도를  과학적 방법을 통해 관측하여 계산된 색 공간이다.<sup>1
 
 
 RGB 색공간은 디지털 공간에서 색을 표현할 때 가장 보편적으로 사용되는 색 공간이다.
 빨강(Red), 초록(Green), 파랑(Blue)을 혼합하여 색을 표현한다. 대표적인 RGB 색 공간으로는 sRGB(standard RGB), 애플 RGB, 어도비 RGB 등이 있다. 
 
 
 그 외에도 YUV, ACES 등의 다양한 색 공간이 있다. 
 YUV 색 공간은 비디오에서 주로 사용된다. Y(밝기), U,V(색) 값을 통해 색을 나타낸다.
 이름이 유사한 YCbCr/YPbPr 색 공간은 YUV와 유사한 원리를 이용한다.
 ACES는 Academy of Motion Picture Arts and Sciences의 후원으로 개발된 색 관리 시스템으로 ACES 2065- 1, ACEScc and ACEScct, ACEScg 등의 색 공간을 포함한다.
 보다 넓은 범위의 색이 표현되며 CG 아티스트들에게서 주로 사용된다.
 https://docs.arnoldrenderer.com/display/A5AFHUG/ACES+Workflow 

## 감마 

감마 보정

>감마 보정은 비디오 카메라, 컴퓨터 그래픽 등에서 비선형 전달 함수를 사용하여 빛의 강도 신호를 비선형적으로 변형하는 것을 말한다.<sup>2
(https://ko.wikipedia.org/wiki/%EA%B0%90%EB%A7%88_%EB%B3%B4%EC%A0%95)

베버의 법칙 

>자극을 받고 있는 감각기에서 자극의 크기가 변화된 것을 느끼려면 처음에 약한 자극을 주면 자극의 변화가 적어도 그 변화를 쉽게 감지할 수 있으나 처음에 강한 자극을 주면 자극의 변화를 감지하는 능력이 약해져서 작은 자극에는 느낄 수 없으며 더 큰 자극에서만 변화를 느낄 수 있다는 법칙이다.<sup>3
[네이버 지식백과] 베버의 법칙 [Weber's law] (두산백과)

 시각적 자극의 변화는 빛의 크기의 변화이다. 암부-중간부-명부로 이어지는 그라데이션이 있을 때, 이미 일정 수준의 시각적 자극이 주어진 중간부에서 명부로 이어지는 구간은 암부에서 중간부로 이어지는 구간보다 변화를 감지하기 어렵고 명부에 가깝게 보인다. 이러한 경향 때문에 암부에서의 그라데이션은 자연스럽지 못하다고 느끼기 쉽다. 실제로 색의 차이가 두드러지게 느껴져 화질이 떨어져 보이는 컬러 밴딩 현상은 주로 어두운 부분에서 나타난다. 그렇기 때문에 밝은 부분의 변화 단계를 줄이고 어두운 부분의 변화 단계를 더 풍부하게 해 색을 더 자연스럽게 보이게 하기 위해 감마 보정(gamma correction)을 한다.
 
 일반적으로 컴퓨터 모니터에는 NTSC 표준 감마(감마2.2)가 적용되어 있다. 사진을 촬영할 때 데이터 파일에도 모니터에서 일어나는 감마 보정을 고려하여 원본 이미지보다 더 밝게 감마 보정된 이미지가 저장되므로 촬영하면서 확인한 이미지와 밝기 차이는 나타나지 않게 된다(감마 보정 작업을 통해 어두운 부분의 단계 변화는 더 자연스럽게 남는다).
 툴을 이용하는 합성 작업 시에 감마 보정을 고려하지 않으면 혼란이 일어나기 쉬우므로 감마 보정에 대한 기본적인 이해가 필요하다. 감마 보정 이외에도 디지털 아티스트들은 원하는 이미지를 정확히 표현하기 위해  Offset correction, Gain correction, Contrast correction, Clamp correction 등의 다양한 보정 작업을 한다. 각자의 그래프는 다음과 같다. 

# What is LUT? Color LookUpTable ?


https://youtu.be/lzImtOVx5QI

## LUT의 개념 

 LUT란 Color LookUpTable의 약자이다. 비디오에 적용하여 룩을 변경할 수 있는 고정된 숫자 값의 테이블<sup>4을 의미한다. 간단하고 쉽게 이미지의 느낌을 살리기 위해 자주 쓰이지만, 다양한 보정에서 활용될 수 있다. 후반 작업에서 주로 사용된다.  

## LUT의 종류
 LUT는 1D LUTs(평면 룩업테이블), 3D LUTs(입체 룩업 테이블) 등으로 크게 구분할 수 있다. 아래 이미지는 각각 평면 룩업테이블과 입체 룩업 테이블을 나타낸 것이다. 1D 룩업테이블은 옵셋,게인,감마,채도,콘트라스트등 정보가 전체적으로 저장된 파일<sup>5이다. 단순한 보정 작업에 쓰인다. 3D 룩업테이블은 이미지의 암부, 미들톤, 하일라이트 각각의 옵셋, 게인, 감마, 채도, 콘트라스트등 정보가 저장된 파일<sup>6로 1D 룩업 테이블 보다 섬세한 보정 작업에 쓰인다. 또한 후반작업 공정에서 로그 영상 이미지나 촬영된 영상을 Rec.709와 같은 HD급 영상의 색 공간으로 표준화하거나 톤 매핑하는 데<sup>7에도 사용될 수 있다. 일반적으로 이야기하는 LUT란 3D LUT를 의미한다. 

## LUT의 적용 
 대표적인 LUT의 확장자는 3DL, CUBE 등이 있으며 이외에도 blut, csp, cub, vf 등으로 그 종류가 많다. LUT는 어도비 포토샵, 어도비 프리미어, 어도비 애프터 이펙트, 다빈치 리졸브, 파이널 컷 등 다양한 툴에서 적용 된다. 아래 링크는 무료로 제공되고 있는 LUT 팩을 모은 리스트이다.   

# What is Logspace and what is main difference with sRGB, why and when we use?


## 로그스페이스란?
 로그 촬영이란 사진 풍부한 밝기 변화를 담아내기 위해 사용되는 사진 촬영 방식이다. 많은 데이터를 저장하기 위해 로그 함수(로그 감마)를 사용하여 데이터를 압축한다. 로그 촬영을 위해 지원되는 색 공간으로는 대표적으로 소니의 S-Gamut이 있다. 

## SRGB와의 차이란?
 sRGB는 감마값이 적용된 색 공간이다. sRGB에서 적용되는 감마 곡선과 로그 촬영에 사용되는 색 공간에 적용되는 감마 곡선의 형태에 차이가 있다. 또한 S-Gamut 색공간에서 표현할 수 있는 색 영역은 sRGB보다 넓다.   
 
## 우리가 로그 스페이스를 사용할 때는?
 로그 촬영을 할 때는 일반적으로 후보정을 전제로 한다. 명부와 암부의 디테일이 후보정 작업에 중요할 때, 로그 촬영을 하고 색보정을 하는 것이 도움이 될 수 있다. 


[각주]


1)


2)


3)


4)


5)


6)


7)

[참고자료]

색공간
https://terms.naver.com/entry.nhn?docId=3340383&cid=58161&categoryId=58161

CIE 표준 표색계 
https://terms.naver.com/entry.nhn?docId=282452&cid=42822&categoryId=42822

CIE 1931 색 공간
https://terms.naver.com/entry.nhn?docId=3389796&ref=y&cid=40942&categoryId=32433

https://blog.naver.com/kcw767/221014850359

CIE 1931 색공간-CIE XYZ
https://blog.naver.com/nav153/40112854429

색공간이 뭐지? RGB YUV
https://comdoc.tistory.com/entry/%EC%83%89%EA%B3%B5%EA%B0%84%EC%9D%B4-%EB%AD%90%EC%A7%80-RGB-YUV
YUV
https://ko.wikipedia.org/wiki/YUV

감마 보정
(https://ko.wikipedia.org/wiki/%EA%B0%90%EB%A7%88_%EB%B3%B4%EC%A0%95)

감마가 어디감마
https://chulin28ho.tistory.com/477
https://www.shutterstock.com/ko/blog/129-free-cinematic-luts/

https://pro.sony/ko_KR/technology/professional-video-lut-look-up-table

https://adstorepost.com/164 

https://camerajabber.com/what-is-a-lut-in-video/

https://visionblog.vieworks.com/knowledge/camera-n-sensor/what-is-lut/

https://adstorepost.com/164

우리는 로그(Log)를 알고 있는가? 1편
https://m.blog.naver.com/theriel/221079507331

우리는 로그(Log)를 알고 있는가? 2편
https://m.blog.naver.com/theriel/221077501142
