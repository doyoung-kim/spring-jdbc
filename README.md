# sample-api project 

MicroService Architecture 구성 및 패턴 설명을 위한 Sample Project 입니다.

## 빌드 및 실행

다음과 같이 빌드 및 실행할 수 있습니다.

```bash
# 빌드
./mvnw clean install -DskipTests
# 실행
./mvnw spring-boot:run
```

정상적인 실행을 위해서는 접속할 DB설정 및 sampledb.sql 실행이 필요합니다.

로컬 application-local.yml 파일 안에있는 정보로 DB접속정보를 맞춰주시기 바랍니다.

```roomsql
# 접속정보
    url: jdbc:mysql://localhost:3306/sampledb?autoReconnect=true&useUnicode=true&characterEncoding=utf8
    username: oscer
    password: Oscer2022@!

# DB 및 계정 생성을 위한 SQL
CREATE DATABASE sampledb DEFAULT CHARACTER SET utf8 COLLATE utf8_unicode_ci;
create user 'oscer'@'%' identified by 'Oscer2022@!';
grant all privileges on sampledb.* to 'oscer'@'%';
flush privileges;
```

실행 후 다음과 같이 테스트하실 수 있습니다.


## 브랜치 관리 전략

기본 브랜치를 main으로 사용

각 아키텍처 패턴 혹은 기술에 대한 예제는 sample이라는 명칭을 붙입니다. 

```
예) sample/cqrs = cqrs 패턴을 위한 예제
예) sample/with-apigw = api-gateway 테스트를 위한 예제
```
