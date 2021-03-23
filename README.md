# build 환경 만들기
 - $ sudo apt install openjdk-8-jdk-headless
 - $ sudo apt install zip unzip
 - $ curl -s "https://get.sdkman.io" | bash
 - $ sdk install gradle

# Code Base
 - 이 코드는 다음의 링크에 있는 예제를 기초로 함
 - https://spring.io/guides/gs/rest-service/

# Code Base에 없는 내용

## gradlew 파일이 없는 경우
 - $ gradle wrapper

## Application.java 파일 생성
 - RestServiceApplication.java

# datadog 설정
 - datadog agent 설치는 생략함
 - $ wget -O dd-java-agent.jar 'https://dtdg.co/latest-java-tracer'

# Run
 - $ ./gradlew bootRun
 - $ ./gradlew build
 - $ java -javaagent:./dd-java-agent.jar -Ddd.service=joseph -Ddd.env=develop -Ddd.http.server.tag.query-string=true -jar build/libs/rest-service-0.0.1-SNAPSHOT.jar


# 참고링크
 - https://sdkman.io/install
 - https://gradle.org/install/
 - https://spring.io/guides/gs/rest-service/
 - https://joochang.tistory.com/80
