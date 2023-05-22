 ```
- [top]이란 ? -
 
   top 명령어는 리눅스 시스템이 실행이 시작된 순간부터 현재까지의 시스템 사용량을 실시간으로 보여주는 명령어입니다. 
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
```c
- top의 사용 옵션 -
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
