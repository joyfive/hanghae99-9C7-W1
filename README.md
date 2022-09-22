# 음반 검색 사이트


목차

## 팀원 및 역할

오기쁨(팀장) : 메인페이지 및 디자인 전반, 게시글 작성 페이지 크롤링 모듈 개발(python/js [POST]method) <br>
유도원 : 회원가입 및 로그인 <br>
안다민 : 게시판 상세보기 및 작성 <br>

## 프로젝트 소개

<p align="justify">
음반을 쿼리를 통해 유저가 직접 찾고 의견도 쓸 수 있는 게시글 형태의 홈페이지
</p>

<br>

## 기술 스택

HTML / CSS / JavaScript / Python / Flask / mongoDB

<br>

## 구현 기능

### 기능 1 : 회원가입 및 로그인
- jwt 이용한 회원가입 및 로그인 기능 구현

### 기능 2 : 메인페이지
####1) 리스팅 기능 [GET]method
- DB에 저장된 게시글 데이터 리스트 형태로 find 및 역순으로 sort (최신 게시글 노출)
- json 활용하여 프론트로 데이터 전달
- js for 문으로 개별 아이템별 딕셔너리 value 호출 
- temp_html로 가공된 데이터 사용자 노출

####2) 상세페이지 이동링크
- 게시글 저장 시 jinja 방식으로 구현한 상세url 활용* 
- temp_html 내 링크 연결 시 데이터의 'num' 필드 값을 활용한 상세페이지 url 이동

### 기능 3 : 게시글 입력 및 확인
####1) 크롤링 모듈 동작 : 
- JS) 사용자 input 값을 파라미터로 치환하여 POST 요청 
- Python) bs4 크롤링 및 데이터 가공 후 프론트로 response 전달 
- JS) 가공데이터로 temp_html 사용자 노출

####2) write.html 
- jinja 일부 활용한 게시판 기능 구현 
- 사용자가 지니뮤직의 파라미터값 입력 시 크롤링 모듈 동작
- 가공데이터로 전달받은 response 값은 사용자 노출 및 게시글 데이터 저장 시 같이 저장 
- 글제목+내용+별점 입력 후 함께 mongoDB에 데이터 저장 
- 게시글 작성 
- 메인페이지 정상 리스팅 확인

####3) view.html 
- 매개변수 keyworld [jinja] 상세 페이지 url 분기 [GET]:jinja를 활용한 서버사이드렌더링 방식
- write에서 POST한 크롤링데이터 및 사용자 데이터 find
- json으로 프론트에서 상세

<br>

## 배운 점 & 아쉬운 점
배운 점 <br>
(기쁨)

(도원)

(다민)
- post한 곳이 아닌 다른 페이지에서 get해올 수 있게 하는 게시판 방법 터득
- 크롤링 자료와 작성 자료 동시 데이터 저장 방법 터득
- 데이터 정렬 역순화
- github conflict 해결

아쉬운 점 <br>
- 좋아요 기능 구현
- 게시물 삭제 및 수정


<p align="justify">

</p>

<br>

## 라이센스

Copyright 2022. hang-hae99 9th W1 team C7. all rights reserved.
