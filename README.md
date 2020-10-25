# 2020JSstudy


## 20201025 Movie Seat Booking(자리 예매 시스템)
[Movie Seat Booking](https://github.com/bradtraversy/vanillawebprojects/tree/master/movie-seat-booking

---------------------------------------------------------------------------------------------------------
* 원하는 영화를 선택할 수 있다.  
* 원하는 영화에 따라 티켓 가격이 달라진다.  
* 원하는 자리를 선택하고 해제할 수 있다.  
* 이미 예매된 자리는 예매할 수 없다.  
* 선택한 자리 수만큼 가격이 올라간다.  

---------------------------------------------------------------------------------------------------------
#### 어려웠던 부분

#### 알게된 부분
  LocalStorage에 대해서는 처음 접해보는 개념이었다.  
  일정시간 또는 영구적으로 값을 저장하고 싶을 때 사용하는 것이 Web Storage API인 LocalStorage
  * 데이터를 사용자 로컬에 보존하는 방식
  * 데이터 저장, 덮어쓰기, 삭제 등 조작 가능
  * JS로 조작
  * 모바일에서도 사용 가능
  * key, value를 하나의 세트로 저장/도메인과 브라우저별로 저장/값은 반드시 문자열 또는 객체(JSON)나 배열 같은 형태로 저장
  * 세션이 끊기거나 동일한 세션이 아니더라도 사용 가능(sessionStorage와 차이점-브라우저 탭이 닫기면 삭제)
  * 유효기간이 없고 영구적으로 이용 가능하며 필요할 때 언제든 사용 가능(Cookie와 차이점-서버 접속시에 자동 송신)
  
  1. 데이터 추가 방법 3가지  
  function init() { //key, value  
	localStorage.Test = "Sample";  
	localStorage["Test"] = "Sample";  
	localStorage.setItem("Test", "Sample");  
  }
  
  2. 데이터 출력 방법 3가지  
  function init() {  
	var val = localStorage.Test;  
	var val = localStorage["Test"];  
	var val = localStorage.getItem("Test");  

	//취득 데이터 출력
	document.querySelector("#result").innerHTML = val;
  }
  
  3. 데이터 삭제하기(화면 출력시 undefined표시)  
  function init() {
	//localStorage 데이터 삭제  
	localStorage.removeItem("Test");   
	//localStorage 데이터 취득  
	var val = localStorage.Test;  
	//취득 데이터 출력  
	document.querySelector("#result").innerHTML = val;  
  }
  
  *clear()를 사용해서 데이터 전부 삭제 가능 localStrage.clear();
  
  
#### 보충하면 좋을 것 같은 부분  
 https://jess2.github.io/2018/06/06/JavaScript/JS-%EB%A1%9C%EC%BB%AC-%EC%8A%A4%ED%86%A0%EB%A6%AC%EC%A7%80-Local-Storage/

