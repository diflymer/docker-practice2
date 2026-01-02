Registry:
![Registry:](screenshots/registry.png)

Auth:
Тест 1: Без аутентификации
![Без аутентификации](screenshots/withoutAuth.png)

С неправильным паролем:
![С неправильным паролем](screenshots/withWrongPass.png)

С правильным паролем:
![С правильным паролем](screenshots/withRightPass.png)

# Docker Orchestration Hands-on Lab

Характеристика узлов в режиме Active до перевода в Drain:
![Active1](screenshots/inActive1.png)
![Active2](screenshots/inActive2.png)
![Active3](screenshots/inActive3.png)

После перевода node2 в Drain:
![Drain1](screenshots/inDrain1.png)
![Drain2](screenshots/inDrain2.png)

Восстанавливаем в Active node2:
![reviveActive1](screenshots/reviveActive1.png)
![reviveActive2](screenshots/reviveActive2.png)

Работа сервисов на node2 не восстановилась!

Чтобы восстановить работу, нужно добавить новые задачи.

# Swarm stack introduction

![swarm1](screenshots/swarm1.png)
![swarm2](screenshots/swarm2.png)

# Репозиторий со счетчиком:
![counter1](screenshots/counter1.png)

Нагрузочное тестирование с 1 репликой:
![counter2](screenshots/counter2.png)

Нагрузочное тестирование с 4 репликами:
![counter3](screenshots/counter3.png)

Производительность выросла на 30% (с 2112 до 2740 RPS), среднее время отклика уменьшилось на 22% (с 4.73 до 3.65 мс),  хвост распределения ухудшился - максимальное время выросло с 15 до 36 мс.

Особенность реплицирования redis: то, что создадутся два разных redis с разными данными. Надо работать с помощью redis-master, redis-replica.