# Variables
## val
- read-only
- 값(value)에서 온 키워드로 읽기 전용 또는 한 번만 할당 가능한 변수를 의미
- 본질적으로 java의 final 변수에 해당하기 때문에 참조를 변경할 수 없다는 의미
- 객체의 메서드를 호출하여 내부 내용을 변경할 수 있다. 
- 즉, 변수에 다른 참조를 대입할 수는 없지만, 해당 객체를 쉽게 수정할 수는 있다.

## var
- mutable
- 변수(variable)에서 온 키워드로 변경될 수 있는 변수를 의미

### Lists: mutable & read-only
- read-only list 를 수정할 수 없어 오류가 발생한다.
```kotlin
val list = listOf("java")
list.add("kotlin")
```
- mutableListOf 를 사용하면 수정 가능한다.
```kotlin
val mutableList = mutableListOf("java")
mutableList.add("kotlin")
```

### 정리
- 기본적으로 var 가 아니라 'val 을 쓰도록 노력한다.
- 왜냐하면, 사이드 이펙트가 없는 변경 불가능한 참조, 변경 불가능한 객체와 함수를 사용하여
코드를 함수형 프로그래밍에 가깝게 작성하면 결국 좀 더 쉽게 이해하고 지원할 수 있다.
- 타입이 문맥상 분명한 경우 명시하지 않고 생략해도 안전하다.