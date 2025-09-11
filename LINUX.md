## 1과목 - 리눅스 운영 및 관리

### 1. 사운드, 스캐너, 프린터

* **ALSA (Advanced Linux Sound Architecture)**

  * 리눅스에서 사운드 카드 지원 시스템.
  * **명령어**: `alsactl`
  * **기능**: 사운드 카드 설정 및 관리.

* **SANE (Scanner Access Now Easy)**

  * 스캐너, 비디오 카메라 등 이미지 장치 API.
  * **참고**: XSANE는 X 윈도 환경에서 스캐너 사용을 돕는 도구.

* **CUPS (Common UNIX Printing System)**

  * 프린터와 관련된 관리 시스템.
  * **주요 명령어**:

    * `lp`: 프린터 작업 요청
    * `lpq`: 프린터 큐 상태 확인
    * `lprm`: 프린트 대기 작업 삭제
    * `lpc`: 프린터 컨트롤 프로그램

---

### 2. 파일 시스템 및 저장장치

* **RAID**

  * **RAID 5**: 최소 3개의 디스크, 1개의 패리티
  * **RAID 6**: 최소 4개의 디스크, 2개의 패리티

* **LVM (Logical Volume Manager)**

  * **PE (Physical Extent)**: 물리적 볼륨의 작은 단위
  * **VG (Volume Group)**: 물리 볼륨(PV)을 결합한 그룹
  * **LV (Logical Volume)**: 사용자가 설정한 논리 볼륨

* **Mirroring**

  * 데이터를 두 개의 디스크에 복제하여 오류 방지

---

### 3. 명령어

* **RPM 명령어**

  * `rpm -e <package>`: 패키지 삭제
  * `rpm -i <package>`: 패키지 설치
  * `rpm -U <package>`: 패키지 업그레이드
  * `rpm -F <package>`: 이전 버전 설치
  * `rpm -V <package>`: 패키지 검증

* **압축 명령어**

  * `tar xvf`: tar 파일 해제
  * `tar cvf`: tar 파일 생성
  * `xz`, `bz2`, `gz`, `compress`: 압축 효율성 순위

* **소스 코드 설치**

  * 순서: `configure` → `make` → `make install`

---

### 4. 패키지 관리

* **YUM 명령어**

  * `yum list`: 패키지 정보 출력
  * `yum history`: 패키지 관리 이력
  * `yum grouplist`: 그룹별 패키지 목록

* **APT 명령어**

  * **패키지 파일 형식**: `.deb`
  * `apt-get remove <package>`: 패키지 제거

* **기타 패키지 관리 도구**

  * `rpm`, `YaST`, `dpkg`: 오프라인 패키지 관리
  * `zypper`: SUSE 리눅스 패키지 관리 도구
  * `pacman`: 아치 리눅스 패키지 관리 도구

---

### 5. 편집기

* **vi**

  * `set nu`: 라인 번호 표시
  * `set ai`: 자동 들여쓰기
  * `set sm`: 괄호 강조

* **vim**

  * 문법 강조, 하이라이트 검색 기능

* **pico/nano**

  * `nano`: 사용 간편한 텍스트 편집기

* **emacs**

  * 다중 언어 지원, 고급 편집 기능

---

## 2과목 - 시스템 명령어 및 프로세스 관리

### 1. 프로세스 관련 명령어

* **`nice`**

  * 프로세스 우선순위 조정: `nice -n 10 bash`

* **`renice`**

  * 실행 중인 프로세스 우선순위 변경: `renice 10 -p 1234`

* **`ps`**

  * 실행 중인 프로세스 상태 확인: `ps aux`

* **`top`**

  * 실시간 CPU, 메모리 사용량 모니터링

* **`jobs`**, **`fg`**, **`bg`**

  * 백그라운드 및 포그라운드 작업 관리

---

### 2. 시스템 호출

* **`fork`**

  * 새로운 프로세스 생성

* **`exec`**

  * 프로세스 덮어쓰기

---

## 3과목 - 파일 시스템 관리

### 1. 파일 시스템 관련 명령어

* **`mount`**

  * 파일 시스템을 마운트: `mount -t ext4 /dev/sdb1 /mnt`

* **`umount`**

  * 파일 시스템 해제: `umount /mnt`

* **`mke2fs`**, **`mkfs.xfs`**

  * `ext4`, `XFS` 파일 시스템 생성

* **`/etc/fstab`**

  * 자동 마운트를 위한 파일, UUID로 장치 연결

---

## 4과목 - 시스템 설정

### 1. 셸 및 환경 설정

* **셸 종류**:

  * `bash`: 기본 셸
  * `csh`: C쉘
  * `ksh`: Korn 셸
  * `tcsh`: 확장 C쉘

* **환경설정 파일**

  * `~/.bashrc`: 사용자별 환경 설정
  * `~/.bash_profile`: 로그인 환경 설정
  * `/etc/profile`: 시스템 전체 환경 설정

---

### 2. 사용자 및 그룹 관리

* **`/etc/passwd`**

  * 사용자 기본 정보 저장

* **`/etc/shadow`**

  * 비밀번호 및 보안 정보 저장

* **`/etc/group`**

  * 그룹 정보 저장

* **`chsh`**

  * 셸 변경: `chsh -s /bin/bash`

---

## 5과목 - 크론 (CRON)

### 1. CRON 설정

* **`crontab`**

  * 주기적인 작업 자동화: `crontab -e`

* **`crontab -l`**

  * 현재 설정된 크론 작업 확인

* **크론 주기 표현식**:
  `분 시 일 월 요일`

---

## 6과목 - 파일 권한 및 보안

### 1. 파일 권한 관리

* **`chmod`**

  * 파일 권한 변경: `chmod 755 <file>`

* **`chown`**

  * 파일 소유자 변경: `chown user:group <file>`

* **`chgrp`**

  * 파일 그룹 변경: `chgrp group <file>`

---

이렇게 모든 내용을 보기 좋게 정리해 드렸습니다. 각 항목별로 중요한 키워드나 명령어를 요약하고, 한눈에 이해할 수 있도록 구조를 잡았습니다. 추가적으로 수정할 부분이나 다른 형식이 필요하시면 알려주세요!
