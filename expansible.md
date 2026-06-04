# flutter 위젯

# expansible 위젯

## expansible 위젯이란?

확장형 위젯으로 숨겨있는 히든 위젯과 항상 보이는 헤더 위젯 두개의 속성을 제공한다.

사용자가 헤더 위젯을 탭하여야만 히든 위젯을 볼수 있게 된다.

## 주요 속성

1. bodyBuilder : 숨겨진 위젯
2. controller : 위젯들을 조종할 컨트롤러
3. headerBuilder : 앞에서 보여주는 기본적인 위젯
4. animationStyle : 애니메이션의 스타일을 지정하고 싶을때 사용 (duration, curve)
5. expansibleBuilder : expansible 위젯 직접 커스텀 가능

### 코드 예제

```jsx
class Ex extends StatefulWidget {
  const Ex({super.key});

  @override
  State<Ex> createState() => _ExState();
}

class _ExState extends State<Ex> {
  final _controller = ExpansibleController();

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      body: Column(
        mainAxisAlignment: MainAxisAlignment.center,
        children: [
          Expansible(
            headerBuilder: (context, animation) {
              return GestureDetector(
                onTap: () {
                  _controller.isExpanded
                      ? _controller.collapse()
                      : _controller.expand();
                },
                child: Container(
                  padding: EdgeInsets.symmetric(horizontal: 100, vertical: 100),
                  decoration: BoxDecoration(
                    color: Colors.grey,
                    borderRadius: BorderRadius.circular(10),
                    border: Border.all(color: Colors.green),
                  ),
                  child: Text(
                    '이걸 눌러보세요',
                    style: TextStyle(fontSize: 50, color: Colors.white),
                  ),
                ),
              );
            },
            bodyBuilder: (context, animation) {
              return Text('안녕하세요', style: TextStyle(fontSize: 40));
            },
            controller: _controller,
          ),
        ],
      ),
    );
  }
}

```

## 사용하는 곳

1. 어떠한 위젯에 상태변화가 나타났을때 숨겨진 것을 나타내고 싶을때
