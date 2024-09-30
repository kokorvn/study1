Week3 과제
=========

MTV 패턴이란?
-----------

* 아키텍처 패턴이란?
  - 재사용 될 수 있는 일반화 된 솔루션
  - 유지보수성, 재사용성, 확장성 보장
  
* MVC 패턴이란?
  - 소프트웨어를 Model, View, Controller로 나눠 설계하는 방식
  - Model: 데이터 입출력
  - View: 응답
  - Controller: Model과 View의 전체적인 제어 담당
  
* Django에서의 MTV? (맥도날드 주문의 예시)
  - Model, Template, View
  1. User -> urls.py : 웹브라우저의 요청
  2. urls.py -> views.py : 00점의 주문을 받는 view에게 요청 정보 전달
  3. views.py : 요청 정보 가공, 추가 정보 필요할 시 models사용
  4. views.py -> models.py : 1955버거 레시피 요청
  5. models.py : DB에서 조회 후 반환
  6. views.py -> templates : 응답에 필요한 정보를 양식에 맞춰 가공 후 전달
  7. user에게 전달 