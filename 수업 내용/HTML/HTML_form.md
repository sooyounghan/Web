-----
### form
-----

1. 사용자가 웹 브라우저를 통해 입력된 모든 데이터를 한 번에 웹 서버로 전송하는 양식
2. 전송한 데이터는 웹 서버가 처리, 처리 결과에 따라 다른 웹 페이지를 보여줌
3. 웹에서의 폼은 크게 사용자가 입력하는 부분과 입력한 내용을 서버로 전송하는 버튼 부분으로 나눠짐

<div align = "center">
<img width="308" alt="제목 없음" src="https://github.com/sooyounghan/JAVA/assets/34672301/94e10da8-3428-4978-a70f-a6bec097e9cf">
</div>

4. 사용자가 다양한 정보를 입력하고 서로 전달할 때 사용하는 태그
5. 단독으로 쓰이지 않고, 사용자가 다양한 정보를 입력하는 양식을 포함하는 최상위 태그

<div align = "center">
<img width="306" alt="제목 없음" src="https://github.com/sooyounghan/JAVA/assets/34672301/25c9a004-9e7a-44af-86ac-c9f31ac5569c">
</div>

6. form 태그의 모든 속성은 필수가 아니라 선택적 사용, 속성을 이용해 데이터를 전송할 때 어디로, 어떻게 보낼지 설정
7. name은 중복이 가능하므로, 주로 id를 사용
8. action : 서버 측의 페이지로 전송 
9. method 방식 : get 방식, post 방식 (기본값 : get 방식)

10. autocomplete 속성 : 자동 완성 기능 (기본값 : on)
```html
<form action = "register.html" autocomplete = "off">
</form>
```

-----
### get, post 방식
-----
1. get 방식 : request의 body부분에 담겨서 전송되며, URL에 정보가 담겨서 전송
2. post 방식 : request의 header부분의 body에 담겨서 전송되며, URL 상에 전달한 정보가 표시되지 않음

<div align = "center">
<img width="306" alt="제목 없음" src="https://github.com/sooyounghan/JAVA/assets/34672301/68352951-fe25-471e-8dab-f1f0325bbe8b">
</div>

-----
### input
-----
1. 사용자로부터 입력을 받을 수 있는 입력 필드(input filed)를 정의할 때 사용
2. 사용자가 데이터를 입력할 수 있는 입력 필드를 선언하기 위해 <form> 요소 내부에서 사용

<div align = "center">
<img src="https://github.com/sooyounghan/JAVA/assets/34672301/850696b9-f7b5-431e-85cc-8b507e9137dd">
</div>

         * radio는 단 하나 선택, checkbox는 다중 선택이 가능함

3. checked 속성 : 페이지가 로드될 때 미리 선택될 <input> 요소를 명시 (하나를 선택해야 하는 경우에는 default 값에만 지정)
4. radio나 checkbox는 <> 설정 후 뒤에 그 항목을 표시할 수 있는 이름 표기
   
```html
   <!-- name에 snsYN을 중복 적용을 통해 수신 허용, 불허했는지에 대한 파라미터 값을 얻기 가능 // name은 중복 가능하지만. id는 중복 불가 -->
		<input type = "radio" name = "snsYN" id = "snsY" value = "Y" checked = "checked"> 수신허용
		<input type = "radio" name = "snsYN" id = "snsN" value = "N"> 수신불허
   ```

5. id 속성
    - id 속성은 고유해야하므로 중복 불가하지만, name은 중복이 가능
    - id 속성은 page 안에서 중복으로 사용할 수 없으며, 주로 JavaScript에서 다루기 위해 지정

6. name 속성
    - 입력 양식을 식별하는 이름 (요소를 구별하기 위한 이름)
    - 변수에 대한 이름
  
7. required 속성
<div align = "center">
<img width="306" alt="제목 없음" src="https://github.com/sooyounghan/JAVA/assets/34672301/5bdca2a4-4a3f-49ee-aefd-9c77c7265b82">
</div>

-----
### input type
-----
1. text = "line"

   - 한 줄 짜리 일반 텍스트를 입력하는 필드

       		<input type = "text" [속성 = "속성 값"]>

   - name 속성 : 텍스트 필드를 구별할 수 있도록 이름 부여
   - size : 텍스트 필드의 길이 지정 (즉, 화면에 몇 글자가 보일지 결정)
   - value : 텍스트 필드 요소가 화면에 표시될 때 텍스트 필드 부분에 표시될 내용
   - maxlength : 텍스트 필드에 입력할 수 있는 최대 문자 개수

2. text = "password"

       		<input type = "password" [속성 = "속성 값"]>

   - 비밀번호 입력란이며, value 속성이 없음


3. input type 종류 참조 : https://www.w3schools.com/html/html_form_input_types.asp

4. 시간 관련 속성 예시

   - datetime-local : 날짜와 시간 모두 조절 가능
   - time : 시간만 설정

```html
<fieldset>
	<legend> FieldSet </legend>
	<ul>
		<li> color : <input type = "color" name = "color" id = "color"></li>
		<li> date : <input type = "date" name = "date1" id = "date1"></li>
		<li> datetime-local : <input type = "datetime-local" name = "date2" id = "date2"></li>
		<li> month : <input type = "month" name = "month" id = "month"></li>
		<li> time : <input type = "time" name = "time" id = "time"></li>
		<li> week : <input type = "week" name = "week" id = "week"></li>
	</ul>
</fieldset>
```
<div align = "center">
<img width="758" alt="20240226_122058" src="https://github.com/sooyounghan/Web/assets/34672301/dcb94480-9744-4dd1-be1b-2aebd9ba31b6">
</div>

```html
<!-- %3A는 : 를 의미 -->
http://localhost:8081/webPro/html/ok.jsp?...date1=2024-02-26&date2=2024-02-27T12%3A18&month=2024-07&time=12%3A22&week=2024-W10
```

5. submit, reset
   - reset : < input > 요소에 입력된 모든 정보를 재설정해 초기화 (value 속성을 사용해 버튼에 표시할 기본 내용 설정 가능)
   - submit : 사용자가 폼에 입력한 정보를 서버로 전송 
-----
### input type 종류
-----   
1. hidden (중요)

   - 사용자에게는 보이지 않는 숨겨진 입력 필드를 정의
   - 숨겨진 입력 필드는 렌더링이 끝난 웹 페이지에서는 전혀 보이지 않으며, 페이지 콘텐츠 내에서 그것을 볼 수 있게 만드는 방법도 없음
   - 숨겨진 입력 필드는 폼 제출 시 사용자가 변경해서는 안 되는 데이터를 함께 보낼 때 유용하게 사용
   - 클라이언트에게 노출시키지 않아도 되는 중요 정보이나 개발자에게 반드시 필요한 정보를 사용할 때 사용

```html
<input type = "hidden" name = "이름" value = "서버로 넘길 값">
```

```html
<form method="get">
    아이디 : <input type="text" name="user_id"><br>
    비밀번호 : <input type="password" name="user_pw"><br>
    <%!int game_token = 200;">
    <input type="hidden" id="gameToken" name="game_token" value="<%=game_token%>">
    <input type="submit">
</form>
```
```html
http://172.30.1.37:8081/webPro/html/formEx.jsp?user_id=&user_pw=&game_token=200
```

			URL 주소 쿼리스트링에 hidden_name인 gameToken=200가 전달되어 전송 (데이터를 은밀하게 전송할 수 있음)   

2. number
	- 숫자를 입력할 수 있는 입력 필드를 정의 (쿼리스트링에 의해 문자열 값으로 전달)
	- 스핀 박스로 표시 (스핀 박스 : 입력 창 오른쪽 작은 화살표를 표시해 화살표 클릭에 따라 숫자 증감 가능)
	- max 속성 : < input > 요소의 최댓값을 명시함
	- min 속성 : < input > 요소의 최솟값을 명시함
	- step 속성 : < input > 요소에 입력할 수 있는 숫자들 사이의 간격을 명시함
	- value 속성 : < input > 요소의 초깃값(value)을 명시함
 
```html
<form action="/examples/media/action_target.php" method="get">
    1부터 20까지의 짝수 : <input type="number" name="even" value="1" min="2" max="20" step="2"><br>
    <input type="submit">
</form>
```
<div align = "center">
<img width="182" alt="20240226_140906" src="https://github.com/sooyounghan/Web/assets/34672301/1f886979-bc9d-42bf-8ac5-61637270a561">
</div>    

3. range
	- 슬라이드 막대를 조정하여 범위 내의 숫자를 선택할 수 있는 입력 필드를 정의
	- 기본값 : 0 ~ 100까지이지만, 다음 요소와 함께 사용하면 그 범위 설정 가능 (기본 범위에서 벗어날 수 있음)
	- max 속성 : < input > 요소의 최댓값을 명시함
	- min 속성 : < input > 요소의 최솟값을 명시함
	- step 속성 : < input > 요소에 입력할 수 있는 숫자들 사이의 간격을 명시함
	- value 속성 : < input > 요소의 초깃값(value)을 명시함

```html
<form oninput="x.value=parseInt(a.value)" action="/examples/media/action_target.php" method="get">
    여러분의 나이대를 골라보세요.<br>
    Age : 0<input type="range" id="age" name="age" min="0" max="60" step="10" value = "10">60
    <output name="x" for="a"></output><br>
    <input type="submit">
</form>
```
- 기본값은 0, 최저값은 10, 최댓값은 60, 간격은 10으로 설정
- 범위 양끝단에 최저값과 최고값을 표기하면, 그 범위를 알 수 있음

<div align = "center">
<img width="179" alt="20240226_141917" src="https://github.com/sooyounghan/Web/assets/34672301/1348ba3e-e25a-4269-8a14-5da7d3dde1a0">
</div>   

4. radio, checkbox
	- radio : 두 개 이상의 선택 중 하나만 선택할 때 사용
	- checkbox : 두 개 이상 여러 가지를 선택해도 될 경우 사용
	- name 속성 : 서버 폼 프로그램에서 라디오 버튼이나 체크박스를 구분하기 위해 이름 지정
	- value 속성 : 선택한 라디오 버튼이나 체크박스를 서버로 알려줄 때 넘길 값 지정
	- checked 속성 : 처음 아무것도 선택되지 않은 상태로 화면에 표시, 기본으로 선택해놓은 항목이 있어야 한다면 사용

5. color
	- 색상표에서 사용자가 색상을 선택할 수 있도록 제공

```html
<li> color : <input type = "color" name = "color" id = "color"></li>
```
```html
http://localhost:8081/webPro/html/ok.jsp?...&color=%23000000
```

	 %23 : #
  	 00 / 00 / 00 : RGB 값 의미


-----
### input type : 분화된 텍스트 필드
-----   
1. search

	  - 검색어를 입력할 수 있는 텍스트 필드를 정의
	  - 검색 필드는 텍스트 필드와 기능적으로는 완전히 똑같지만, 브라우저에 의해 다르게 표현 가능
	  - 반드시 name 속성을 설정해야 하며, name 속성이 설정되어 있지 않으면 서버로 제출되지 않음
	  - placeholder 속성 : 사용자가 적절한 값을 입력할 수 있도록 도와주는 짧은 도움말을 명시

```html
<input type = "search">
<input type = "submit" value = "검색">
```

```html
<form action="/examples/media/action_target.php" method="get">
    검색 <input type="search" name="search" placeholder = "검색어를 입력하세요.">
    <input type="submit">
</form>
```

2. url

 	- 웹 주소도 텍스트 필드로 type으로 별도 지정 가능, URL 입력란 만들기
 	- 반드시 http://로 시작하는 사이트 주소를 입력

3. e-mal

 	- 메일 주소 입력란 만들기

4. tel

	 - 전화번호 입력란 만들기

< email, tel, url 속성은 DB와 연동하여 유효성 검사 필요 >
```html
<fieldset> <!-- 유효성 검사 필요 -->
	<legend> FieldSet </legend>
		<ul>
			<li> E-mail : <input type = "email" name = "email" id = "email"></li>
			<li> tel : <input type = "tel" name = "tel" id = "tel"></li>
			<li> URL : <input type = "url" name = "url" id = "url"></li>
		</ul>
</fieldset>
```

<div align = "center">
<img width="744" alt="20240226_123738" src="https://github.com/sooyounghan/Web/assets/34672301/9a136e3e-6af1-4c16-8cd6-2d58cb876d22">
</div>

5. image
	- webapp/imgs에 저장
	- 제출 버튼(submit button)으로 사용될 이미지를 정의
	- 텍스트가 아닌 이미지 형태로 된 제출 버튼을 생성하며, 이때 해당 이미지의 경로는 src 속성에 명시
	- 강제 크기 조정 가능
  
< img src 형태 (순수 image) >
```html
<img src="http://localhost:8081/webPro/imgs/submit-button.gif" alt="submit" title="submit image" style="width:300px;height:100px">
```
	img의 src는 절대경로 또는 상대경로 가능 (절대경로는 위와 같이 명시해야함) / title은 그 image의 이름 / style 속성으로 너비, 크기 조정  

 < input type 형태 (submit 가능) >
 ```html
<input type = "image" src="<%=request.getContextPath()%>/imgs/submit-button.gif" style="width:300px;height:100px">
```
	 img src와 동일하지만, 제출 기능이 추가적으로 존재하며, 상대경로로 표시  

<div align = "center">
<img width="338" alt="20240226_154130" src="https://github.com/sooyounghan/Web/assets/34672301/7d3b35f9-df7b-4993-bc25-3b6120cbc05c">
</div>   

- css 선택자(Collector) 이용
```html
<head>
<meta charset="UTF-8">
	<title> Form Example </title>
	<style>
	/* CSS 주석문 */
	/* Selector (선택자) : { css속성:값;css속성:값;..css속성:값; } */
	/* 선택자에는 tag, .클래스명, #id명 가능 */
	/* img { width:300px;height:200px; } img 태그를 선택해 너비를 100으로 일괄 적용 */
	.c1 { width:200px;height:100px; } /* 클래스 c1인 요소에 대해 너비(width)와 높이(height)에 일괄 적용하겠다는 의미며, 여기에서는 이미지에 대해 submit 역할을 하는 input 요소에 대해 조정 */
	</style>
</head>
```
```html
<img src="http://localhost:8081/webPro/imgs/submit-button.gif" alt="submit" title="submit image" class = "c1">
<input type = "image" src="<%=request.getContextPath()%>/imgs/submit-button.gif" class = "c1">
```

6. file
    
	- 파일이 전송되는 것이 아니라 파일명에 대한 문자열이 전송
 	- 문자열 데이터를 받아서 클라이언트에게 속한 파일을 복사해 서버에 저장 (복사본 저장) : 인코딩 설정을 다르게 해야함

		   * File 업로드 기능 구현 시 form 태그의 method 방식은 post 방식, enctype = "multipart/form-data" 속성 값 설정
    
<div align = "center">
<img width="148" alt="20240226_124413" src="https://github.com/sooyounghan/Web/assets/34672301/43c1d257-d388-40b3-9e33-4fca49bccda0">
</div>  

```html
http://localhost:8081/webPro/html/ok.jsp?...file=1.txt&tel=&url= <!-- 1.txt 파일명이 문자열로 전송 -->
```

7. button
	- 단순한 푸시 버튼으로 렌더링 (폼 안에 버튼 형태를 만듬)
	- submit이나 reset 같은 자체 기능이 없이 오직 버튼만 넣기 때문에 스크립트 함수 등을 연결해 사용
	- value 속성을 통해 버튼에 표시할 내용 지정
	- 이벤트 처리기 (주로 Click 이벤트)를 부착하여, 클릭 버튼 가능

```html
<!-- button 모양 추가하되, 이름은 click이고, onclick 기능으로 누르면 창이 뜨는데, 그 메세지가 안녕 출력 -->
<input type = "button" value = "click" onclick = "alert('안녕');">
```
	- javaScript : onclick 이벤트는 버튼을 클릭했을 때 특정 기능을 수행하게 해줌
 	- javaScript : alert('표시내용') : alert창 (메세지 창)을 띄우되, 표시내용을 담은 창을 띄움

<div align = "center">
<img width="411" alt="20240226_161456" src="https://github.com/sooyounghan/Web/assets/34672301/ea119ed1-40fd-45bc-bf84-43c81de724a5">
</div>   

-----
### input 태그의 다양한 속성
-----   
1. autofocus 속성
	- 입력 커서를 표시하는 기능
	- 페이지를 불러오자마자 폼의 요소 중에서 원하는 요소에 마우스 커서 표시 가능

```html
<input type = "text" id = "name" autofocus required>
```

2. readonly 속성
   	- 읽기 전용 필드 만들기
   	- 사용자에게 내용을 보여주기만 하고 입력은 받을 수 없음
   	- true, false 값 중 하나만 사용

```html
<input type = "text" id = "subj" value = "오전 9시 ~ 11시" readonly>
```

3. required 속성
   	- 필수 필드에 필요한 내용에 부여하여 필수 필드로 설정 가능
   	- required = "required"

4. placeholder 속성
	- 사용자가 텍스트를 입력할 때 도움이 되도록 입력란에 적당한 힌트 내용을 표시
	- 그 필드를 클릭하면 내용이 사라지도록 함
