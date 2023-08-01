Shoeprize Project
=================
* 모델
    * 제조사(제품 생산업체)
        * 제조사명
        * 제조사 영문명
    * 제품
        * 제품명 : 예)에어 맥스 99
        * 제품명 영문 : 예)AIR MAX 99
        * 제품코드: 10자 내외의 문자열 (예 : ABCD-012)
        * 제조사
        * 출시일시
        * 가격 : 달러, 유로, 원, 엔 등의 정보 저장 필요
        * 관리자 코멘트 : 한글 및 유니코드 100자 내외의 문자열
----------------------------------------------------
* API
    * 제조사 등록 API
    * 제조사 조회 API GET /{제조사 모델명}/{UUID}
        * 존재하지 않는 UUID 처리 필수
    * 제품 등록 API
    * 제품 조회 API GET /{제품 모델명}/{UUID}
        * 제품정보와, 제조사 정보를 모두 포함합니다.
        * 관리자 코멘트는 노출하지 않습니다.
        * 출시 일시는 조회하는 국가에 따라 클라이언트에서 표시할 예정입니다.
        * 존재하지 않는 UUID 처리 필수
------------------------------------------------------------
* 참고
    * 모델의 필드 추가 제한 없음
        * API는 RESTfull 규칙을 준수합니다.
------------------------------------------------------------

shoeprize 사전과제

DRF APIView를 사용해서 RESTful한 API를 구현<br>
관리자 코멘트는 blank, null = True 설정, 시리얼라이저에 미포함<br>
try, except를 활용 존재하지 않는 제조사, 제품의 UUID 가 있다면 404<br>
postman을 활용해 테스트 구현

<img width="859" alt="스크린샷 2023-07-28 오후 6 11 43" src="https://github.com/banghyunjae/banghyunjae_shoeprize-project/assets/127192957/5dcf6036-9a02-4ddc-be99-4a2bd2405ecb">

<img width="856" alt="스크린샷 2023-07-28 오후 6 11 55" src="https://github.com/banghyunjae/banghyunjae_shoeprize-project/assets/127192957/c8d7d945-062c-4c35-b085-ddc4b6cb2195">

<img width="855" alt="스크린샷 2023-07-28 오후 6 12 02" src="https://github.com/banghyunjae/banghyunjae_shoeprize-project/assets/127192957/742b0001-f24f-4c9c-99d7-a87e679eeec9">

<img width="853" alt="스크린샷 2023-07-28 오후 6 12 09" src="https://github.com/banghyunjae/banghyunjae_shoeprize-project/assets/127192957/c08d4b3a-e23f-47d9-a739-ed9113ff40dc">

