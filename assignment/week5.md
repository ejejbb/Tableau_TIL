# Fifth Study Week

- 39강: [LOD](#39강-lod)

- 40강: [EXCLUDE](#40-lod-exclude)

- 41강: [INCLUDE](#41-lod-include)

- 42강 : [매개변수](#42-매개변수)

- 43강 : [매개변수 실습](#43-매개변수-실습) 
![링크](https://youtu.be/GJvB8hBqeE8?si=3jIj1iymZHZ7mBam)

- 44강: [매개변수 실습](#44-매개변수-실습)

- 45강: [마크카드](#45-워크시트-마크카드)

- 46강: [서식계층](#46-서식-계층)

- 47강: [워크시트](#47-워크시트-서식)

- [문제1](#문제-1)

- [문제2](#문제-2)

## Study Schedule

| 강의 범위     | 강의 이수 여부 | 링크                                                                                                        |
|--------------|---------|-----------------------------------------------------------------------------------------------------------|
| 1~9강        |  ✅      | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=84)       |
| 10~19강      | ✅      | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=75)       |
| 20~29강      | ✅      | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=65)       |
| 30~38강      | ✅      | [링크](https://www.youtube.com/watch?v=e6J0Ljd6h44&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=55)       |
| 39~47강      | ✅      | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=45)       |
| 48~59강      | 🍽️      | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=35)       |
| 60~69강      | 🍽️      | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=25)       |
| 70~79강      | 🍽️      | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=15)       |
| 80~89강      | 🍽️      | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=5)        |


<!-- 여기까진 그대로 둬 주세요-->

> **🧞‍♀️ 오늘의 스터디는 지니와 함께합니다.**

## 39강. LOD

<!-- INCLUDE, EXCLUDE, FIXED 등 본 강의에서 알게 된 LOD 표현식에 대해 알게 된 점을 적어주세요. -->
- LOD(Level of Detail): 현재 뷰에는 영향을 받지 않고 원하는 세부 수준에서 계산 가능
- 표현식: INCLUDE, EXCLUDE, `FIXED`

### 1. FIXED에서 설정한 차원이 뷰에 포함되어 있을 때-1
- '지역별 매출' 계산된 필드 만들기   
  <img width="375" alt="1" src="https://github.com/user-attachments/assets/12266b7e-ea65-4ca8-b9be-b9129822d3d2">

- 현재 뷰에서 보여주는 세부 수준인 '국가/지역' 기준이 아니라 '지역' 수준에 따라 합계된 매출이 나타나게 됨.   
  <img width="429" alt="2" src="https://github.com/user-attachments/assets/99593df5-54ca-4941-b78e-5c64a9e31a35">


### 2. FIXED에서 설정한 차원이 뷰에 포함되어 있지 않을 때
- '범주별 매출' 계산된 필드 만들기   
  <img width="374" alt="3" src="https://github.com/user-attachments/assets/1801a0d1-2723-49e1-bc17-17d9bde80438">

- 현재 뷰에서는 '지역별 매출'을 보여주지만, 추가된 열에서 뷰에 나타나 있지 않은 '범주별 매출'을 보여준다.   
  <img width="343" alt="4" src="https://github.com/user-attachments/assets/d64e25d4-7e5c-4b7d-ab29-d7fb6bef4d85">


### 3. FIXED에서 설정한 차원이 뷰에 포함되어 있을 때-2
- '전체 매출'과 '제품 구성 비율' 계산된 필드 만들기   
  <img width="371" alt="5" src="https://github.com/user-attachments/assets/ec38ed05-5398-4bae-b56a-69fe87f526df">
  <img width="373" alt="6" src="https://github.com/user-attachments/assets/fbb86ceb-bf11-4eaf-aadb-c0d960d09f83">

- 필터로 하위범주의 가전제품을 제외해도, 계산된 필드로 생성된 열은 변함이 없다.   
  <img width="790" alt="7" src="https://github.com/user-attachments/assets/c4ad81de-cb02-475b-b15a-549e8e400cba">



## 40. LOD EXCLUDE

<!-- INCLUDE, EXCLUDE, FIXED 등 본 강의에서 알게 된 LOD 표현식에 대해 알게 된 점을 적고, 아래 두 질문에 답해보세요 :) -->
- LOD 표현식: INCLUDE, `EXCLUDE`, FIXED   
-> 현재 뷰에서 특정 차원을 제외하여 계산할 때 사용

- 계산된 필드 만들기
: '액세서리 매출', 'exclude 하위 범주 매출', '각 제품별 매출과 액세서리 매출의 차이'   
<img width="370" alt="10" src="https://github.com/user-attachments/assets/15c535fc-b3d0-495d-906b-47cd924444ea">
->
<img width="796" alt="11" src="https://github.com/user-attachments/assets/f593ef18-a8ee-4c8e-b530-d45c88cf7e18">   


<img width="366" alt="12" src="https://github.com/user-attachments/assets/843b9993-2d54-4b55-95de-6a0251d05ba7">
<img width="366" alt="13" src="https://github.com/user-attachments/assets/394c1bd1-0408-4b0a-bd3e-c73b00513ed7">   
->
<img width="674" alt="14" src="https://github.com/user-attachments/assets/a0a9b0e4-02ed-4a4f-959b-68c9b1865021">   

=> 모든 제품의 매출이 액세서리 매출을 기준으로 얼마나 차이가 나는지에 대해(액세서리 매출 기준 더 많은지 적은지) 확인 가능 
```
exclude 하위 범주 매출: 하위 범주 차원을 무시하고 액세서리의 매출 값만 반환
```
    

> **🧞‍♀️ FIXED와 EXCLUDE을 사용하는 경우의 차이가 무엇인가요?**

```
FIXED는 ①현재 뷰에는 영향을 받지 않고 ②원하는 세부 수준에서 계산하고자 할 때 사용한다.

EXCLUDE는 ①현재 뷰에서 ②특정 차원을 제외하여 계산하고자 할 때 사용한다.
```

> **🧞‍♀️ 왜 ATTR 함수를 사용하나요?**

```
 ①데이터의 일관성을 유지하고
 ②계산식 오류를 방지하기 위함이다.

-> 하위 범주 매출 필드가 여러 값을 가질 수 있기 때문에, ATTR 함수를 사용하여 일관된 단일 값을 반환할 수 있다.
-> SUM과 같은 집계 함수는 단일 값과 연산해야 하므로 ATTR을 사용한다.
```


## 41. LOD INCLUDE

<!-- INCLUDE, EXCLUDE, FIXED 등 본 강의에서 알게 된 LOD 표현식에 대해 알게 된 점을 적고, 아래 두 질문에 답해보세요 :) -->

- LOD 표현식: `INCLUDE`, EXCLUDE, FIXED   
-> 현재 뷰에서 특정 차원을 추가하여 계산할 때 사용   
-> `EXCLUDE`와 마찬가지로 차원 필터를 통해 해당 값을 변경할 수 있다.

 - `각 도시의 고객당 평균 매출`을 확인하기 위해   
'국가/지역', '시/도', '주문id' 필드를 행 선반에 놓고 매출 필드를 더블클릭하는 것으로 가능하지만   
해당 값들은 따로 필드를 생성한 것이 아니기 때문에 이 값을 재사용하기 위해서는 `INCLUDE` LOD 표현식을 사용한다.   

<img width="365" alt="15" src="https://github.com/user-attachments/assets/9024634e-546f-47c2-9dd2-dadbdbf28d13">   

-> 해당 함수는 주문id 차원을 포함해서 합계한 매출에 평균을 반환한다는 의미이다.

### 계산된 필드를 사용한 것과 사용하지 않은 것 비교
[계산된 필드 사용x]   
<img width="540" alt="16" src="https://github.com/user-attachments/assets/4eadf6ba-27a4-4b87-9b8d-6a3d97dd0e8c">   

vs.   

[계산된 필드 사용o]   
<img width="438" alt="17" src="https://github.com/user-attachments/assets/1754981d-87db-4973-beda-771cd8c85cc8">   

-> 설명: 주문id 차원을 현재 뷰에서 표시하지 않지만 include lod 표현식을 통해 해당 차원을 계산에 추가할 수 있다.

```
# INCLUDE 대신 FIXED 사용하여 동일한 결과 나타내기

INCLUDE 사용: AVG({INCLUDE [주문 Id]:SUM([매출])})
FIXED 사용: AVG({FIXED [주문 Id]:SUM([매출])})
```

> **🧞‍♀️ 그렇다면 어떤 경우에 각 표현식을 사용하나요? 예시와 함께 적어보아요**


```
# LOD 표현식 차이

- 뷰에 표시되는 값이 차원이면, FIXED LOD 표현식만 사용 가능.
: FIXED 표현식은 측정값과 차원을 반환할 수 있지만, INCLUDE와 EXCLUDE 표현식은 측정값만 반환할 수 있기 때문.

- 반환 값이 차원 필터의 영향을 받게 되는 경우에는 INCLUDE 또는 EXCLUDE 표현식만 사용 가능.
: FIXED는 차원 필터의 영향을 받지 않기 때문.
```

## 42. 매개변수

<!-- 매개변수에 대해 알게 된 점을 적어주세요 -->
- 매개변수   
: 고정된 상수값이 아닌 동적인 값으로 변경하기 위해 활용하는 기능   
: 계산식, `필터`, 참조선을 함께 사용해야 작동됨.   
-> 필터의 필드 기준에서 매개변수를 선택해야 함.

- 매개변수 실습 예시   
: 하위범주별 매출을 보고자 할 때, 상위10개에서 상위5개로 변경하고자 한다면 필터를 직접 편집할 수 있지만 단계가 복잡하다. 이러한 경우에 `매개변수`를 만들어 사용하면 쉽게 해결 가능!

```
# 매개변수를 만드는 몇 가지 방법

1. 필터를 통해 만들기
2. 원하는 필드 위에 마우스 우클릭 > 만들기 > 매개변수 만들기
3. 데이터 패널을 통해 만들기
```

실습: <img width="420" alt="18" src="https://github.com/user-attachments/assets/9b0f5328-2d49-466b-b35c-d5bb801d1c55">



> **🧞‍♀️ 집합에도 매개변수를 적용할 수 있나요? 시도해봅시다**
<img width="341" alt="19" src="https://github.com/user-attachments/assets/91bbc87f-0914-48be-9501-3213cbf97438">
<img width="799" alt="20" src="https://github.com/user-attachments/assets/ab55b42c-7392-476f-8aac-6b49dd430989">



## 43. 매개변수 실습
<!-- 영상 묶음에 포함되지 않아 찾기 어려우실까 링크를 아래에 첨부하겠습니다. 수강 후 삭제해주세요-->

https://www.youtube.com/watch?v=GJvB8hBqeE8

매개변수는 `계산식`, 필터, 참조선을 함께 사용해야 작동됨.

### 실습1. 차원 선택하기
'~별 매출'을 보고자 할 때, 행 선반에 원하는 필드를 끌어다 놓을 수도 있지만 매개변수를 활용하면 조금 더 쉽게 변경 가능하다.

[실습]   
매개변수 만들기:   
<img width="422" alt="21" src="https://github.com/user-attachments/assets/4a9c1771-bae3-48fe-a8c0-b9fbb1d2279f">   
매개변수 작동을 위한 계산된 필드 만들기:   
<img width="361" alt="22" src="https://github.com/user-attachments/assets/a848a881-685e-4bcf-ba5f-6c67b6e9e6bb">   
어떤 차원을 선택했는지 한 눈에 확인하기 위해 제목 변경하기:   
<img width="328" alt="23" src="https://github.com/user-attachments/assets/3f65e386-b158-4f2d-a405-2703dc5d4a6b">   
실습결과:   
<img width="799" alt="24" src="https://github.com/user-attachments/assets/24777120-a07b-47b9-b41a-6f09a668ef85">



### 실습2. 측정값 선택하기
'항목별 ~'을 보고자 할 때, 열 선반에 원하는 필드를 끌어다 놓을 수도 있지만 매개변수를 활용하면 조금 더 쉽게 변경 가능하다.

[실습]   
매개변수 만들기:   
<img width="421" alt="25" src="https://github.com/user-attachments/assets/02886dbc-f140-4855-a616-f9aca384f1bd">   
매개변수 작동을 위한 계산된 필드 만들기:   
<img width="364" alt="26" src="https://github.com/user-attachments/assets/f105a13b-f686-450d-a5c5-6fc4c7162822">   
어떤 차원을 선택했는지 한 눈에 확인하기 위해 제목 변경하기:   
<img width="329" alt="27" src="https://github.com/user-attachments/assets/d14a9c59-e323-4de3-84ef-9244c279a99e">   
실습결과:   
<img width="796" alt="28" src="https://github.com/user-attachments/assets/a4f65089-f9dd-4b63-9a08-393a6985b827">   


[추가 실습]: 측정값 단위 나타내기
매개변수 만들기:    
<img width="365" alt="29" src="https://github.com/user-attachments/assets/fbf20914-60da-425d-8b6b-99cdb303edc5">   
실습결과:   
<img width="796" alt="30" src="https://github.com/user-attachments/assets/45fd7d19-e96a-4dac-ad1b-defdb0ddb49d">




## 44. 매개변수 실습

<!-- 매개변수에 대해 알게 된 점을 적어주세요 -->

매개변수는 계산식, 필터, `참조선`을 함께 사용해야 작동됨.

[실습1]: `목표 매출`을 달성한 나라와 그렇지 않은 나라를 구분하기   
참조선 만들기(`분석` 탭에서 `참조선`을 뷰로 드래그):   
<img width="284" alt="31" src="https://github.com/user-attachments/assets/03aa7bd5-ded2-4d79-b95f-ba11c4e0d560">   
색상 구분하기:   
<img width="363" alt="32" src="https://github.com/user-attachments/assets/4ba68000-bece-471d-b81a-864f14b2ff37">   
실습 결과:   
<img width="796" alt="33" src="https://github.com/user-attachments/assets/c30ee01b-546d-48d2-86c0-2a692d3b6c74">   


[실습2]: `날짜 범위`의 매출합계 구하기   
'시작 날짜', '마지막 날짜' 매개변수 만들기:   
<img width="421" alt="34" src="https://github.com/user-attachments/assets/48259b5e-c1c4-4240-b3d9-7cb3cf6d81bb">   
참조선 만들기:   
<img width="287" alt="35" src="https://github.com/user-attachments/assets/a9670e33-b76e-4d1a-9322-64b1544da869">   
제목 변경하기:    
<img width="364" alt="36" src="https://github.com/user-attachments/assets/0c83d924-c28f-4e08-b3ba-61851cfbf93e">
<img width="331" alt="37" src="https://github.com/user-attachments/assets/478f34a6-733a-42c5-9788-d97152728e89">   
실습 결과:   
<img width="798" alt="38" src="https://github.com/user-attachments/assets/482bd7df-b169-4557-8e2e-6624d4fcde29">


## 45. 워크시트 마크카드

<!-- 마크카드에 대해 알게 된 점을 적어주세요 -->
`마크카드`: 마크의 서식을 변경할 때 활용
```
# 색상
'후광 옵션'은 '맵'에서만 적용됨.

연속형 필드는 '색상 범위 범례'가 표시되고
불연속형 필드는 '항목별 범례'가 나타남.

# 레이블
레이블이 다른 레이블과 겹치는 경우에 자동으로 레이블을 숨김.
-> '레이블이 다른 마크와 겹치도록 허용' 옵션을 선택해야 함.

# 세부정보
불연속형 필드를 사용하면 해당 차트에서 데이터를 구분해 표시하고
연속형 필드를 사용하면 도구 설명에 데이터가 추가됨.

# 차트 유형에 따라 경로, 모양 등 마크 카드가 다양하게 나타나기도 함.
```


## 46. 서식 계층

<!-- 서식계층에 대해 알게 된 점을 적어주세요 -->

> **🧞‍♀️ 서식계층을 일반적인 것에서 구체적인 것 순서로 기입해보세요**
![캡처](https://github.com/user-attachments/assets/aef34ea0-7379-4e68-8244-770168f9a0ed)



## 47. 워크시트 서식

<!-- 워크시트 서식에 대해 알게 된 점을 적어주세요!-->



## 문제 리스트



## 문제 1.

```
가장 많이 주문한 사람들은 물건 배송을 빨리 받았을까요?
조건을 준수하여 아래 이미지를 만들어봆시다.
1) 국가/지역별(이하 '나라'로 통칭), 범주별로 배송일자가 다를 수 있으니 먼저, 나라별/범주별로 평균 배송일자를 설정한 뒤,
2) 각 나라에서 가장 많이 주문한 사람의 이름을 첫 번째 열,
3) 그 사람이 주문한 제품 이름을 2번째 열,
4) 각 상품이 배송까지 걸린 날 수를 표현하고
5) 그리고 만약 배송이 각 나라/범주별 평균보다 빨랐다면 '빠름', 같다면 '평균', 느리다면 '느림' 으로 print 해주세요. 
```

![이미지주소](https://github.com/yousrchive/BUSINESS-INTELLIGENCE-TABLEAU/blob/main/study/img/2nd%20study/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202024-08-13%20%E1%84%8B%E1%85%A9%E1%84%8C%E1%85%A5%E1%86%AB%2010.12.36.png?raw=true)

<!-- 여기까지 오는 과정 중 알게 된 점을 기입하고, 결과는 시트 명을 본인 이름으로 바꾸어 표시해주세요.-->

## 문제 2.

```
채원이는 태블로를 쓰실 수 없는 상사분께 보고하기 위한 대시보드를 만들고 싶어요. 

제품 중분류별로 구분하되 매개변수로써 수익, 매출, 수량을 입력하면 저절로 각각 지표에 해당하는 그래프로 바뀌도록 설계하고자 해요.

 어떤 값이 각 지표의 평균보다 낮은 값을 갖고 있다면 색깔을 주황색으로, 그것보다 높다면 파란색으로 표시하고 싶어요. 그 평균값은 각 지표별로 달라야 해요.
```

![example](https://github.com/yousrchive/BUSINESS-INTELLIGENCE-TABLEAU/blob/main/study/img/2nd%20study/%E1%84%83%E1%85%A1%E1%84%8B%E1%85%AE%E1%86%AB%E1%84%85%E1%85%A9%E1%84%83%E1%85%B3.png?raw=true)

<!-- 예시 사진은 지워주세요-->
