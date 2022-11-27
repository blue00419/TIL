(https://codingdog.tistory.com/entry/java-thread-start-vs-run-%EC%96%B4%EB%96%A4-%EC%B0%A8%EC%9D%B4%EA%B0%80-%EC%9E%88%EC%9D%84%EA%B9%8C%EC%9A%94)
thread를 구현하는 방법은 thread 클래스를 상속받는 것과
runnable 인터페이스를 구현하는 방법 2가지가 존재한다.
java는 다중 상속이 안되기 때문에 보통 runnable인터페이스를 구현하는것이 일반적이다.

start(), run()의 차이
- run()을 호출하는 것은 생성된 쓰레드를 실행시키는 것이 아니라 
단순히 클래스에 속한 메서드 하나를 호출하는 것이다.
- start()는 새로운 쓰레드가 작업을 실행하는데 필요한 호출스택을 생성한 다음에
run()을 호출해서, 생성된 호출스택에 run()이 첫번째로 저장되게 한다.
start()의 역할은 new 상태에 있는 쓰레디를 runnable한 상태로 되게 해준다.

무슨 말인지 모르겠고 어렵다.
1. thread를 new해서 한개 만든다.
2. start()를 해서 runnable 상태로 만든다.
3. runnable 상태란 대기 큐에 들어가는 것.
4. 큐에 들어가기 위해선 메타 데이터가 필요하다.
5. 어느 그룹에 속해있는지, 우선 순위는 어떻게 되는지, 기타 등등
6. 그후 override된 run()을 호출해서 동작한다.
7. 2~5의 과정이 start()가 thread를 new 상태에서 run()이 가능한 상태로 만들어 준다는 말이다.

1. thread를 new해서 한개 만든다.
2. run()을 바로 호출한다.
3. 위에서 2~5번의 과정이 빠져 생성된 thread가 뭐하는 놈인지 알 길이 없는데 돌려버린게 된다.

하나의 thread는 두번 start() 시키면 exception이 난다.
