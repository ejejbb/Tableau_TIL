# 9주차 문제

여러 대시보드를 참고하시어, 학술제 주제 관련 데이터(없을 경우, 본인 관심 데이터)를 사용해 나만의 대시보드를 제작해주세요.

**단, 워크시트 3개 이상의 그래프를 표시해야 하며 각 시트 간 상호작용성 필터 or 하이라이트 동작은 꼭 추가되어야 합니다.**

어떤 부분에 가중을 두었는지, 어떤 사용자 편의성을 고려하였는지에 대한 설명이 필요합니다.

---

### 사용한 데이터셋
https://www.kaggle.com/datasets/nelgiriyewithana/billionaires-statistics-dataset   
이 데이터에서 미국 데이터만 필터링하여 사용

### 대시보드 링크(태블로 퍼블릭)
https://public.tableau.com/app/profile/.63651269/viz/_17332482594500/sheet12?publish=yes
---
### 대시보드 설명
대시보드1. [미국의 억만장자]
1) 상단의 표: 미국의 인구, gdp, 조세율, 조세수익을 볼 수 있도록 하였다.
2) 맵차트
- 각 state 위에 마우스오버하면 state명, 그 주에 부자가 몇 명 있는지, 그리고 final worth의 합계가 상세정보로 나오게 하였다.
- state에 필터 동작을 추가하여 각 state를 클릭하면 우측의 그래프들이 변하도록 하였다.
3) 막대그래프: 각 막대그래프를 클릭하면 person name에 해당하는 wikipedia url이 상세정보에 나오도록 하였다.
4) 버블차트: 연령대별로 부자가 몇 명이나 있는지 한 눈에 볼 수 있도록 하였다.
5) 트리맵: 산업별로 부자가 몇 명이나 있는지 한 눈에 볼 수 있도록 하였다. -> 워드클라우드보다 트리맵이 좁은 면적 시각화에 유리하였다.
6) 탐색버튼: 우측상단에 탐색버튼을 삽입하여 별자리 대시보드로 이동할 수 있도록 하였다.

대시보드2. [별자리]
이미지를 클릭하면 값이 변하도록 만들고 싶었으나 이미지는 데이터의 값과 연동되지 않으므로 birthday를 별자리별로 그룹화하여 별자리별 final worth를 막대그래프로 시각화하고 각 막대그래프를 클릭하면 표의 값들이 변하도록 하였다.
1) 표1: count, 해당 별자리에 미국의 억만장자가 몇 명이나 있는지 보여준다.
2) 표2: top1, 해당 별자리 중에서 가장 재산이 많은 사람은 누구인지 보여준다. 이 표 위에 마우스오버하면 이름, 이 사람이 일하는 분야, final worth, 전세계 기준 재산 순위를 보여준다.
3) 탐색버튼: 다시 미국의 억만장자 대시보드로 돌아갈 수 있도로 하였다.


