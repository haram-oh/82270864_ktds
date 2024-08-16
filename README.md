# template

## 프로젝트 설명
샘플 Spring boot Application

## 기능 목록
- TODO List 목록 조회, 삭제, 수정.
- JPA를 사용하여 스키마 및 샘플 데이터 생성.
- 로컬용 h2 mem db 샘플.
- 개발용 postgresql 접속 템플릿.

## Application 동작 방법
~~~bash
./mvnw spring-boot:run
~~~

- 웹브라우저에서 서버 또는 로컬 8080 포트로 접속
~~~
http://[hostname]:8080
~~~

## DB 접속 예제
~~~yaml
  datasource:
    # jdbc driver
    driver-class-name: org.postgresql.Driver
    # url: jdbc:postgresql://localhost:5432/postgres
    url: jdbc:postgresql://[hostname]:[port]/[database]
    # 사용자명
    username: sa
    # 비밀번호
    password: 1234
~~~

## 배포시 유의사항
- ingress.yaml host 변경
- 각자 네임스페이스에 배포