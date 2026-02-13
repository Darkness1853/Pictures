# Структура Нашей базы данных postgres_billing_db
## call_records (записи вызовов)
| Столбец | Описание (Description) |
| :--- | :--- |
| `record_id` | Уникальный идентификатор записи (Unique record identifier) |
| `subscriber_id` | Идентификатор абонента (Subscriber identifier) |
| `service_type_id` | Идентификатор типа услуги (Service type identifier) |
| `call_date` | Дата и время вызова (Call date and time) |
| `destination_number` | Номер назначения (Destination phone number) |
| `duration_seconds` | Длительность в секундах (Duration in seconds) |
| `quantity` | Количество (например, количество СМС) (Quantity, e.g., number of SMS) |
| `cost` | Стоимость вызова (Cost of the call) |

## data_usage (использование данных)
| Столбец | Описание (Description) |
| :--- | :--- |
| `usage_id` | Уникальный идентификатор использования (Unique usage identifier) |
| `subscriber_id` | Идентификатор абонента (Subscriber identifier) |
| `usage_date` | Дата использования (Usage date) |
| `data_mb` | Объем данных в МБ (Data volume in MB) |
| `cost` | Стоимость использованных данных (Cost of data used) |

## invoices (счета)
| Столбец | Описание (Description) |
| :--- | :--- |
| `invoice_id` | Уникальный идентификатор счета (Unique invoice identifier) |
| `subscriber_id` | Идентификатор абонента (Subscriber identifier) |
| `billing_period` | Расчетный период (Billing period) |
| `issue_date` | Дата выписки счета (Invoice issue date) |
| `due_date` | Срок оплаты (Payment due date) |
| `monthly_fee` | Ежемесячная плата за тариф (Monthly plan fee) |
| `usage_charges` | Начисления за использование (Usage charges) |
| `total_amount` | Итоговая сумма к оплате (Total amount due) |
| `status` | Статус счета (Invoice status) |

## payments (платежи)
| Столбец | Описание (Description) |
| :--- | :--- |
| `payments_id` | Уникальный идентификатор платежа (Unique payment identifier) |
| `subscriber_id` | Идентификатор абонента (Subscriber identifier) |
| `invoice_id` | Идентификатор оплачиваемого счета (Paid invoice identifier) |
| `payment_date` | Дата платежа (Payment date) |
| `amount` | Сумма платежа (Payment amount) |
| `payment_method` | Способ оплаты (Payment method) |
| `transaction_id` | Идентификатор транзакции (Transaction identifier) |

## plan_changes (изменение планов)
| Столбец | Описание (Description) |
| :--- | :--- |
| `change_id` | Уникальный идентификатор изменения (Unique change identifier) |
| `subscriber_id` | Идентификатор абонента (Subscriber identifier) |
| `old_plan_id` | Идентификатор старого тарифного плана (Old tariff plan identifier) |
| `new_plan_id` | Идентификатор нового тарифного плана (New tariff plan identifier) |
| `change_date` | Дата изменения (Change date) |
| `reason` | Причина изменения (Reason for change) |

## service_types (типы служб)
| Столбец | Описание (Description) |
| :--- | :--- |
| `service_type_id` | Уникальный идентификатор типа услуги (Unique service type identifier) |
| `service_name` | Название услуги (Service name) |
| `description` | Описание услуги (Service description) |

## subscribers (абоненты)
| Столбец | Описание (Description) |
| :--- | :--- |
| `subscriber_id` | Уникальный идентификатор абонента (Unique subscriber identifier) |
| `phone_number` | Номер телефона (Phone number) |
| `first_name` | Имя (First name) |
| `last_name` | Фамилия (Last name) |
| `email` | Адрес электронной почты (Email address) |
| `plan_id` | Идентификатор текущего тарифного плана (Current tariff plan identifier) |
| `registration_date` | Дата регистрации (Registration date) |
| `status` | Статус аккаунта (Account status) |
| `balance` | Баланс счета (Account balance) |

## tariff_plans (тарифные планы)
| Столбец | Описание (Description) |
| :--- | :--- |
| `plan_id` | Уникальный идентификатор тарифного плана (Unique plan identifier) |
| `plan_name` | Название тарифа (Plan name) |
| `monthly_fee` | Ежемесячная абонентская плата (Monthly subscription fee) |
| `minutes_included` | Включенные минуты (Minutes included) |
| `sms_included` | Включенные СМС (SMS included) |
| `data_gb_included` | Включенный трафик данных в ГБ (Data traffic included in GB) |
| `price_per_minute` | Цена за минуту сверх пакета (Price per extra minute) |
| `price_per_sms` | Цена за СМС сверх пакета (Price per extra SMS) |
| `price_per_gb` | Цена за ГБ сверх пакета (Price per extra GB) |
| `is_active` | Флаг активности тарифа (Plan active flag) |