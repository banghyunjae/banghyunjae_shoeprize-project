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


