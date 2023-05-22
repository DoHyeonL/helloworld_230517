 
#  [top]이란 ? 
 ```
top 명령어는 리눅스 시스템의 사용량을 실시간으로 보여주는 명령어. 
 ```
 ```
 ex)실행 예시
 ```
 ![top](https://github.com/DoHyeonL/helloworld_230517/assets/125560095/f05fa5a8-1c24-48a6-ae72-1f8b050e4ca8)
 
 ```
 명령어가 실행된 후 첫번째 문단은 
```
 
 ![top(1)](https://github.com/DoHyeonL/helloworld_230517/assets/125560095/baf4c611-9d82-4a70-8330-692c4f160c3a)

- 현재 시각(10:37:53)
- 경과한 시간(1 min)
- 사용자의 수(1 user) 
- load의 평균(0.49, 0.26, 0.10) 
```
을 표시해주며
```
![top(2)](https://github.com/DoHyeonL/helloworld_230517/assets/125560095/4a989e3c-28e0-4cb7-9d34-ec3bda8747a4)
```
두번째 문단에서는
```
- 실행된 전체 프로세스의 수 
- 현재 진행중인 프로세스의 수 
- 유효상태의 프로세스의 수 
- 종료된 프로세스의 수  
- 좀비 프로세스의 수 
 ```
등을 표시해준다.
```
![top(3)](https://github.com/DoHyeonL/helloworld_230517/assets/125560095/67e815a9-d1ba-4563-b941-77dc7752b7c5)
```
세번째 문단에서는
```
- 사용자가 실행시킨 프로세스의 CPU 사용률
- 시스템 자체에서 사용하고 있는 CPU 사용률
- nice 정책에 의해 사용되 있는 CPU 사용률
- 사용되지 않고 남은 CPU 사용률
- 입출력 대기 상태의 CPU 사용률
- IRQs에 사용된 CPU 사용률
- softIRQs에 사용된 CPU 사용률
- steal의 값
```
등을 표시해준다.
```
![top(4)](https://github.com/DoHyeonL/helloworld_230517/assets/125560095/63b9e40e-7e2f-4eb0-a7c7-cabea3914799)
```
그리고 그 다음 문단에서는 Mem과 Swap의 각 메모리 사용량을 표시해준다.
```
---
```c
- top의 명령어 옵션 -
```

- top -d 1 : 사용량의 갱신 주기를 1초로 변경.(기본 3초)
- top -m : 메모리 사용률을 시각화.

![top5](https://github.com/DoHyeonL/helloworld_230517/assets/125560095/10cb59d5-c07e-4d81-8015-8416ecaf24ae)

- shift + p : CPU 사용률이 높은 프로세스를 기준으로 나열
- shift + t : 수행시간이 긴 프로세스를 기준으로 나열
- k : kill할 프로세스 PID 입력 가능
- h : 상단의 트랙 기준 쓰레드로 변경
- u : 모니터링할 유저를 선택하여 해당 프로세스를 감시
```
등의 옵션들이 있다.
```

---

# [ps]란 ? 
```
현재 실행중인 프로세스의 목록과 상태를 출력하여 보여주는 명령어.
```
![ps](https://github.com/DoHyeonL/helloworld_230517/assets/125560095/6f67262b-926b-4fe1-a8d5-bbbe06d5726b)

```
top은 그때 그때의 사용량을 보여주는 모니터링과 비슷한 개념이라면 ps는 프로세스 전체 사용시간 동안의 CPU 사용량을 보여준다.
```
---
```c
- ps의 사용 옵션 -
```
- ps -ef : 모든 프로세스를 풀 포맷으로 출력한다.

![ps -ef](https://github.com/DoHyeonL/helloworld_230517/assets/125560095/982d9164-ed24-4694-b6ea-b028d40f81f0)

- ps -ef | grep : 모든 프로세스들 중 특정 프로세스를 풀 포맷으로 출력.

![ps -ef _ grep](https://github.com/DoHyeonL/helloworld_230517/assets/125560095/895bedd6-39ff-4d94-9c19-b8bb2c071782)

- ps ax : 시스템의 모든 프로세스를 BSD 포맷으로 출력

![ps ax](https://github.com/DoHyeonL/helloworld_230517/assets/125560095/62e7a12c-d545-441b-99fa-a48d358bcc8b)

- ps aux : 실행중인 모든 프로세스 확인

![ps aux](https://github.com/DoHyeonL/helloworld_230517/assets/125560095/dbc84d66-5421-415a-91c6-ec70f00a4f1f)

- ps auxf : 실행중인 프로세스를 트리구조로 출력
- ps auxfww : 실행중인 프로세스를 트리구조 + 실행중인 옵션 확인 

---

# [jobs]란 ?
```
현재 계정에서 실행중인 작업의 상태 표시하는 명령어.
```

![jobs](https://github.com/DoHyeonL/helloworld_230517/assets/125560095/5eb3531f-ec24-4d65-a28c-00fdb5ee9d2d)

```
- jobs으로 출력되는 작업의 상태값 -
```

- Running : 작업이 계속 진행중인 상태.
- Done : 작업이 완료되어 0을 반환한 상태.
- Done(code) : 작업이 완료되어 0이 아닌 코드를 반환한 상태.
- Stopped : 작업이 일시 중단된 상태.
- Stopped(SIGTSTP) : SIGTSTP 시그널이 작업을 일시 중단한 상태.
- Stopped(SIGSTOP) : SIGSTOP 시그널이 작업을 일시 중단한 상태.
- Stopped(SIGTTIN) : SIGTTIN 시그널이 작업을 일시 중단한 상태.
- Stopped(SIGTTOU) : SIGTTOU 시그널이 작업을 일시 중단한 상태.

```
- jobs의  옵션 -
```

- -l : 프로세스 그룹 ID를 state필드 앞에 출력.
- -n : 프로세스 그룹 중 대표 프로세스 ID를 출력.
- -p : 각 프로세스 아이디에 대해 한 행씩 출력.
- command : 지정한 명령어를 실행.



