# Getting Started

Nuevo Test

### Clean, Compile, Test, Jar

- gradlew.bat clean build

### Run Jar

- Local: gradlew.bat bootRun
- Background: nohup bash gradlew.bat bootRun &

### Testing Application

- Abrir navegador: http://localhost:8081/rest/mscovid/test?msg=testing
- curl -X GET 'http://localhost:8081/rest/mscovid/test?msg=testing'

## Linux

### Clean, Compile, Test, Jar

- gradle clean build

### Run Jar

- Local: gradle bootRun
- Background: nohup bash gradle bootRun &

### Testing Application

- Abrir navegador: http://localhost:8081/rest/mscovid/test?msg=testing
- curl -X GET 'http://localhost:8081/rest/mscovid/test?msg=testing'

# Using Docker to test this app.

## Docker in Linux

```bash
### Compile Test Jar Code
docker run --rm -it -p 9010:8081 -u gradle -v $(pwd):/home/gradle/project -w /home/gradle/project gradle gradle clean build

### Run Jar
docker run --rm -it -p 9010:8081 -u gradle -v $(pwd):/home/gradle/project -w /home/gradle/project gradle gradle bootRun &

curl -X GET 'http://localhost:9081/rest/mscovid/test?msg=testing'
```
