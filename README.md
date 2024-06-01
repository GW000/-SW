
# <div align="center">오픈소스SW개론</div> 
### <div align="right">20194058 임건우 </div>


## <div align="center">[과제] 리눅스(Linux)의 명령어 조사 후 README 파일 작성하기</div>  

### 1. top
> top(table of processes) 명령어는 시스템 성능 정보를 실시간으로 출력하는 명령어입니다.

> + top : 서버구동 시간에 대한 정보를 표시합니다.
>
> + Tasks : 프로세스의 상태 정보를 표시합니다.
>
> + %Cpu(s) : CPU데 대한 정보를 표시합니다.
>   + us : 사용자의 CPU사용 비중을 표시합니다.
>   + sy : 시스템의 CPU사용 비중을 표시합니다.
>   + ni : 우선순위가 낮은 프로세스의 CPU사용 비중을 표시합니다.
>   + id : 유휴 상태의 CPU사용 비중을 표시합니다.
>   + wa : I/O를 대기중인 CPU 사용률을 표시합니다.
>   + hi : 하드웨어 인터럽트를 관리하는 시간의 비율을 표시합니다.
>   + si : 소프트웨어 인터럽트를 관리하는 시간의 비율을 표시합니다.
>   + st : 가상 CPU가 실제 CPU를 기다리는 시간을 표시합니다.
>
> + MiB Mem : 실제 메모리 사용량을 표시합니다.
>   + total : 총 메모리를 표시합니다.
>   + free : 사용 가능한 메모리를 표시합니다.
>   + used : 사용중인 메모리를 표시합니다.
>   + buff/cache : 버퍼및 캐시로 자용중인 메모리를 표시합니다.
>     
> + MiB Swap : 스왑 메모리 사용량을 표시합니다.
>   + total : 총 스왑 메모리를 표시합니다.
>   + free : 사용 가능한 스왑 메모리를 표시합니다.
>   + used : 사용중인 스왑 메모리를 표시합니다.

| 명령어 |<div align="center">설명</div> |
|:---:|:---|
|**1**|CPU Core별로 사용량을 보여줍니다.|
|**k**|kill 할 프로세스 PID를 입력하여 프로세스를 종료합니다.|
|**a**|메모리 사용량에 따라 정렬합니다.|
|**b**|Batch 모드로 작동합니다.|
|**f**|정렬 기준을 변경합니다.|
|**h**|도움말을 표시합니다.|
|**Shift + p**|CPU 사용률을 내림차순으로 정렬합니다.|
|**Shift + m**|메모리 사용률을 내림차순으로 정렬합니다.|
|**Shift + t**|프로세스가 돌아가고 있는 시간 순으로 정렬합니다.|
***
### 2. ps
> ps(process Status) 명령어는 현재 구동중인 프로세스의 정보를 출력하는 명령어입니다.

> + USER : BSD 계열에서 나타나는 항목으로 프로세스 소유자의 이름을 표시합니다.
>
> + Tasks : System V 계열에서 나타나는 항목으로 프로세스 소유자의 이름을 표시합니다.
>
> + PID : 프로세스 식별번호를 표시합니다.
>
> + PPID : 상위 프로세스 ID를 표시합니다.
>
> + %CPU : (BSD)CPU사용 비율의 추정치를 표시합니다.
>
> + %MEM : (BSD)메모리사용 비율의 추정치를 표시합니다.
>
> + VSZ : KB단위 또는 페이지 단위의 가상메모리 사용량을 표시합니다.
>
> + RSS : 실제 메모리 사용량을 표시합니다.
>
> + TTY : 프로세스와 연결된 터미널을 표시합니다.
>
> + S/STAT : 현재 프로세스의 상태코드를 표시합니다. (S: System V / STAT : BSD)
>   
> + TIME : 총 CPU시간을 표시합니다.
>
> + COMMAND : 프로세스의 실행 명령행을 표시합니다.
>
> + STIME : 프로세스가 시작된 시간을 표시합니다.
>
> + C/CP : 짧은 시간동안의 CPU 사용률을 표시합니다. (C : System V / CP : BSD)
>
> + F : 프로세스의 플래그를 표시합니다.
>
> + PRI : 실제 실행 우선순위를 표시합니다.
>
> + NI : 우선순위 번호를 표시합니다.
>
```bash
$ ps [option]
```
| 옵션 |<div align="center">설명</div> |
|:---:|:---|
|**a**|모든 프로세스를 출력합니다.|
|**e**|커널 프로세스를 제외한 모든 프로세세스를 출력합니다.|
|**f**|풀 포맷으로 보여줍니다.|
|**l**|긴 포맷으로 보여줍니다.|
|**o**|출력 포맷을 지정합니다.|
|**p**|특정 PID를 지정합니다.|
|**r**|현재 실행중인 프로세스를 출력합니다.|
|**u**|특정 사용자의 프러세스 정보를 출력합니다.|
|**x**|터미널에 종속되지 않은 프로세스를 출력합니다.|
***
### 3. jobs
> 백그라운드로 실행 중인 프로세스나 현재 중지된 프로세스의 목록을 출력해 주는 명령어입니다.

> + Running : 현재 실행중인 상태입니다.
>
> + Stopped : 일시중단된 상태입니다.
>
> + Done : 완료된 상태입니다.
>
> + Terminated : 강제 종료된 상태입니다.

```bash
$ jobs [option]
```
| 옵션 |<div align="center">설명</div> |
|:---:|:---|
|**p**|프로세스 ID를 출력합니다.|
|**e**|현재 실행중인 모든 프로세세스를 출력합니다.|
|**f**|유저 명, 시작시간을 출력합니다.|
|**l**|프로세스 상태를 출력합니다.|
|**n**|상태변화가 일어난 작업을 출력합니다.|
***
### 4. kill
***
