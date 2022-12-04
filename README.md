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

- [ ] grid-template
- [ ] justify-items
- [ ] align-items
- [ ] place-items
- [ ] justify-content
- [ ] align-content
- [ ] place-content
- [ ] justify-self
- [ ] align-self
- [ ] place-self
- [ ] grid-auto-rows
- [ ] grid-auto-flow
- [ ] grid-auto-columns

### Keywords & Functions:

- [ ] repeat
- [ ] fr
- [ ] minmax
- [ ] auto-fit
- [ ] auto-fill
- [ ] min-content
- [ ] max-content

## SCSS:

- [ ] Variables
- [ ] Nesting
- [ ] Partials
- [ ] Mixins
- [ ] Extend
- [ ] Responsive
