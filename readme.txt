=== Robokassa payment gateway for Woocommerce Subscriptions ===
Contributors: Robokassa
Tags: robokassa payment gateway, robokassa, robokassa woocommerce, ecommerce, payment gateway, woo-commerce, woocommerce, woocommerce subscriptions, recurring payment, рекуррентные платежи, подписки, рекурренты ===
Requires at least: 5.0.2
Tested up to: 5.3
Stable tag: 5.3
Requires PHP: 5.6.32
License: GPLv2 or later
License URI: https://www.gnu.org/licenses/gpl-2.0.html

Позволяет использовать интерфейс (платежный шлюз) для оплаты через Робокассу в WooCommerce. Поддерживает интеграцию чеков (закон 54-ФЗ)

== Description ==

Данный плагин позволяет принимать платежи в Woocommerce Subscriptions через платежный шлюз Robokassa.

В плагине осуществлена  поддержка всех необходимых функций для приема платежей, такие как:
* Возможность формирования подписочной системы на товары (рекуррентные списания)
* Передача состава товаров в заказе для отправки чека клиенту и в налоговую (54-ФЗ)
* Выбор платежной системы при оформление заказа, до отправки на страницу оплаты
* Выбор системы налогообложения
* Выбор размера ставки НДС для товаров в заказе
* Выгрузка товарных позиций в RoboMarket
* Поддержка оплаты через iframe (при данном типе оплаты не все платежные системы доступны)

Robokassa – ведущий сервис по приёму платежей в сети Интернет, более 15 лет предлагающий максимально широкий спектр возможностей для оплаты товаров и услуг.

Основные преимущества:

* Быстрая интеграция
* Отсутствие абонентской платы и скрытых комиссий
* Все наиболее востребованные способы оплаты
* Удобный личный кабинет
* Комплекс решений по 54ФЗ
* Поддержка 24/7

Поддержка https://www.robokassa.ru

Почта: techsupport@robokassa.ru
Телефон: 8 (800) 500-25-57
https://www.robokassa.ru/ru/Support/SendMsg.aspx

Рекуррентные платежи подключаются Робокассой после согласования, просто напишите запрос через личный кабинет.
ВНИМАНИЕ! Использование функционала переодических списаний возможно только при подключенной функции в личном кабинете Робокассы и с приобретенным плагином WooCommerce Subscriptions

Если вы еще не клиент - то просим писать запрос на support@robokassa.ru

== Installation ==

Этапы установки плагина на сайт:

1. Скачайте репозиторий в папку /wp-content/plugins/woocommerce_robokassa
1. Активируйте плагин в настройках WordPress /wp-admin/plugins.php
1. Настройте параметры подключения /wp-admin/admin.php?page=robokassa_payment_main_rb

Настройка магазина на стороне [Робокассы](https://auth.robokassa.ru/partner/Login.aspx)
1. Алгоритм расчета хеша – MD5
1. Result Url – http(s)://your-domain.ru/?robokassa=result
1. Success Url – http(s)://your-domain.ru/?robokassa=success
1. Fail Url – http(s)://your-domain.ru/?robokassa=fail
1. Метод отсылки данных по Result Url, Success Url и fail Url  – POST

Настройка на стороне сайта:
1. Указать платежные данные: Логин магазина, Пароль магазина #1, Пароль магазина #2
1. Активировать тестовый режим при необходимости, так же необходимо будет внести: Пароль магазина для тестов #1, Пароль магазина для тестов #2

== Frequently Asked Questions ==

= Как вывести все платежные системы на странице оформления заказа =

Активировать режим выбора оплаты в магазине
`Настройки плагина > Общие настройки > Выбор способа оплаты - В магазине`

== Screenshots ==

1. `/assets/images/screenshot-1.png`
2. `/assets/images/screenshot-2.png`
3. `/assets/images/screenshot-3.png`

== Changelog ==

= 1.0 =
* Добавлена поддержка плагина WooCommerce Subscriptions

== Upgrade Notice ==

= 1.0 =
* При переходе на новую версию будут удалены все старые настройки!
