<h1> Github practice </h1>

<h3> 기본적인 git 연동 </h3>

1. 해당 폴더에 git init (git 저장소로 지정해주기)
2. git add . (스테이지에 올리기)
3. git commit -m "커밋메세지" (git 로컬저장소에 커밋)
4. git remote add <b>origin</b> "깃허브 주소" (원격 저장소와 연동 / origin은 원격 저장소 별명)
5. git push origin master (git에서 원격저장소 origin에 로컬저장소 master을 푸쉬)

- 해당 저장소에 있는 리모트 저장소 정보 보기 : git remote -v

<h3> git clone 해오기 </h3>

1. github에서 repository에서 code를 눌러서 원격저장소 주소를 복사해온다.
2. 프로젝트를 복사할 내 폴더 하나를 지정한다.
3. 폴더에 우클릭 후 git bash here
4. git clone "복사한 원격저장소 주소"
5. 완료 - 기본적으로 origin으로 설정된다.

<h3> git branch 관련 </h3>

1. git branch "브랜치 이름" (브랜치 생성)
2. git branch (잘 생성되었는지 브랜치 목록 확인 / master는 로컬 default 값)
3. git checkout "브랜치 이름" (해당 브랜치로 이동)
4. git branch -D "브랜치 이름" (해당 브랜치 삭제)

<h3> git으로 협업하기 </h3>

1. 내가 작업할 장소에 <b>git clone 원격 저장소 주소</b> (자동으로 download & origin으로 remote 연동)
2. git status나 git checkout master로 현재 상태 확인
3. 내 작업물 commit 하기 전에 <b> 무조건 git checkout 후 git pull origin master</b>로 원격(origin)에서 최신상태를 유지해줄 것.
4. 만약 작업 브랜치를 따로 만들 경우
 - git branch "새 브랜치 이름" (생성) + git checkout "새 브랜치 이름" (이동)  
   git add . -> git commit -m "메세지" -> git push origin "새 브랜치 이름"  
   을 진행하면 원격 저장소에 master 브랜치가 아닌 작업 브랜치로 분리되어 commit된다.  
4-1. 바로 master 브랜치로 올릴거면 git checkout master 후 바로 
 - git add . -> git commit -m "메세지" -> git push origin master 를 진행해준다.

<h4> 무조건 올리기 전에 git pull origin "브랜치" 해주자 </h4>

5. 지금 상황이 원격저장소에 내 작업브랜치에 완료, master 브랜치에는 커밋되지 않은 상태이면
 - git checkout master (브랜치 master로 수정) -> git pull origin "작업 브랜치"  
   master로 브랜치 변경 후에 작업 브랜치 내용을 pull해서 merge해준다.  
   즉, master 브랜치 + 내 작업 브랜치 이므로 이 작업물을 다시 master에 push  
   git push origin master ( master 브랜치에 내 작업브랜치 pull해서 합치고 다시 push)  
 
 6. master브랜치를 push, pull 용도로만 사용하기
 
 <b> 6-1. push 할때 </b>
  - 내 작업 브랜치인 상황에서 git add . -> git commit 해주기 (내 작업 브랜치에 commit)  
    git checkout master -> git merge "내 작업 브랜치" (작업브랜치와 master와 합치기)  
    git push origin master (commit은 작업 브랜치에 / push용으로 master와 합침 후에 원격에 push)  
    즉, 원격 저장소에 push할때 작업 브랜치 + master 브랜치 merge 후 push  
    
 <b> 6-2. pull 할때 </b>
  - 작업중인 파일을 작업 브랜치에 git add . -> git commit 해준다.  
    git checkout master 후 git pull origin master (원격에서 팀원작업물 받아오기)  
    내 작업브랜치에 pull한 작업물 반영하기 위해 git checkout "작업 브랜치" 후 git merge master  
    즉, 작업물 저장하고 원격에서 받아온 후 내 작업브랜치로 가서 master와 merge 해준다.
 
<h4> 팀원과 같은 부분을 작업하면 push나 pull할때 오류가 발생 -> 손수 고쳐주자 </h4>
 
---

<h2> markdown practice </h2>

<h3> 문단 </h3>

---

 1: 첫번째 문단이다.2: 두번째 문단이다.  
 3: 세번째 문단이다.4: 네번째 문단이다.
 
 <h3> 표 </h3>
 
 ---
 
 
 | 값 | 의미 | 기본값 |
|---|:---:|---:|
| `ex1` | meaning | `static` |
| `ex2` | meaning |  |
| `ex3` | meaning |  |
| `ex4` | meaning |  |
