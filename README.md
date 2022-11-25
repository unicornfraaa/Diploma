# **Запуск SUT, авто-тестов и генерация репорта**

**Подключение SUT к PostgreSQL:**

1. Запустить Docker Desktop
1. Открыть проект в IntelliJ IDEA
1. В терминале в корне проекта запустить контейнеры:
*docker-compose up -d*
1. Запустить приложение:
*java -jar aqa-shop.jar --spring.datasource.url=jdbc:postgresql://localhost:5432/app*
1. Открыть второй терминал и запустить тесты:
*./gradlew clean test -DdbUrl=jdbc:postgresql://localhost:5432/app*
1. Создать отчёт Allure и открыть в браузере:
*./gradlew allureServe*
1. Закрыть отчёт во втором терминале:
*CTRL + C* → *Y*
1. Перейти в первый терминал и остановить приложение: 
*CTRL + C* 

**Подключение SUT к MySQL:**

1. Запустить приложение в первом терминале:
*java -jar aqa-shop.jar --spring.datasource.url=jdbc:mysql://localhost:3306/app*
1. Во втором терминале  запустить тесты:
*./gradlew clean test -DdbUrl=jdbc:mysql://localhost:3306/app*
1. Создать отчёт Allure и открыть в браузере:
*./gradlew allureServe*
1. Закрыть отчёт во втором терминале:
*CTRL + C* → *Y*
1. Перейти в первый терминал и остановить приложение: 
*CTRL + C* 
1. Остановить контейнеры:
*docker-compose down*
