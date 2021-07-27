# Официальный модуль приема платежей Robokassa для WordPress WooCommerce Subscriptions с поддержкой периодических платежей.

Рекуррентные платежи подключаются Робокассой после согласования, просто напишите запрос через личный кабинет.
ВНИМАНИЕ! Использование функционала переодических списаний возможно только при подключенной функции в личном кабинете Робокассы и с приобретенным плагином WooCommerce Subscriptions

Данный модуль позволяет добавить на сайт способ оплаты через Робокассу. 
Для корректной работы модуля необходима регистрация в сервисе.

Порядок регистрации описан в [документации Robokassa](https://docs.robokassa.ru/#7844)

### Возможности
* Возможность формирования подписочной системы на товары (рекуррентные списания)
* Передача состава товаров в заказе для отправки чека клиенту и в налоговую (54-ФЗ)
* Выбор платежной системы при оформление заказа, до отправки на страницу оплаты
* Выбор системы налогообложения
* Выбор размера ставки НДС для товаров в заказе
* Выгрузка товарных позиций в RoboMarket
* Поддержка оплаты через iframe (при данном типе оплаты не все платежные системы доступны)
* Приём платежей в тестовом режиме;
* Автоматическая смена статуса заказа;
* Поддержка отправки второго чека и маркировки товара

### Совместимость
Версия WordPress:5.7 или выше;

Версия PHP:5.6.32 или выше;

### Установка

1. Скачайте репозиторий в папку /wp-content/plugins/woocommerce_robokassa
2. Активируйте плагин в настройках WordPress /wp-admin/plugins.php
3. Настройте параметры подключения /wp-admin/admin.php?page=robokassa_payment_main_rb

### Настройка модуля

Настройка магазина на стороне [Робокассы](http://partner.robokassa.ru/)
1. Алгоритм расчета хеша – MD5
1. Result Url – http(s)://your-domain.ru/?robokassa=result
1. Success Url – http(s)://your-domain.ru/?robokassa=success
1. Fail Url – http(s)://your-domain.ru/?robokassa=fail
1. Метод отсылки данных по Result Url, Success Url и fail Url  – POST

Настройка на стороне сайта:
1. Указать платежные данные: Логин магазина, Пароль магазина #1, Пароль магазина #2
1. Активировать тестовый режим при необходимости, так же необходимо будет внести: Пароль магазина для тестов #1, Пароль магазина для тестов #2

### Фискализация

Для подключения автоматического формирования чеков в соответвии с ФЗ-54 необходимо подключить одну из доступных фискальных схем в Личном кабинете Robokassa ([Раздел "Фискализация"](https://partner.robokassa.ru/Fiscalization)) и указать настройки модуля:

* Система налогообложения.
* Признак способа расчёта.
* Признак предмета расчёта.
* Система налогообложения

### Changelog

= 1.0.0 =
* Добавлена поддержка плагина WooCommerce Subscriptions

= 1.0.1 =
* Добавлена поддержка WordPress 5.8

= 1.0.2 =
* Добавлена проверка факта установки плагина WooCommerce
