# CSS Masterclass

(S)CSS Layout Masterclass: Flexbox & Grid

## Flexbox:

- [x] flex-direction

* row
  - 기본값, 가로 배열
* column

  - 세로 배열

* flex-direction으로 방향 번경 가능

- [x] order

* 배치 순서를 지정
  - 기본값: 0
  - 수가 커질수록 우선순위 낮아짐

- [x] justify-content

* main-axis

- [x] align-items

* cross-axis

- [x] align-self

* 자식 아이템의 위치를 직접 변경
* 부모의 높이가 지정되어 있어야함

- [x] flex-wrap

* flexbox는 width보다도, '같은 줄'에 있도록 하는 것을 우선시
* nowrap
  * 기본값
  * box에 지정한 크기를 줄여서라도 같은 줄에 있도록 함
* wrap
  * child의 사이즈를 유지하라고 하는 것, 줄바꿈 허용

- [x] align-content

* justify-content와 비슷하지만 'line'에 관한 것
* 행 간 공백을 얼마나 둘건지
<img src="https://i.ibb.co/jhZgMC5/justfiy-content.png" alt="justfiy-content" width="500" height="300">

- [x] flex-grow
* child에게 줄 수 있는 property
* 남아있는 공간이 있을때, 늘어나는 비율을 설정
    * 남아있는 공간이 없다면 원래 지정한 크기로 돌아감
* 기본값 0
- [x] flex-shrink
* child에게 줄 수 있는 property
* nowrap 상태일때, 화면이 작아지면서 줄어드는 비율을 설정
* 기본값 1
- [x] flex-basis
* child에게 줄 수 있는 property
* flex item의 초기 크기를 지정
* main-axis를 기준으로 item들의 크기를 변경
* shrink, grow 적용전에 초기 size

## Grid:

- [x] grid-template-columns
* 각 column의 크기와 개수
- [x] grid-template-rows
* 각 row의 크기와 개수
- [x] column-gap
* column 사이 공간 크기
- [x] row-gap
* row 사이 공간 크기
- [x] gap
* column과 row 사이 공간 크기를 한번에 적용
- [x] grid-template-areas
* 자식들에게 grid-area로 변수를 주면 그것들을 template에 각각의 레이아웃으로 지정가능
    * grid-area에 있는 이름과 grid-template-areas에 있는 이름이 같아야함
    * 조건
        * 같은 영역으로 이어져 있어야함
        * grid-area 지정한곳이 'ㄱ'자나 'ㄴ'자 모양이면 안되고 직사각형이나 정사각형일때만 실행
- [x] grid-column-start
- [x] grid-column-end
- [x] grid-row-start
- [x] grid-row-end
- [x] grid-column
- [x] grid-row
* 자식에게 지정
* grid를 시작하는 라인과 끝나는 라인들을 각각 지정 가능
* 각 라인을 숫자로 인덱싱
    * 뒤에서 부터 인덱싱도 가능 (마지막 라인은 -1)
* span으로 시작점과 끝점을 대신 할수도 있음
    * 숫자와 같이 사용 가능
    * span을 하나의 cell로 인식

- [x] grid-template
* grid-area를 사용
* grid-template-areas 와의 차이점은 row의 높이를 한 행마다 정함
* 마지막 행에 높이와 각각의 넓이를 적어줌
    * ex) footer footer footer footer 1fr / 1fr 1fr 1fr 1fr
* * *
- [x] justify-items
* 수평
- [x] align-items
* 수직
- [x] place-items
* 수직 수평
* 자식들을 늘이거나 이동시켜 grid를 채움
* * *
- [x] justify-content
* 수평
- [x] align-content
* 수직
- [x] place-content
* 수직 수평
* content는 grid 전체배열을 움직여줌

* * *
- [x] justify-self
- [x] align-self
- [x] place-self
* place-items의 작동을 개별적으로 주고싶을때 사용 
* * *
- [x] grid-auto-rows
*  만들어놓은 row보다 더 많은 content가 있으면, 자동으로 row를 만듬
- [x] grid-auto-flow
* flex-direction과 비슷
* row가 끝날 때 새로운 row를 만들지, 새로운 column을 만들지 결정
- [x] grid-auto-columns
* grid-auto-flow: column;일때 작동한다.

* * *

### Keywords & Functions:

- [x] repeat
- [x] fr
* grid에서 사용 가능한 공간
* fr값 비율로 공간을 나눈다
* block은 height가 기본값으로 0이기때문에 container에 height를 값을 주지않으면 fr로 높이 지정이 되지 않음.
- [x] minmax
* 화면 크기가 줄어들거나 늘어날때 한계(제한) 값 설정
* minmax(최소, 최대)
* * *
- [x] auto-fit
* 화면에서 남는 자리를 element들로 채움. (크기 화면에 맞게 늘어남)
- [x] auto-fill
* 화면에서 남는 자리를 빈 칸으로 채움. (크기 고정, 칸 수 늘어남)
<br>
<img src="https://i.ibb.co/tMypbkR/auto.png" alt="auto" border="0">
6번 박스가 추가가 되면 fill은 빈 칸에 추가 되고, fit은 다른 박스들의 넓이를 줄여 6개가 꽉차게 배치

* * *
- [x] min-content
* content의 크기를 최대한 줄여 cell의 크기를 줄인다.
- [x] max-content
* content의 크기만큼 cell의 크기를 늘린다.
* repeat(), minmax와 결합하여 반응형 디자인을 만들 수 있다.
## SCSS:
- [x] Variables
* _variables.scss
* 앞에 _ 붙어있으면 css로 변하지 않았으면 하는 것들
* &변수명 : 속성값; 
- [x] Nesting
* 타켓하는 코드를 명확하게 해줌
* 프로그래밍 언어처럼 선택자 중괄호 안에 선택자를 넣게되면 자식 이 됨

- [x] Partials
- [x] Mixins
* 함수와 비슷한 동작을 하는 문법이며, CSS를 반복적으로 재사용할 스타일 그룹 선언을 정의
* 상황에 따라 다르게 코딩을 하고 싶을때 사용
- [x] Extend
* 다른 코드를 확장하거나 같은 코드를 중복하고 싶지 않을때 사용

- [x] Responsive
* Mixin에서 미디어 쿼리를 이용해 반응형 CSS를 구현