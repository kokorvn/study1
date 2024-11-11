HTTP Method
===========

브라우저 캐싱이란?
--------------
1. client가 server에게 Index.html을 달라 요청하고
2. server는 client 에게 내용을 반환해주는 것
   
* 캐싱을 하면 안 되는 경우
  :: 로그인 화면 / 은행업무 / 원서 접수 등 개인정보가 중요하거나 중복 접수의 에러 발생 시

* 단순 조회 요청
  1) 여러 번 요청해도 결과 동일
  2) url에 정보를 넣어 전달해도 됨
  3) 캐싱 가능
   
* 새로운 리소스 생성 요청
  1) 요청마다 결과 변경 가능
  2) 민감한 정보를 다룸
  3) 캐싱 불가능

- 요청의 분류
: GET/ POST/ PUT/ DELETE/ PATCH/ OPTIONS/ HEAD

1) GET
   * 웹 브라우저의 기본 Http Method
   * 브라우저 캐싱 기능 지원
   * 정보 읽기, 검색 요청에 주로 사용됨
   * url에 정보를 넣어 전달
  
2) POST
   * 기본 지원 x
   * 캐싱 기능 지원x( 멱등성 x)
   * 새로운 요소 생성, 로그인 등에 사용됨
   * Request Body에 정보 들어감


Http Request
------------
1) start-line( 시작 라인 )
2) header( 헤더 )
3) Empty-line ( 공백 라인 )
4) message-body( 바디 )
   
* form/ input?
  - 데이터를 입력받고 전송하기 위한 태그
  - Input태그에서 데이터를 입력받을 수 있고, form 태그의 action 속성의 url로 전송
  - form 태그의 method 속성은 POST로 변경해서 POST방식으로 요청 가능

* 1) Input
  - input 태그의 type 속성을 이용해 입력받을 데이터 양식 정할 수 있다
  - type = 'submit'인 input 태그 혹은 <button> 태그를 사용하면 제출 버튼을 만들 수 있다
  - name 속성을 이용해 정보를 전달할 때 키 값을 지정할 수 있다
  
* 2) Form
  - form 태그 안에 input태그를 중첩해 원하는 양식의 데이터를 사용자에게 입력받을 수 있다
  - action 속성에 지정한 링크로 입력받은 데이터를 전송한다
  - method 속성에 지정한 http method를 이용해 전송한다