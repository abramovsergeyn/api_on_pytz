1. Сервер api, порт 8080
2. api_pytz.py - api сервер; api_test.py - тест работы сервера
3. по запросу GET / отдает текущее время в запрошеной зоне в html, пустое время отдает в GTM
4. по запросу POST /api/v1/convert конвертирует время из одного часового пояса в другой часовой пояс
5. пример для проверки: curl -X POST -d '{"date": "10.10.2023 10:10:00", "tz": "EST"}' http://$IP_SERVER:8080/api/v1/convert/GMT
6. по запросу POST /api/v1/datediff отдает число секунд между датами из параметра json
7. пример для проверки: curl -X POST -d '{"first_date": "10.10.2024 10:10:00", "first_tz": "EST", "second_date": "12:30am 2024-10-10", "second_tz": "Europe/Moscow"}' http://$IP_SERVER:8080/api/v1/datediff
8. Ссылка на postman: 
