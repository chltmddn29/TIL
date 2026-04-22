# widgetsBinding

## widgetsBinding

flutter의 위젯 레이어와 엔진 사이의 연결 역할을 해주는 것

### 주요역할

1. 프레임 스케쥴링 : 언제 위젯을 다시 그릴지 결정
2. 생명 주기 관리 : 앱의 생명주기 처리
3. 입력 처리 : 터치, 키보드 입력 등 위젯에 터치 전달

### 계층구조

<img width="1098" height="520" alt="image" src="https://github.com/user-attachments/assets/eb6890bf-091a-487b-812c-dc67f0fc9ea6" />


이러한 구조를 가진다.

각 바인딩의 역할로는

GestureBinding : 제스쳐 인식

SchedulerBinding : 스케쥴링 관리

ServicesBinding : 플랫폼 채널 및 시스템 서비스 관리

PaintingBinding : 이미지 캐시 관리

semanticsBinding : 접근성 트리 관리

RenderBinding : 렌더 트리 관리

WidgetBinding : 위젯 트리 관리
