## 프로세스와 스레드
### 프로세스(Process)
<img src="https://user-images.githubusercontent.com/62992052/105209806-9c8dff00-5b8d-11eb-8cbd-aecb068dbb73.png" width="500">
#### 정의
 - 컴퓨터에서 연속적으로 실행되고 있는 프로그램
 - 메모리에 올라와 실행되고 있는 프로그램 인스턴스(독립적 개체)
 - OS로부터 시스템 자원을 할당받는 작업의 단위
 - 동적 개념으로 실행된 프로그램

cf. OS가 할당해주는 시스템 자원의 예
 - CPU 시간
 - 운영되기 위해 필요한 주소 공간
 - Code, Data, Stack, Heap 구조의 독립된 메모리 영역

#### 특징

- 프로세스는 각각 독립된 메모리영역을 할당받는다
- 프로세스당 최소 1개의 스레드를 가진다 -> main thread
- 각 프로세스는 별도의 주소공간에서 실행되며 타 프로세스의 변수나 자료구조에 접근불가
- 한 프로세스가 다른 프로세스에 접근하려면 프로세스간 통신(IPC, Inter Process Communication) 을 사용해야한다.
	- e.g., 파이프(PIPE), 메세지 큐(Message Queue), 공유메모리(Shared Memory), 소켓(Socket)  등을 이용한 통신방법 이용
</br>
### 스레드(Thread)
<img src="https://user-images.githubusercontent.com/62992052/105209813-9dbf2c00-5b8d-11eb-9064-baba373b5ca7.png" width="500">
#### 정의
 - 프로세스 내에서 실행되는 여러 흐름의 단위
 - 프로세스의 특정한 수행 경로
 - 프로세스가 할당받은 자원을 이용하는 실행의 단위

#### 특징
 - 스레드는 프로세스 내에서 각각 Stack만 따로 할당받고, Code, Data, Heap 영역은 공유
 - 스레드는 한 프로세스 내에서 동작되는 여러 실행의 흐름으로, 프로세스 내의 주소공간이나 자원(힙 공간 등)을 같은 프로세스 내에 스레드끼리 공유하며 실행
 - 한 스레드가 프로세스 자원을 변경하면, 다른 이웃 스레드(sibling thread)도 변경 결과를 즉시 볼 수 있다.
</br>
### 자바 스레드

#### 추후 보충

---
#### 참고
> https://gmlwjd9405.github.io/2018/09/14/process-vs-thread.html
> https://coding-factory.tistory.com/279
