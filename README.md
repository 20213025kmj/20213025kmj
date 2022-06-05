# 리눅스 명령어
------------------------
   ### 1. top
   > 실시간으로 CPU 사용률을 체크해주는 도구
  
   ### _top 정보 시스템 내용_
   * 00:00:00 현재 서버 시간
   * 0 days, 00:00 : uptime 켜져있는 시간
   * 0 users 유저의 수
   * load average 현재 시스템이 얼마나 일을 하고 있는지
   * Tasks 프로세스의 개수
     
   ### CPU
   * %us : 유저레벨에서 사용하고 있는 CPU 비중
   * %sy : 시스템 레벨에서 사용하고 있는 CPU 비중
   * %id : 유휴 상태의 CPU 비중
   * %wa : 시스템이 I/O 요청을 처리하지 못한 상태에서의 CPU idle 상태인 비중
     
   ### 메모리
   > Mem
   * total : 전체 물리적인 메모리
   * used : 사용중인 메모리
   * free : 사용되지 않는 여유 메모리
   * buffers : 버퍼된 메모리
   
   > Swap 
   * total : 전체 스왑 메모리
   * used : 사용중인 스왑 메모리
   * free : 남아있는 스왑 메모리
   * cached : 캐싱 메모리

  ### 프로세스 상태
  * PID : 프로세스 ID (PID)
  * USER : 프로세스를 실행시킨 사용자 
  * IDPRI : 프로세스의 우선순위 (priority)
  * NI : NICE 값. 일의 nice value값이다. 마이너스를 가지는 nice value는 우선순위가 높음.
  * VIRT : 가상 메모리의 사용량(SWAP+RES)
  * RES : 현재 페이지가 상주하고 있는 크기(Resident Size)
  * SHR : 분할된 페이지, 프로세스에 의해 사용된 메모리를 나눈 메모리의 총합.
  * S : 프로세스의 상태
  * %CPU : 프로세스가 사용하는 CPU의 사용율
  * %MEM : 프로세스가 사용하는 메모리의 사용율
  * COMMAND : 실행된 명령어
--------------------------
  ### _top 실행 후 명령어_
  명령어 | 설명
  --- | ---
  shift + p | CPU 사용률이 높은 프로세스 순서대로 표시
  shift + m | 메모리 사용률이 높은 프로세스 순서대로 표시
  shift + t | 프로세스가 돌아가고 있는 시간 순서대로 표시
  -k | 프로세스  kill  - k 입력 후 종료할 PID 입력 signal을 입력하라고 하면 kill signal인 9를 입력
  -a | 메모리 사용량에 따라 정렬
  -b | Batch 모드 작동
  -c | 명령행/프로그램 이름 토글
  -d | 지연 시간 간격은 다음과 같다. -d ss. tt (seconds.tenths)
  -h | 도움말 
  -H | 스레드 토글
  -i | 유휴 프로세스 토글
  -m | VIRT/USED 토글
  -M | 메모리 유닛 탐지
  -n | 반복 횟수 제한 : -n number
  -p | PID를 다음과 같이 모니터 : -pN1 -pN2 ... or -pN1, N2 [, ...] 
  -s | 보안 모드 작동
  -S | 누적 시간 모드 토글
  -u | 사용자별 모니터링 : -u somebody
  -U | 사용자별 모니터링 : -U somebody
  -v | version
  space bar | refresh
  -u | 입력한 유저의 프로세스만 표시 -which u
  숫자 1 | CPU Core별로 사용량을 보여준다.
  -------------------- 
  ### 2. ps 
  > 프로세스에 대한 정보를 얻기 위한 명령어
  >> 사용방법
  >> ps [OPTION]
  
  ### 프로세스 정보
  * PID - 프로세스 ID  PID를 알면 오작동하는 프로세스를 제거할 수 있음
  * TTY - 프로세스의 제어 터미널 이름
  * TIME - 프로세스의 누적 CPU 시간(분 및 초)입니다.
  * CMD - 프로세스를 시작하는 데 사용된 명령의 이름입니다.
  
  ### 옵션 
  옵션 | 설명
  --- | ---
  -e | 모든 프로세스를 출력해 준다.
  -f | 풀 포맷으로 보여준다.(UID, PID 등)-l 긴 포맷으로 보여준다.
  p, -p | 특정 PID의 프로세스를 보여준다.
  -u | 특정 사용자의 프로세스를 보여준다.
  -ef |  UID, PID, PPID, C, STIME, TIME 및 CMD 레이블이 정보를 표시함
  
  * UID - 프로세스를 실행하는 사용자인 USER와 동일
  * PPID - 상위 프로세스의 ID
  * C - %CPU와 동일, 프로세스 CPU 활용도
  * STIME - = START


  
