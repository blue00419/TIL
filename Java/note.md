특징
Java는 [객체 지향 프로그래밍](https://github.com/blue00419/TIL/blob/main/OOP/note) 언어다.

JVM만 설치하면 OS에 종속되지않고 작동한다.

기본 자료형을 제외한 모든 요소들이 객체로 표현된다.

[Garbage Collector](https://github.com/blue00419/TIL/blob/main/Garbage Collector/note)를 통해 자동으로 메모리를 관리한다.

[멀티쓰레드](https://github.com/blue00419/TIL/blob/main/Multi-Thread/note)를 지원한다.

Call by Reference와 Call by Value의 차이점
- Call by Reference
매개 변수의 원래 주소에 값을 저장하는 방식
클래스 객체를 인수로 전달한 경우
(ex. 객체를 2개를 생성해서 각각 10, 20의 값을 넣고 swap메서드에 int 값이아닌 클래스를 객체를 넘겨 서로 값을 바꾸면 정상적으로 값이 변경된다.)
- Call by Value
주어진 값을 복사하여 처리하는 방식
기본 데이터형을 인수로 전달한 경우
(ex. int형으로 10, 20의 값을 선언하고 swap메서드에 넣으면 메서드내에서는 값이 변하지만 메서드를 빠져나가면 변경사항이 적용되지 않는다. 안과 밖이 영향을 끼치지 못함)

오버로딩, 오버라이딩 차이
- 오버로딩
같은 이름의 메서드를 여러개 만들어서 매개변수의 유형과 개수, 리턴 타입 등을 다르개 정의해서 사용.
(ex. int sum(int a, int b), double sum(double a, double b))
- 오버라이딩
부모 클래스에 있는 메소드를 자식 클래스에서 재정의해 사용.
자식 클래스에서 부모 클래스의 메소드를 재정의 했지만 부모 클래스의 메소드 또한 호출하고 싶은 경우엔 super 예약어를 사용한다.
오버로딩과 오버라이딩 둘다 메서드 이름은 동일해야한다.

[Runnable과 Thread의 차이점](https://github.com/blue00419/TIL/blob/main/Java/Runnable%20and%20Thread.md)


Constructor(생성자)
- 값을 초기화 할 때 사용
- 객체 생성시 필요한 필드 값을 받도록 강제하는 역할
- 상속 시 최상위의 생성자부터 초기화한 후 최하위의 생성자까지 실행되어 자식 객체 생성.
- 하위 클래스에서 상위 클래스의 매개변수가 존재하는 생성자를 호출하고 싶으면 super() 예약어를 사용하여 명시적으로 생성자를 호출해야한다.

this, super 예약어
- this는 클래스 내에 맴버 변수나 메소드를 가리킬 수 있다.
- super는 상위 클래스 내에 맴버 변수나 메소드를 가리킬 수 있다.
상위 클래스의 접근 범위가 public이나 protected로 되어 있어야 접근 가능

접근 제한자
클래스 정의시에 접근, 사용에 대한 제한을 주기 위한 제한자
- public 접근 제한이 없다.
- protected 같은 패키지에 있는 객체와 상속관계의 객체들만 접근 가능
- default 같은 패키지 내에서만 접근 가능
- private 같은 클래스 내에서만 접근 가능

쓰레드와 프로세스
