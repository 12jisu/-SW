# -SW
# 1. top 명령어
> 시스템의 상태를 전반적으로 가장 빠르게 파악 가능할 수 있는 명령어
> > 옵션 없이 입력하면 간격을 기본 3초로 두고 화면을 갱신하여 정보를 보여준다.
  ## 1) top 명령어를 실행하기 전 옵션
     - b : 순간의 정보를 확인
     - n : top 실행 주기 설정(반복 횟수)
  ## 2) top 명령어를 실행한 후 명령어
     - shift + p : CPU 사용률 내림차순으로 정리
     - shift + m : 메모리 사용률 내림차순으로 정리
     - shift + t : 프로세스가 돌아가고 있는 시간 순서
     - k : kill.k를 입력 후, PID 번호를 작성 (signal은 9)
     - f : sort field를 선택 후 화면 -> q를 누르면 RES 순으로 정렬
     - a : 메모리 사용량에 따라 정렬
     - b : Batch 모드로 작동
     - 1 : CPU Core별로 사용량 보여줌

--------------------------------------------------------------------------------------------       
    
# 2. ps 명령어
> Process State의 약자로, 현재 실행 중인 프로세스와 상태를 출력하는 명령어
> > ps 명령어의 옵션은 각 시스템 계열 System V(-), BSD(-사용 안 함), GNU(--)마다 다른 표기법 출력
  ## 1) ps 명령어 출력 항목
     - USER(BSD) : 프로세스 소유자의 이름
     - PID : 프로세스의 식별 번호
     - PPID : 부모 프로세스의 PID
     - %CPU : CPU 사용 비율의 추정치
     - %MEM : Memory 사용 비율의 추정치
     - VSZ : K 단위 또는 페이지 단위의 가상 메모리 사용량
     - RSS : 실제 메모리 사용량
     - TTY : 프로세스와 연결된 터미널
  ## 2) ps 명령어 옵션
     - A : 모든 프로세스를 출력
     - a : 터미널에 종속되지 않은 모든 프로세스를 출력
     - e : 커널 프로세스를 제외한 모든 프로세스를 출력
     - f : 출력을 풀 포맷으로 표기 (UID, PID, PPID 등이 함께 표시)
     - o : 출력 포맷을 지정
     - M : 64비트 프로세스들을 출력
     - m : 프로세스뿐만 아니라 커널 스레드도 출력
     - p : 특정 PID를 지정하여 출력
 
--------------------------------------------------------------------------------------------       

# 3. jobs 명령어
> 셸에서 실행중인 프로세스 목록을 확인할 수 있는 명령어
> > 현재 쉘 세션에서 실행시킨 백그라운드 작업의 목록이 출력되며, 각 작업에는 번호를 붙여서 사용 가
  ## 1) jobs 명령어 옵션
     - l : 프로세스 ID와 함게 job 목록을 출력
     - n : 마지막으로 알림 이후 변경된 job만 출력
     - p : job의 프로세스 ID만 출력
     - r : 실행 중인 job만 출력
     - s : 중지된 job만 출력
     - command : 지정된 명령어를 실행

--------------------------------------------------------------------------------------------       

# 4. kill  명령어
> 프로세스에 신호를 보내어 그 프로세스를 종료하거나 다시 시작하는 데 사용되는 명령어
> > 기본 구문은 kill [옵션][프로세스 ID]
  ## 1) kill 명령어 주요 옵션
     - l : 모든 시그널 목록을 표시
     - s : 지정한 시그널을 보냄
     - 9 : SIGKILL 시그널을 보내어 강제 종료
     - 15 : SIGTERM 시그널을 보내어 정상 종료를 요청

--------------------------------------------------------------------------------------------       
