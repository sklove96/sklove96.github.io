---

layout: posts

title: "[Java] HTML 기본요소"

date: 2020-07-21

categories: [Java]

---
### HTML

- - -
 <br>
#### HTML이란?
<blockQuote>HTML(Hypertext Markup Language)란 우리가 보는 웹페이지가
어떠한 구조를 가지고 있는지 브라우저로 하여금 알 수 있도록 하는 마크업 언어.
</blockQuote>
<br>
- - -
#### HTML 기본 요소
<br>
- 주석문 : `ctrl`+`shift`+`/`
<br>
- 줄 바꿈: `<br />`
<br>
- 글자 태그: `<h1></h1>`~`<h6></h6>`
<br>
- 단락 나누기: `<p></p>`
<br>
- 앵커 태그: 서로 다른 웹페이지 사이 이동, 웹페이지 내부에서 특정 위치로 이동
~~~java
<a href="https://www.naver.com"> 네이버 </a>
~~~
<br>
- 페이지 내부에서 특정 위치로 이동
: 아이디를 각각 alpha, beta, gamma라고 지정하였을 때
~~~
<a href="#alpha">Move to Alpha</a>
<a href="#beta">Move to Beta</a>
<a href="#gamma">Move to Gamma</a>
~~~
<br>

- 글자 형태 태그

 1) `<b>`:  굵게
2)` <sup>`:  주)
3)` <u>`:  밑줄
4) `<sub>`:  작게
5) `<nobr>`:  특정 영역 줄바꿈 못하도록
<br>
- Marquee 태그

 1) `<marquee>`흐르는 문자열
2) `<marquee behavior="slide">`슬라이드 문자열
3) `<marquee behavior="alternate">`좌우 이동 문자열
<br>
- 목록 태그

 1) `<ol>` : 상위 항목
2) `<li>` : 하위 항목들
<br>
- 정의 목록 태그

 1) `<dl>` : 정의 목록
2) `<dt>` : 정의 용어
3) `<dd>` : 정의 설명
<br>
- 테이블 태그

         <tr><th> title1 </th> <th> title2 </th></tr>
         <tr><td>1행 1열</td> <td>1행 2열</td></tr>
         <tr><td>2행 1열</td> <td>2행 2열</td></tr>
         <tr><td>3행 1열</td> <td>3행 2열</td></tr>
         <tr><td>4행 1열</td> <td>4행 2열</td></tr>
<br>
- 테이블 태그 속성 : 테이블 내에 정의해주기
~~~
<table border="1" align="center"
	           width="80%" height="200"
	           bgcolor="silver" bordercolor="red"
	           cellpadding="20" cellspacing="30">
</table>
~~~
<br>
- 이미지 태그
```
<img alt= “” src=”./images/…”>
```
```
<img alt= “” src=”./images/…” width=”300” height=”200”>
// 이렇게 뒤에 설정 가능
```
```
: <img alt= “src= https://s.pstatic.net/static/www/mobile/edit/2020/0525/mobile_184814546796.jpg” >
//이렇게 링크 설정 가능
```
<br>
- 비디오 태그
~~~
``<video src="./contents/Wildlife.mp4"`
              controls="controls"
              autoplay="autoplay"
              loop="loop"
              width="640"
              height="480"></video>`
~~~
<video src="./contents/Wildlife.mp4"
              controls="controls"
              autoplay="autoplay"
              loop="loop"
              width="640"
              height="480"></video>

<br>
- 입력 양식 태그

 `<form action="">`
    
        <input type="text"/><br /> <!-- 글자 입력 양식 생성 -->
        <input type="button"/><br /> <!-- 버튼 생성 -->
        <input type="checkbox"/><br /> <!-- 체크박스 생성 -->
        <input type="file"/><br /> <!-- 파일 입력  생성 -->
        <input type="password"/><br /> <!-- 비밀번호 입력양식  생성 -->
        <input type="radio"/><br /> <!-- 라디오 버튼 생성 -->
        <input type="reset"/><br /> <!-- 초기화 버튼 생성 -->
        <input type="submit"/><br /> <!-- 제출 버튼 생성 -->
        <input type="hidden"/><br /> <!-- 보이지 않는 입력양식 생성 -->
         
    </form>
<br>
- Label 태그

 ~~~
<form action="">
        <label for="name">이름 : </label>
        <input type="text" id="name"/>
        <br />
        <label>비밀번호 : </label>
        <input type="password"/>
     </form>
~~~

<br>
- 입력 양식 태그
~~~
<form action="">
		<input type="color" /><br /><!-- 색상 선택 양식 생성 -->
		
		<input type="date" /><br /><!-- 일 선택 양식 생성 -->
		<input type="datetime-local" /><br /><!-- 일/시간 선택 양식 생성 -->
		<input type="datetime" value="2017-10-23"/><br /><!-- 일/시간 출력 -->
		
		<input type="email"/><br /><!-- 이메일 입력 양식 생성 -->
		<input type="number"/><br /><!-- 숫자 입력 양식 생성 -->
		<input type="range" value="9"/><br /><!-- 범위 선택 입력 양식 생성 -->
		<input type="search"/><br /><!-- 검색어 입력 양식 생성 -->
		<input type="tel"/><br /><!-- 전화번호 입력 양식 생성 -->
		<input type="url"/><br /><!--  URL 입력 양식 생성 -->
	</form>
~~~
<br>
- textarea 태그
~~~
-> 여러 줄의 글자를 입력할 때 사용하는 태그 &
   input 태그가 아닌 입력 양식 태그
   
   속성:
   - cols: 태그의 너비 지정,
   - rows: 태그의 높이 지정
   
   -- 예제))
   
   <textarea rows="5" cols="50">
      글자를 입력합니다(1).
      글자를 입력합니다(2).
      
      <!-- 이때에는 여백도 인식됨  -->
      
    </textarea>
~~~
<br>
- select 태그

~~~
<select>
 <option>김밥</>
 <option>떡볶이</>
 ...
 
 >>이렇게 선택할 수 있는 항목들 생김

~~~
<select>
 <option>김밥</option>
 <option>떡볶이</option>
  <option>순대</option>
 </select>
<br>
- Fieldset & legend 태그

~~~
입력 양식을 설명하는 태그.
  -legend 태그는 fieldset 태그안에서만 사용할 수 있음.
     -> 다른 곳에서 쓸 수 있지만 아무 효과가 없다.
~~~
~~~java
//예제
<form action="">
   
     <fieldset>
     <legend>로그인</legend>     
     <table>    
       <tr>
         <td><label for="id">아이디</label></td>
         <td><input type="text" id="id"></td>      
       </tr>      
        <tr>
         <td><label>비밀번호</label></td>
         <td><input type="password" id="pw"></td>      
       </tr>           
     </table>      
     
     <input type="submit" value="로그인">
     </fieldset>
   </form>

~~~
<br>
- 공간분할 태그
~~~
<h1>써주면 자동으로 줄 바꿈이 됨
이는 줄 바꿈의 개념이 아니라 h1이 차지하는 영역이 크기 때문에
줄 바꿈이 되는 것.
~~~

 ~~~
 -<div>: 한 줄의 개념 o
 -<span>: inline형식으로 공간 분할( 한 줄 안에 차례차례 위치하는 형식 )
 ~~~
<br>
- 시멘틱 구조 태그


	  . <header>: 헤더를 의미한다(회사명/로고).
	  . <nav>: 네비게이션을 의미(주메뉴 구성)한다.
	  . <aside>: 사이드에 위치(sub 메뉴/광고)하는 공간을 의미한다.
      . <section>: 여러 중심 내용을 감싸는 공간을 의미한다.
      . <article>: 글자가 많이 들어가는 부분을 의미한다.
	  . <footer> : 맺음말(ex>> 이용약관|주소(위치)|저작권|사이트맵)을 의미한다

<br>
- 문단 정렬 태그

~~~
<pre>: 소스코드에 쓰여있는 형식 그대로 결과 나타남( 복붙해도 형식 그대로)
<xmp>: 하나의 텍스트처럼 인식되어 처리
~~~
