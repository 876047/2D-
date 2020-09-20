# 알파란 무엇인가(What is Alpha)?


 알파 채널이란 이미지의 투명도에 대한 정보가 지정되는 채널을 말한다. 알파 채널을 활용하여 이미지에서 사용하고 싶은 부분만 추출하는 작업(마스킹 작업)을 할 수 있다. 알파 채널에서는 투명도를 지정하기 위해 명도를 활용한다. 흰색에 가까울 수록 불투명해지고 검은색에 가까울 수록 투명해진다. 합성 작업에서 주로 사용된다. 스트레이트 알파(언 프리-멀티플라이드 알파)와 프리-멀티플라이드 알파로 구분할 수 있다. 스트레이트 알파는 알파 채널의 값이 다른 채널에 적용되지 않은 상태를 뜻하며 프리 멀티 플라이드 알파는 합성을 하기 전 알파 채널의 값이 다른 채널에 적용된 상태를 말한다. 마스킹을 적용하기 전과 후를 구분하는 이유는 합성 프로그램에서 사용할 때 이중으로 마스킹을 할 위험이 있기 떄문이다. 
 
![알파마스크](https://user-images.githubusercontent.com/71231278/93719775-af80ca80-fbbf-11ea-9276-9bea84898b2a.png)

[그림 1] 스트레이트 알파와 프리멀티플라이드 알파(이미지 출처: https://limnu.com/premultiplied-alpha-primer-artists/)


# 색이란 무엇인가?(What is color)?

색은 시각적 자극이다. 우리 눈은 각각 , 긴 파장(빨간 빛), 중간 파장(녹색 빛), 짧은 파장(푸른 빛)에 민감하게 반응하는 세 종류의 원추세포를 통해 빛을 색으로 인지하게 된다. 개인적인 경험에 따라 색을 해석하는 방식은 다를 수 있다. '색상, 명도, 채도'는 색을 구분하는 데 있어서 중요한 세 가지 특성이다.     

**색상**

색의 세 가지 특성 중 하나이다. 색상환 중 어디에 위치하는가로 나타낼 수 있다. 

![색상환](https://user-images.githubusercontent.com/71231278/93719021-dc7eae80-fbba-11ea-9c36-eaaf99795c5a.png)

[그림2] 색상환(이미지 출처: https://commons.wikimedia.org/wiki/File:MunsellColorWheel.svg)

**명도**

색의 세 가지 특성 중 하나이다. 명도의 단계로 색이 얼마나 밝고 어두운지 나타낼 수 있다. 흰 색에 가까울수록 명도가 높고 검은색에 가까울수록 명도가 낮다. 

![명도](https://user-images.githubusercontent.com/71231278/93719228-0ab0be00-fbbc-11ea-9115-3cdc526e4c8e.jpg)

[그림3] 명도

**채도** 

색의 세 가지 특성 중 하나이다. 색상이 얼마나 선명한지 나타낼 수 있다. 채도가 낮은 색일수록 회색에 가깝고, 채도가 높은 색일수록 형광에 가깝다.   

![채도](https://user-images.githubusercontent.com/71231278/93719274-5feccf80-fbbc-11ea-993a-5c8b053ce01f.png)

[그림4] 채도(이미지 출처: https://en.wikipedia.org/wiki/File:Red_saturations.svg)

## 색 조합 원리 

* 가산 혼합

![가산 혼합](https://user-images.githubusercontent.com/71231278/93720064-a7c22580-fbc1-11ea-9362-719c4a4d9da7.png)

[그림5] 가산 혼합(이미지 출처: https://99designs.com/blog/tips/correct-file-formats-rgb-and-cmyk/)

가산 혼합은 광원을 사용하여 색을 조합할 때 나타난다. 빨강, 초록, 파랑의 광원의 조합을 통해 다양한 색상을 만들어낼 수 있다. 가산 혼합 방식을 사용하는 대표적안 색 모델로는 RGB 색 모델이 있다.  


* 감산 혼합

![감산 혼합](https://user-images.githubusercontent.com/71231278/93720062-a42e9e80-fbc1-11ea-877b-8ca2ad45bfb5.png)

[그림6] 감산 혼합 (이미지 출처: https://99designs.com/blog/tips/correct-file-formats-rgb-and-cmyk/)



감산 혼합은 잉크나 물감 등을 통해 색을 조합할 때 나타난다. 시안, 마젠타, 노랑을 이용하여 다양한 색상을 만들어낸다. 감산 혼합 방식을 사용하는 대표적인 색 모델로는 CMYK 색 모델이 있다. 



## 디지털 색상

* RGB 

인쇄해야 하는 결과물을 작업할 때는 CMYK가 주로 사용되는 반면 디지털 화면에서 전시되는 결과물을 작업할 때에는 RGB 색 모델이 주로 사용된다. RGB 모델은 우리 눈이 빛을 인식하는 것과 비슷한 원리로 작동하여 폭 넓게 사용되지만, 원하는 색을 직관적으로 찾기 어렵다는 단점이 있다. RGB 색 모델에서는 0~255까지의 값을 가지는 각각의 R, G, B 채널을 조합해서 색상을 만든다.  

![RGB](https://user-images.githubusercontent.com/71231278/93721038-4f425680-fbc8-11ea-89d4-b1b85f74e99b.png)

[그림6] RGB 색 모델 (이미지 출처: https://en.wikipedia.org/wiki/File:RGB_color_solid_cube.png)

* HSL

 RGB 색 모델보다 직관적으로 색을 고를 수 있도록 만들어진 색 모델. 색의 특성인 Hue(색상), Saturation(채도), Luminance(밝기)를 활용하여 색을 나타낸다. 유사한 색 모델로는 HSV 등이 있다. 
 
![HSL색모델](https://user-images.githubusercontent.com/71231278/93721400-ef00e400-fbca-11ea-8937-8e5d6d241dd3.png)

[그림7] 클립 스튜디오에서의 HSL 색 모델 컬러써클

## 참고자료

David Hart, 2016, WHAT IS PREMULTIPLIED ALPHA? A PRIMER FOR ARTISTS., Retrieved from https://limnu.com/premultiplied-alpha-primer-artists/
Khan Academy Labs, 2016, What is the "Color" we saying?, Retrieved from https://www.youtube.com/watch?v=0DXZvcfPVrk&list=PLP8UjARyH0gV5JUFrCeWQTpvt959NhfNH&index=65
Khan Academy Labs, 2019, RGB color Model, Retrieved from https://youtu.be/T0jzClmP2pc
Khan Academy Labs, 2019, HSL color Model, Retrieved from https://youtu.be/Ceur-ARJ4Wc
