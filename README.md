# mini-project
비트캠프 2차 미니 프로젝트 


## 프로젝트 기간
- 준비: 2020년 10월 22일
- 발표: 2020년 10월 23일


## 참여자
- 김태희: https://github.com/TaeheeKim15
- 유지연: https://github.com/jiyounyou


## 주제
- 결혼정보회사 회원 관리 시스템


## 프로그램 사용 대상
- 결혼을 꿈꾸는 20 - 40대 남성과 여성


## 구현 방식
- 서버와 클라이언트 App을 각각 만든다. (ServerApp & ClientApp)
- 서버와 클라이언트는 stateless 방식으로 통신한다.
- Create(생성), Read(읽기), Update(갱신), Delete(삭제)를 구현한다.
- 입력된 정보는 json형식의 파일로 저장하고 읽어들인다.


## 기능
### 회원 등록
  - 새로운 회원 정보를 저장한다.
  - 아이디, 비밀번호, 이름, 성별, 나이, 전화번호, 취미, 성격
    (id, password, name, gender, age, tel, hobby, personal)
  - 아이디는 중복해서 저장하지 않도록 기능 구현한다.

### 전체 회원 조회
  - 저장된 모든 회원을 조회한다.

### 여성 회원
  - 저장된 회원 중 여성 회원의 정보를 조회한다.
  - 회원 정보는 남녀 구분 없이 저장되어 있기 때문에 성별 저장 정보에 필터를 적용하여 여성 정보만 출력한다.

### 남성 회원
  - 저장된 회원 중 남성 회원의 정보를 조회한다.
  - 회원 정보는 남녀 구분 없이 저장되어 있기 때문에 성별 저장 정보에 필터를 적용하여 남성 정보만 출력한다.

### 회원 상세 보기
  - 저장된 회원 중 한 명의 이름을 입력해서 그 회원의 상세 정보를 조회한다.
  - 성별, 나이, 취미, 성격를 출력한다.
    
### 회원 탈퇴
  - 저장된 정보에서 특정 회원의 정보를 삭제한다.
  - 회원 탈퇴를 시도하면, 아이디를 입력받고 그 아이디로 저장된 정보가 있는지 조회한다.
    또한 비밀번호를 입력해야 하는데, 아이디에 등록된 비밀번호와 일치해야 회원 탈퇴가 가능하다.

### 회원 매칭
  - 좋아하는 이성의 성격을 선택하여 걸맞는 상대 정보를 제공한다.
  - 자신의 성별을 선택하면, 반대 성별의 회원 정보를 제공한다.


### 디폴트 회원 리스트
- 아래 json 형식의 데이터를 사용 (여성 회원 9명, 남성 회원 7명)
[{"id":"kimth","password":"1111","name":"김태희","gender":1,"age":30,"tel":"010-1111-1111","hobby":"피규어 수집","personal":1},{"id":"youjy","password":"1111","name":"유지연","gender":1,"age":33,"tel":"010-2222-2222","hobby":"맛집 탐방","personal":2},{"id":"eomjh","password":"1111","name":"엄정화","gender":1,"age":25,"tel":"010-3333-3333","hobby":"퍼즐맞추기","personal":3},{"id":"jeonjh","password":"1111","name":"전지현","gender":1,"age":40,"tel":"010-4444-4444","hobby":"돈까스먹기","personal":4},{"id":"junghh","password":"1111","name":"정현희","gender":1,"age":34,"tel":"010-5555-5555","hobby":"요리","personal":5},{"id":"iu","password":"1111","name":"아이유","gender":1,"age":24,"tel":"010-6666-6666","hobby":"불우이웃돕기","personal":6},{"id":"baedn","password":"1111","name":"배두나","gender":1,"age":37,"tel":"010-7777-7777","hobby":"범인검거","personal":7},{"id":"jessica","password":"1111","name":"제시카","gender":1,"age":37,"tel":"010-8888-8888","hobby":"음주","personal":8},{"id":"leehr","password":"1111","name":"이효리","gender":1,"age":40,"tel":"010-9999-9999","hobby":"댄스파티","personal":9},{"id":"mapodaegyo","password":"2222","name":"곽철용","gender":2,"age":56,"tel":"010-7465-8997","hobby":"화투","personal":1},{"id":"dooli","password":"2222","name":"둘리","gender":2,"age":156,"tel":"010-5641-8907","hobby":"초능력","personal":2},{"id":"bit84","password":"2222","name":"김기안","gender":2,"age":45,"tel":"010-7156-5913","hobby":"그림그리기","personal":3},{"id":"ssal","password":"2222","name":"최농부","gender":2,"age":35,"tel":"010-3613-1504","hobby":"벌초","personal":4},{"id":"bjkim","password":"2222","name":"중도서관","gender":2,"age":28,"tel":"010-9623-1595","hobby":"게임","personal":5},{"id":"stealer","password":"2222","name":"도둑임","gender":2,"age":36,"tel":"010-9643-0388","hobby":"소매치기","personal":6},{"id":"gag","password":"2222","name":"박명수","gender":2,"age":47,"tel":"010-7460-7797","hobby":"만담","personal":7}]


## 실행 화면 예시
### 클라이언트 접속시 노출 화면
<pre>
            ♥ Finding your love... ♥
            ╱▔▔╲╱▔▔╲┊┊╭━━━━━━━━━━━━
            ▏┈╭╮╭╮┈▕┊┊┃ Finding
            ╲┈┏━━┓┈╱┊╭┫ your Love♥
            ┊╲╰━━╯╱━━╯╰━━━━━━━━━━━━
            ┊┊╲┈┈╱┊┊┊┊┊┊┊┊  ♥    ♥
            ┊┊┊╲╱┊┊┊┊┊┊┊┊┊♥    ♥   ♥

        ♥ 원하는 번호를 입력하세요! ♥  (예: 1)
 ------------------------------------------------------
 (1) 회원 등록       (2) 전체 회원 조회 
 (3) 여성회원 조회   (4) 남성회원 조회 
 (5) 회원 상세 보기  (6) 회원 탈퇴  
 (7) 회원 매칭       (0) 나가기           (99) 종료
 ------------------------------------------------------
</pre>

### 회원 정보 등록 예시
<pre>
명령> 1
[회원 등록]
★ 입력하신 정보는 변경할 수 없습니다.
★ 신중하게 입력하시길 바랍니다.
● 아이디? 
hollys
● 비밀번호? 
123
● 이름? 
hollys
● 성별?
  1: 여자
  2: 남자
>
1
● 나이? 
123
● 전화번호? 
123
● 취미? 
123
● 회원님의 성격 유형을 입력해주세요. (택 1)
(1) 다정한 (2) 자신감 넘치는 (3) 성실한
(4) 꼼꼼한 (5) 외향적인 (6) 내성적인
(7) 자상한 (8) 끈기있는 (9) 낙천적인
> 
4
</pre>

### 전체 회원 조회
<pre>
명령> 2
[전체 회원 목록]
김태희님 (30세, 여성), 피규어 수집을/를 즐깁니다.
유지연님 (33세, 여성), 맛집 탐방을/를 즐깁니다.
엄정화님 (25세, 여성), 퍼즐맞추기을/를 즐깁니다.
전지현님 (40세, 여성), 돈까스먹기을/를 즐깁니다.
정현희님 (34세, 여성), 요리을/를 즐깁니다.
아이유님 (24세, 여성), 불우이웃돕기을/를 즐깁니다.
배두나님 (37세, 여성), 범인검거을/를 즐깁니다.
제시카님 (37세, 여성), 음주을/를 즐깁니다.
이효리님 (40세, 여성), 댄스파티을/를 즐깁니다.
곽철용님 (56세, 남성), 화투을/를 즐깁니다.
둘리님 (156세, 남성), 초능력을/를 즐깁니다.
김기안님 (45세, 남성), 그림그리기을/를 즐깁니다.
최농부님 (35세, 남성), 벌초을/를 즐깁니다.
중도서관님 (28세, 남성), 게임을/를 즐깁니다.
도둑임님 (36세, 남성), 소매치기을/를 즐깁니다.
박명수님 (47세, 남성), 만담을/를 즐깁니다.
hollys님 (123세, 여성), 말타기을/를 즐깁니다.
</pre>

### 여성 회원 목록 조회
<pre>
명령> 3
[여성 회원 목록]
김태희(30세), 피규어 수집을/를 즐깁니다.
유지연(33세), 맛집 탐방을/를 즐깁니다.
엄정화(25세), 퍼즐맞추기을/를 즐깁니다.
전지현(40세), 돈까스먹기을/를 즐깁니다.
정현희(34세), 요리을/를 즐깁니다.
아이유(24세), 불우이웃돕기을/를 즐깁니다.
배두나(37세), 범인검거을/를 즐깁니다.
제시카(37세), 음주을/를 즐깁니다.
이효리(40세), 댄스파티을/를 즐깁니다.
</pre>

### 남성 회원 목록 조회
<pre>
명령> 4
[남성 회원 목록]
곽철용(56세), 화투을/를 즐깁니다.
둘리(156세), 초능력을/를 즐깁니다.
김기안(45세), 그림그리기을/를 즐깁니다.
최농부(35세), 벌초을/를 즐깁니다.
중도서관(28세), 게임을/를 즐깁니다.
도둑임(36세), 소매치기을/를 즐깁니다.
박명수(47세), 만담을/를 즐깁니다.
</pre>

### 회원 상세 보기 예시

<pre>

명령> 5
[회원 상세보기]
이름? 
둘리
♥ 둘리님의 정보는 아래와 같습니다.
-----------------------------------
성별: 남성
나이: 156세
취미: 초능력
성격: 자신감 넘치는 성격
-----------------------------------
♥ 둘리님의 연락처가 궁금하신가요?
♥ 프리미엄 서비스에 가입하세요!
</pre>

### 회원 탈퇴 예시1
<pre>
명령> 6
[회원 탈퇴]
● 탈퇴하려는 아이디를 입력하세요. > 
youjy
정말 삭제하시겠습니까?(y/N) 
y
● 비밀번호를 입력하세요. >
1111
비밀번호가 일치하지 않습니다.
</pre>

### 회원 탈퇴 예시2
<pre>
명령> 6
[회원 탈퇴]
● 탈퇴하려는 아이디를 입력하세요. > 
hollys
정말 삭제하시겠습니까?(y/N) 
y 
● 비밀번호를 입력하세요. >
123
회원 탈퇴가 완료되었습니다.
♥ Finding your love... ♥ 를 이용해주셔서 감사합니다.
                               

     ,;;;;;;\     ,;;;;;;,
   ,;;;@@@@@/   /;;@@@@@;;;,
  ,;;;@@,;;;\   \,@,;;;,@@;;;,
  ;;;@@;;;' '\   \;' ';;;@@;;;
  ;;;@@;;;   /   /    ;;;@@;;;
   ;;;@@';;, \   \  ,;;'@@;;;
    ';;;@@';;,\   \;;'@@;;;'
      ';;;@@';/   /'@@;;;'
        ';;;@/   /@@;;;' see you later!
          ';/   /;@;;'   bye.....♥
                \;'
</pre>

### 회원 매칭 예시
<pre>
명령> 7
[회원님 맞춤 이성 목록]
● 회원님의 성별을 입력해주세요
  1: 여자
  2: 남자
>
1
● 회원님이 원하시는 이성의 성격 유형을 입력해주세요. (택 1)
(1) 다정한 (2) 자신감 넘치는 (3)성실한
(4) 꼼꼼한 (5) 외향적인 (6) 내성적인
(7) 자상한 (8) 끈기있는 (9) 낙천적인
> 
5
♥ 외향적인 이성분들은 아래와 같습니다.
-----------------------------------
<< 중도서관 회원님 >>
나이 : 28세
게임 를(을) 즐기는 회원
-----------------------------------
♥ 중도서관님의 연락처가 궁금하신가요?
♥ 프리미엄 서비스에 가입하세요!
</pre>

### 나가기 예시
<pre>
명령> 0
다음에 또 만나요!

 _                
| |               
| |__  _   _  ___ 
| '_ \| | | |/ _ \
| |_) | |_| |  __/
|_.__/ \__, |\___|
        __/ |     
       |___/    
</pre>


## 사용한 Ascii Art
### 접속 화면
<pre>
╱▔▔╲╱▔▔╲┊┊╭━━━━━━━━━━━━
▏┈╭╮╭╮┈▕┊┊┃ Finding
╲┈┏━━┓┈╱┊╭┫ your Love♥
┊╲╰━━╯╱━━╯╰━━━━━━━━━━━━
┊┊╲┈┈╱┊┊┊┊┊┊┊┊  ♥    ♥
┊┊┊╲╱┊┊┊┊┊┊┊┊┊♥    ♥   ♥
</pre>

### 끝내기 화면
<pre>
 _                
| |               
| |__  _   _  ___ 
| '_ \| | | |/ _ \
| |_) | |_| |  __/
|_.__/ \__, |\___|
        __/ |     
       |___/   
</pre>

### 회원 탈퇴 화면
<pre>
     ,;;;;;;\     ,;;;;;;,
   ,;;;@@@@@/   /;;@@@@@;;;,
  ,;;;@@,;;;\   \,@,;;;,@@;;;,
  ;;;@@;;;' '\   \;' ';;;@@;;;
  ;;;@@;;;   /   /    ;;;@@;;;
   ;;;@@';;, \   \  ,;;'@@;;;
    ';;;@@';;,\   \;;'@@;;;'
      ';;;@@';/   /'@@;;;'
        ';;;@/   /@@;;;' see you later!
          ';/   /;@;;'   bye.....♥
                \;'
</pre>
