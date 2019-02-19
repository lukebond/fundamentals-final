FROM maven:3-jdk-8-alpine
ADD . /build
WORKDIR /build
RUN mvn -B -f pom.xml \
  -s /usr/share/maven/ref/settings-docker.xml \
  dependency:resolve
RUN mvn -B -s /usr/share/maven/ref/settings-docker.xml \
  package -DskipTests
CMD java -jar /app/ddev-0.0.1-SNAPSHOT.jar \
  --spring.profiles.active=postgres
