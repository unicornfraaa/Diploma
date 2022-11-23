# **Запуск SUT, авто-тестов и генерация репорта**

**Подключение SUT к PostgreSQL:**

1. Запустить Docker Desktop
1. Открыть проект в IntelliJ IDEA
1. В терминале в корне проекта запустить контейнеры:
*docker-compose up -d*
1. Запустить приложение:
*java -jar aqa-shop.jar --spring.datasource.url=jdbc:postgresql://localhost:5432/app*
1. Открыть второй терминал
1. Запустить тесты:
*./gradlew clean test -DdbUrl=jdbc:postgresql://localhost:5432/app*
1. Создать отчёт Allure и открыть в браузере:
*./gradlew allureServe*
1. Закрыть отчёт
1. Перейти в первый терминал
1. Остановить приложение: 
*CTRL + C* → *Y*
1. Остановить контейнеры:
*docker-compose down*

**Подключение SUT к MySQL:**

1. Запустить Docker Desktop
1. Открыть проект в IntelliJ IDEA
1. В терминале в корне проекта запустить контейнеры:
*docker-compose up -d*
1. Запустить приложение:
*java -jar aqa-shop.jar --spring.datasource.url=jdbc:mysql://localhost:3306/app*
1. Открыть второй терминал
1. Запустить тесты:
*./gradlew clean test -DdbUrl=jdbc:mysql://localhost:3306/app*
1. Создать отчёт Allure и открыть в браузере:
*./gradlew allureServe*
1. Закрыть отчёт
1. Перейти в первый терминал
1. Остановить приложение: 
*CTRL + C* → *Y*
1. Остановить контейнеры:
*docker-compose down*
