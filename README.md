# HTML
## HTML 구조태그
* HTML은 **웹문서를** 뜻한다.
* `태그`웹문서에 들어가는 내용~제목 모든 요소는 `<태그>`로 묶여서 만들어진다.
## HTML 주의사항
* 파일명.html
* 모든 파일명, 폴더명은 영문 소문자 사용, 특수문자 금지, 공백 금지, 한글 금지, 숫자 앞 금지
* start.html = O
* start1.html = O
* 1start.html = X (숫자앞)
* basic start.html = X (공백)
* basic_start.html = O (허용 특수문자 _ -)
* basic%start.html = X (허용 외 특수문자)
* 시작.html = X (한글)
## VSC 단축키
* 화면 분할(좌우) : `ctrl+\`
* 화면 분할(상하) : `ctrl+k` - > `ctrl+\`
* 바꾸기/찾기 : 바꾸고 싶은 글자 선택하고 -> `ctrl + H`
* 커서 위치 기준 한 줄 복제 : `shift + alt + ↑↓` (블록상태로도 복제 가능)
* 커서 위치 기준 라인이동 : `Alt + ↑↓`
* 들여쓰기 제거/추가 : `Ctrl + [/]`
* 다른 이름으로 저장 : `Ctrl + Shift + s`
## HTML 단축키
* `html:5` Tab키 : 구조태그 생성
* 한 줄 주석 : `ctrl + /`
* 블록 주석 " `shift + alt + a`
## title 올바른 작성법
* **제작페이지가 메인일경우 : 사이트명**
* **제작페이지가 서브일경우 : 서브명 | 사이트명**
* 서브명 | 경로 | 사이트명
* 서브명-정보 | 경로 | 사이트명
* 채식주의자-한강 | 국내소설 | 교보문고
* 소년이온다-한강 | 국내소설 | 교보문고(띄어쓰기 안 해도 ㄱㅊ)
* 소년이 온다-한강-창비 | 국내소설 | 교보문고
## 태그속성 class, id
### class
* `<태그 class="값"></태그>`
* 2번 이상 반복하는 이름인 경우
* 예) lnb, snb, container 등
### id
* `<태그 id="값"></태그>`
* 반복하면 안되는 단독 명칭인 경우
* 예) header, gnb, footer 등
## HTML 기초 문서 태그
* 블록태그 : w100% 기본, 새로운 행, 크기가 큼
* 인라인태그 : 열(옆으로 나열), 크기는 내용만큼 인식
### 제목
* `h1~h6` : 블록태그, h1대제목, h6소제목(가장작은), h레벨이 높을수록(1~3) 검색어로 인식될 확률 높음, SEO마케팅 목적
### 내용
* `p` : 블록, 한줄~여러줄 단락형태의 내용일 때
* `br` : 인라인, 줄바꿈할 때 사용
* `em` : 인라인, 단순 문맥 강조, 주로 p 자식으로 사용
* `strong` : 인라인, 중요+심각성 강조, p자식위주
* `sub` : 인라인, 아래첨자(거의 안 씀)
* `sup` : 인라인, 위첨자(거의 안 씀)
* `s`/`del` : 인라인, 교체, 삭제 텍스트(취소선)
* `blockquote` : 블록, 긴 인용문
* `q` : 인라인, 짧은 인용문
* `code` : 인라인, 컴퓨터 명령어를 화면에 표시할 때
* `address` : 블록, **footer 안** 연락처·주소 등,(해당 서비스 주소만 포함.해당 사이트-내 주소), address 안 블록 사용 주의(유효성에러)
### 레이아웃
* `div` : 블록, 그룹, 자식이 2개 이상이며 같은 방향일 때, 블록과 인라인을 자식으로 모두 가질 수 있음
* `span` : 인라인, 그룹(위 div와 같음), 보조(디자인), 인라인만 자식으로 가질 수 있음
* `hr` : 블록, 경계구분용(디자인 테두리 용도 아님)

### 특수문자 태그
* `&;` : 특수문자 시작=& 끝=;
* `&copy;` | footer 저작권마크 ⓒ (제일 자주 씀)
* `&lt;` | <
* `&gt;` | >
* `&amp;` | &
## 링크태그
* `a` : 블록,인라인 둘 다 가능.(내용 취급)하나의 페이지에서 다른 페이지를 연결할 때 사용하는 하이퍼링크를 정의. (필수)`href`와 함께 사용.
* 필수구조 : `<a href="주소>글자</a>`
* 링크 새 창 열기 속성 : `<a target="_blank">클릭대상</a>`
<!-- <a href="링크" target="_blank">내용</a> -->
<!-- #top :: 아이디로 인식 / # 임시태그로 인식 -->
### 링크태그 href 주소 작성법
* 절대경로 : `href="http://주소"` | 실제 서비스되는 웹주소
* 상대주소 : `href="./폴더 및 파일"` 같은 위치 또는 하위 경로
* 상대주소 : `href="../폴더 및 파일"` 상위 위치
### 바로가기링크`a`(스크롤 이동-특정 위치로)
1. 링크 클릭 시 이동하고 싶은 위치의 태그에 `id="위치명"` 입력하기 | 예) `<body id="top"></body>`
2. `a`태그에 2번 id(#) 연결 | 예) `<a href="#top"></a>` - **(#필수)**
## 이미지(img) - 인라인(inline)
* `img` = 인라인.src 이미지 경로 속성 값으로 상대경로 방식으로 작성(닫기태그 없음) | `<img src="이미지경로" alt="대체텍스트>`
* 대체텍스트 alt 속성 필수 작성 | 예) `img src="./search.png" alt="검색"` | 이미지 내 정보 대체텍스트로 작성
### 이미지 필수 속성
* `src` : 이미지 경로(**상대**/절대경로)
* `alt` : 대체텍스트( alt="의미가 있는 경우" | alt="" 의미가 없는 경우)
### 이미지 선택 속성
* `class` | `id` (이미지 외 모든 태그 동일)
## background-image (CSS 배경이미지)
### `img` 태그가 아닌 background-image로 처리하는 경우
* 형제, 자식, 자손 요소와 겹쳐져서 디자인 된 경우
* 쇼핑몰 상품 썸네일, 히어로 배너, 광고배너 등 활용
### 태그-배경이미지 적용 작성순서
1. `<태그 style="">`
2. `<태그 style="background-image:;">`
3. `<태그 style="background-image:url(경로);">`
## 파비콘(favicion)
* 웹브라우저 제목표시줄(탭) 앞 사이트 구분 아이콘(필수요소)
* head 안에 작성 | link:favicion > href 링크부분에 이미지로 경로 변경 `link rel="#" href="#" type="image/x-icon"`
* 사이즈가 다 다를 땐 가장 큰 이미지로 진행
* web > 16x16 | 32x32 | 96x96
* apple > 57x57 | 180x180
* android > 192x192
## 비디오(video)태그 - 블록(block)
### 로컬 환경에 동영상 파일이 있는 경우 연결방법
* `<video></video>`
* `<video src="상대경로"></video>`
### 동영상 관련 속성
* `<video src="상대주소" autoplay muted loop controls></vidoe>`
* 자동재생 : autoplay | 음소거 : muted | 반복재생 : loop | 재생바 : controls
### 유튜브 영상
* 원하는 영상 재생 > 우클릭(소스코드복사)
### 유튜브 영상 속성
* `<iframe src="http://www.youtube.com/embed/동영상이름">`
* `<iframe src="http://www.youtube.com/embed/동영상이름?속성=값&속성=값">`
<!-- 예) `<iframe src="http://www.~embed/wEThWSF31?autoplay=1&mute=1&loop=1&playlist=wEThWSF31">` -->
### 유튜브 영상 속성 종류
* `autoplay=1` : 재생함 | 재생안함(0)
* `mute=1` : 음소거함 | 음소거안함(0)
* `loop=1` : 반복재생함 | 반복재생안함(0)
* `playlist=동영상이름` : loop=1일 경우 함께 사용
* `controls=0` : 재생바숨김 , 재생바보임(1)>이 경우 굳이 안 써도 됨
## 목록태그 + 레이아웃
* 2개 이상의 목록(li)를 묶어주는 그룹 태그(ol,ul)
### 비순차 ul + li
* 목록li에 순서가 없는 경우(비순차) : ul 그룹 태그 사용 | `<ul><li></li></ul>`
* ul의 자식은 li만 올 수 있다. 자손은 모두 가능
### 순차 ol + li
* 목록li에 순서가 있는 경우 : ol 그룹 태그 사용 | `<ol><li></li></ol>`
## 비순차목록
* `dl` 그룹 | `dt` 제목 | `dd` 내용
* `dt-dd` 는 h4~h6 정도로 구성된 제목과 내용이 연속적으로 2개 이상 구성되어 있을 경우 사용한다.
* `dl`의 자식은 `dt`, `dd`만 올 수 있음.
* `dt-dd` 형제는 `dt-dd`만 가능함. (dd가 dt의 앞에 올 수 없음)
* `<dl>[<dt></dt><dd></dd>][<dt></dt><dd></dd>]</dl>` (ㅇ) | `<dl><dd></dd><dt></dt>` (x) 
## form 폼 태그
* 사용자로부터 입력 받을 수 있는 폼을 정의
### `<form action="#" method="#"></form>`
* action : 사용자가 입력 또는 선택한 정보를 전송하는 주소 | 폼 데이터를 제출할 서버 스크립트
    * 예) 네이버 로그인 중이라면 아이디, 비밀번호를 네이버 서버(=action)로 전송해서 유효성 체크
* method : action에 정보를 전송할 때 어떤 방식으로 전송할 것인지 결정하는 방식 **get, post**
    * post : http 본문에 포함하여 서버 전송 | 입력정보 비공개 | 예시) 로그인 할 때 | **보안 높음**
    * get : 폼 데이터 url 추가하여 서버 전송 | 주소창에 입력정보 공개 | 예시) 검색했을 때 | **보안 낮음**
### form action
* 입력정보
* 선택정보
* 결정버튼
### fieldset
* 양식의 일부를 그룹화. legend 그룹 제목 필수 포함.
<!-- <form action="#" method="get">
    <fieldset>
        <legend>연습그룹</legend>
    </fieldset>
</form> -->
### `<input>` 입력 및 선택양식(inline)
* 사용자의 입력 및 선택 양식 담을 때 사용
* 입력 및 선택 구분을 위해 type속성을 연결하여 컨트롤 양식 활용
* `<input type="" name="" value="" id="" class="">`
* type : 용도에 따른 종류 선택|입력 필드의 종류 (ex : 비번=password)
* name 
    * 입력양식(text, password 등) : 서버 전송 시 데이터 구분을 위한 개별이름(데이터 구분)
    * 선택양식(select, checkbox, radio) : 선택 요소 2개 이상을 묶는 그룹명
* value
    * 입력양식 :input 요소의 처음부터 입력되어있는 초기값 (ex 수량 1)(필요할 때만 사용)
    * 선택양식 : 데이터 구분용(name 의미동일)
* id : css or js 데이터 구분명(name 동일설정가능)
* class : 반복 디자인 사용 시 설정하는 반복이름
`<input type="text" placeholder="한줄 입력"><br>`
`<input type="password" placeholder="입력 보안"><br>`
`<input type="tel" placeholder="전화번호"><br>`
`<input type="url" placeholder="주소"><br>`
`<input type="email" placeholder="이메일"><br>`
`<input type="number" placeholder="숫자"><br>`
`<input type="search" placeholder="검색어"><br>`
`<input type="time"><br> <!-- 시간입력 html5 -->`
`<input type="week"><br> <!-- 날짜입력(시간x) html5 -->`
`<input type="hidden"><br> <!-- 서버로 전송되는 숨김영역의 값 -->`
`<input type="checkbox"><input type="checkbox"> 선택양식<br> <!-- 다중선택 -->`
`<input type="radio"><input type="radio"> 선택양식<br> <!-- 단일선택 -->`
`<textarea>여러 줄 입력</textarea>`
* label : 입력,선택 시 for="id" 연결로 선택영역 늘릴 수 있음
* select-option : select 선택박스 > option 선택박스 값
`<select name="(그룹명)" id="(css,js 용)"><option value="(서버 전송값)"></option></select>`
* input 내 value = 초기값 | min = 입력 가능한 최소값 | max = 입력 가능한 최대값 입력 가능
* `autofocus` : 페이지 접속 시 바로 커서 위치 **활성화**
### button
* `<a>` : 단순 페이지 이동(조건x)
* `<button>` : 페이지 이동(조건부)
    * 로그인 성공 -> 메인이동 | 로그인 실패 -> 이동x
* `<button type="종류"></button>`
* name, value 속성 사용 안 함 | 'id+class'는 필요에 따라 사용
* button
    * submit, reset을 제외한 모든 범용적 기능
    * 사용자의 입력(input), 선택(select, checkbox, radio) 요소가 없는 경우 단순 버튼의 기능만 활용할 때 form 없이 버튼만 사용할 수 있음(이전, 다음, 재생, 일시정지 등)
    * 페이지 내에서 이전/다음 이동, 재생, 일시정지, 정지 등 다양한 기능 활용
    * 서버 전송이 아닌 조건에 따른 다른 창 띄우기(우편번호찾기, 본인인증 등)
    * 버튼 클릭 시 타 페이지로 넘어가게 할 때: `onclick="window.location.href='페이지경로'"` 
* submit
    * form action, method 방식 서버에 전송하는 데이터
    * (예) 아이디, 비번 입력 후 서버 전송해서 유효성 검사
    * (예) 상품을 장바구니(서버)에 담기
    * (예) 장바구니에 담은 상품을 구입해서 내 구입목록(서버)에 저장하기
* reset
    * 기존 데이터를 현재 페이지에서 제거, 취소할 경우