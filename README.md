"# architecture-sprint-6"

# Требуемые показатели

RTO = 45 мин
RPO = 15 мин
Доступность = 99,9%

На текущий момент сервис хранит ограниченный набор данных, который включает в себя:
базовую информацию о клиентах — ФИО, контакты, документы,
информацию о продуктах и тарифах,
историю заявок клиентов.
Общий объём данных, которые хранятся в системе, равен 50 GB.

LoadBalancer Kubernetes

# Задание 1

## Пункт 1

Приложения client-info, core-app, aggregator, settlement - stateless-приложения, поэтому оптимальным вариантом является
вертикальное масштабирование VPA в рамках кластера Kubernetes cluster 1.

## Пункт 2

### Приложение

Для обеспечения высокой степени отказоустойчивости применяется Active-Active фейловер-стретегия с георезервированием.
Независимые kubernetes кластеры с идентичными настройками разворачивается в двух ЦОДах. Для балансировки нагрузки и 
выполнении Active-Active фейловер-стретегии применяется Global Server Load Balancer.

### База данных

#### Конфигурация базы данных

#### Шардирование