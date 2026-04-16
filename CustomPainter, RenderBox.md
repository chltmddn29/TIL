# CustomPainer와 RenderBox

## CustomPainter란

### 더 유연하고 세밀한 직접 화면에 그리기 위한 저수준의 API

예) 벡터 그래픽, 차트, 복잡한 애니메이션 등

## CustomPainter 사용법

1. CustomPainter를 상속받는 클래스 만들기
2. CustomPaint 사용
3. Paint 객체로 정의

## RenderBox란

Flutter 렌더링의 핵심 요소, 위젯과 레이아웃과 그리기 사용, 보통 바로 사용하기보단

위젯 API로 간접적으로 사용

### RenderBox 렌더링 시스템의 구조

1. 위젯 : 사용할 위젯
2. 요소 : 위젯에서 사용하는 세부 요소
3. 렌더 객체 : 실제로 렌더링할 것들

## CustomRenderBox 사용법

1. RenderBox를 상속받는 클래스 만들기
2. SingleChildRenderObjectWidget을 상속받는 위젯 만들기
3. SingleChildRenderObjectElement를 확장하는 요소 만들기(필요할때만)

## CustomPainter와 RenderBox의 차이점

1. 목적의 차이
    1. CustomPainter : 그리기
    2. RenderBox : 레이아웃과 그리기
2. 구현의 차이
    1. CustomPainter : 구현의 상대적으로 쉬움
    2. RenderBox : 구현이 어렵지만 유연하여 사용성 높음
