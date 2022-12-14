# Отчётные документы по итогам тестирования

Отчёт по результату автоматизированного тестирования функционала покупки и оформления кредита по данным банковских карт веб-сервиса покупки тура "Путешествие дня".

## Количество тест-кейсов

Всего было проведено 60 автотестов. Общий процент успешных тестов равен 36.66%.

![1](https://user-images.githubusercontent.com/105659262/203978899-343cf22c-244d-4ed3-90ec-de3ceee18c85.png)

Результаты прогона тестов не зависят от типа подключенной БД, поэтому представлен единый отчёт по тестам.

### Результаты тестов по градации серьезности:

![2](https://user-images.githubusercontent.com/105659262/203980496-42400661-8255-43d2-96a0-85598a428d64.png)

### Результаты тестов по тестируемому функционалу:

![3](https://user-images.githubusercontent.com/105659262/203980759-7f9c0264-7a28-4aa4-9c47-10f64cdf2666.png)

### Общие итоги:

|                  | Кол-во тестов  | Passed | Failed | Passed, % |
|:-----------------|    :----:   |   :----:   |  :----:   |----------:|
| API тестирование | 16  | 4 | 12 |       25% |
| UI тестирование  | 44  | 18 | 26 |    40.91% |
| Всего            | 60  | 22 | 38 |    36.67% |

В результате прогона тестов было составлено 15 [issue](https://github.com/unicornfraaa/Diploma/issues).

## Общие рекомендации 

- для увеличения testability SUT рекомендуется добавить элементам страницы атрибут test-id
- необходимо качественная техническая документация по проекту
