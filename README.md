# Sprint_7

## Модуль: Создание курьера (test_courier_creation.py)

- **`test_courier_created_successfully`** — Проверка успешного создания профиля при заполнении всех обязательных полей.
- **`test_courier_created_response_code`** — Валидация HTTP-статуса 201 в ответе на успешный запрос.
- **`test_courier_created_response_text`** — Проверка структуры ответа: наличие и истинность флага {"ok": true}.
- **`test_create_courier_withot_login_shows_error`** — Обработка ошибки, если не передано обязательное поле login.
- **`test_identical_couriers_cant_create`** — Запрет на регистрацию полных дубликатов курьеров.
- **`test_create_courier_when_login_repeat_shows_error`** — Контроль уникальности логина: система должна отклонять повторную регистрацию существующего имени пользователя.

## Модуль: Авторизация курьера (test_courier_login.py)

- **`test_courier_login_successfully`** — Успешная авторизация под существующим пользователем с валидными учетными данными.
- **`test_courier_login_get_id`** — Получение идентификатора (id) курьера в теле успешного ответа от сервера аутентификации.
- **`test_courier_login_withot_password_shows_error`** — Ошибка входа при отсутствии поля password в запросе.
- **`test_courier_login_with_invalid_password_shows_error`** — Отклонение запроса при вводе неверного пароля для существующего логина.
- **`test_non_existent_courier_login_shows_error`** — Обработка попытки входа под несуществующим аккаунтом.

## Модуль: Оформление заказа (test_order_creation.py)

- **`test_order_create_different_scooter_colors`** — Параметризованная проверка эндпоинта создания заказа. Тестирует передачу цветов BLACK, GREY, их комбинации [BLACK, GREY], а также отсутствие параметра цвета.

## Модуль: Просмотр доступных заказов (test_order_list.py)

- **`test_orders_get_list`** — Проверка получения массива заказов, которые доступны текущему курьеру для назначения или взятия в работу.
