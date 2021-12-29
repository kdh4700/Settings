# 1장. Git이란?

# Git을 사용하는 이유

- 효울적인 협업
e.g. 공동 작업 시 업로드 버전이 서로 다를 수 있음
각 버전을 통합하는게 필요함 git 사용 시 자동으로 처리할 수 있음
- 쉬운 버전관리
e.g. 기존 버전 관리 방식은 하나의 파일을 여러 버전으로 나누어 저장
git은 각 파일을 스냅샷 형식으로 저장하여 각 스냅샷 버전으로 이동 가능

# Git의 특징

- 가지 치기와 병합
e.g. 여러가지 작업 시 다른 작업을 독립적으로 진행이 가능하며 추후 병합 적용 가능

![Untitled](https://user-images.githubusercontent.com/51807451/147663052-66bb8d5c-cc1a-404f-89b3-8e060c466d5b.png)

- 가볍고 빠르다. 
대부분의 git 작업은 로컬에서 작업 (svn에 모든 코드는 중앙시스템 git은 모든 코드가 로컬에 있고 수정 병합 시에만 중앙시스템 이용)
- 분산 작업 
e.g. 각 사용자끼리 연결이 단절되도 문제가 생기지 않음
통합관리자는 병합에만 집중

![1%E1%84%8C%E1%85%A1%E1%86%BC%20Git%E1%84%8B%E1%85%B5%E1%84%85%E1%85%A1%E1%86%AB%2036bf01fa790e4e1f82b0b1c1f20fead6/Untitled%201.png](1%E1%84%8C%E1%85%A1%E1%86%BC%20Git%E1%84%8B%E1%85%B5%E1%84%85%E1%85%A1%E1%86%AB%2036bf01fa790e4e1f82b0b1c1f20fead6/Untitled%201.png)

- 데이터 보장
git은 데이터 무결성을 보장
check sum (16진수 문자, commit id) → 파일 또는 구성이 완벽하여 버전관리가 명확
- 준비영역 (Staging area)
수정한 영역을 repository에 반영하기 전 검토하는 단계

![1%E1%84%8C%E1%85%A1%E1%86%BC%20Git%E1%84%8B%E1%85%B5%E1%84%85%E1%85%A1%E1%86%AB%2036bf01fa790e4e1f82b0b1c1f20fead6/Untitled%202.png](1%E1%84%8C%E1%85%A1%E1%86%BC%20Git%E1%84%8B%E1%85%B5%E1%84%85%E1%85%A1%E1%86%AB%2036bf01fa790e4e1f82b0b1c1f20fead6/Untitled%202.png)

- 오픈 소스 
소스코드를 공개한 상태에서 인터넷에서 누구나 프로젝트 발전에 기여할 수 있음
git에 장점을 그대로 가져가고 전 세계 프로그래머들이 참여할 수 있음

# Git 설치와 초기 설정

리눅스와 맥은 git이 이미 설치되어 있음.

- 사용자 정보 설정
저장소에 코드를 반영할 때 등록될 사용자 정보를 설정
프로젝트 마다 다른 사용자 정보를 넣으려면 —global 제외

![1%E1%84%8C%E1%85%A1%E1%86%BC%20Git%E1%84%8B%E1%85%B5%E1%84%85%E1%85%A1%E1%86%AB%2036bf01fa790e4e1f82b0b1c1f20fead6/Untitled%203.png](1%E1%84%8C%E1%85%A1%E1%86%BC%20Git%E1%84%8B%E1%85%B5%E1%84%85%E1%85%A1%E1%86%AB%2036bf01fa790e4e1f82b0b1c1f20fead6/Untitled%203.png)

- 설정 정보 확인

![1%E1%84%8C%E1%85%A1%E1%86%BC%20Git%E1%84%8B%E1%85%B5%E1%84%85%E1%85%A1%E1%86%AB%2036bf01fa790e4e1f82b0b1c1f20fead6/Untitled%204.png](1%E1%84%8C%E1%85%A1%E1%86%BC%20Git%E1%84%8B%E1%85%B5%E1%84%85%E1%85%A1%E1%86%AB%2036bf01fa790e4e1f82b0b1c1f20fead6/Untitled%204.png)

# Git 저장소 생성

`Git init`

기존의 디렉토리를 git repository로 설정
e.g. myproject 폴더에서 작업중일 때 myproject 접근해서 git init을 하면 myproject가 git repository가 된다. 

# 기존 디렉토리 사용

Git을 사용할 프로젝트 폴더로 이동 후 아래의 명령어를 실행해주세요.

![1%E1%84%8C%E1%85%A1%E1%86%BC%20Git%E1%84%8B%E1%85%B5%E1%84%85%E1%85%A1%E1%86%AB%2036bf01fa790e4e1f82b0b1c1f20fead6/Untitled%205.png](1%E1%84%8C%E1%85%A1%E1%86%BC%20Git%E1%84%8B%E1%85%B5%E1%84%85%E1%85%A1%E1%86%AB%2036bf01fa790e4e1f82b0b1c1f20fead6/Untitled%205.png)

프로젝트 디렉토리에 `.git` 디렉토리가 생성되며 저장소 생성이 완료되었습니다. 
디렉토리 명을 만드려면 `git init 폴더명`

![1%E1%84%8C%E1%85%A1%E1%86%BC%20Git%E1%84%8B%E1%85%B5%E1%84%85%E1%85%A1%E1%86%AB%2036bf01fa790e4e1f82b0b1c1f20fead6/Untitled%206.png](1%E1%84%8C%E1%85%A1%E1%86%BC%20Git%E1%84%8B%E1%85%B5%E1%84%85%E1%85%A1%E1%86%AB%2036bf01fa790e4e1f82b0b1c1f20fead6/Untitled%206.png)

현재 있는 디렉토리에서 프로젝트 폴더에 git 저장소를 만드려면??

![1%E1%84%8C%E1%85%A1%E1%86%BC%20Git%E1%84%8B%E1%85%B5%E1%84%85%E1%85%A1%E1%86%AB%2036bf01fa790e4e1f82b0b1c1f20fead6/Untitled%207.png](1%E1%84%8C%E1%85%A1%E1%86%BC%20Git%E1%84%8B%E1%85%B5%E1%84%85%E1%85%A1%E1%86%AB%2036bf01fa790e4e1f82b0b1c1f20fead6/Untitled%207.png)
