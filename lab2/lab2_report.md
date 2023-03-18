<p> University: [ITMO University](https://itmo.ru/ru/)
<p> Faculty: [FICT](https://fict.itmo.ru)
<p> Course: [IP-telephony](https://github.com/itmo-ict-faculty/ip-telephony) <p>
<p> Year: 2022/2023
<p> Group: K34212
<p> Author: Novozhilova Anna Vladimirovna
<p> Lab: Lab2
<p> Date of create: 18.03.2023
<p> Date of finished: 18.03.2023

<h4>Отчёт о выполнении лабораторной работы</h4>
**Цель работы**: Изучить построение сети IP-телефонии с помощью маршрутизатора Cisco 2811, коммутатора Cisco catalyst 3560 и IP телефонов Cisco 7960.

<h5>Часть 1</h5>

1. В этой части работы была создана схема сети, состоящая из последовательно подулюченных друг к другу роутера и коммутатора, к которому в свою очередь подключены три IP-телефона (см. Рисунок 1).
<image src="https://github.com/anny-nov/2022_2023-ip-telephony-k34212-novozhilova-a-v/blob/main/lab2/img/1.png">
Рисунок 1 - Первая схема

2. Имя роутера было изменено на CMERouter (см. Рисунок 2).
<image src="https://github.com/anny-nov/2022_2023-ip-telephony-k34212-novozhilova-a-v/blob/main/lab2/img/2.png">
Рисунок 2 - Изменение имени устройства

3. С помощью консольной команды был отключен синтаксис ввода слов от DNS серверов. (см. Рисунок 3).
<image src="https://github.com/anny-nov/2022_2023-ip-telephony-k34212-novozhilova-a-v/blob/main/lab2/img/3.png">
Рисунок 3 - Отключение синтаксиса ввода слов

4. На физическую консоль, а также на пять самых используемых при подключении по SSH и Telnet был установлен пароль (см. Рисунок 4).
<image src="https://github.com/anny-nov/2022_2023-ip-telephony-k34212-novozhilova-a-v/blob/main/lab2/img/4.png">
Рисунок 4 - Назначение паролей

5. Для роутера был сконфигурирован интерфейс, включая IP-адрес и маску подсети. После настройки интерфейс был переведен в статус On (см. Рисунок 5).
<image src="https://github.com/anny-nov/2022_2023-ip-telephony-k34212-novozhilova-a-v/blob/main/lab2/img/5.png">
Рисунок 5 - Настройка интерфейса

6. На роутере был создан новый dhcp-пул адресов, с включенной опцией 150, что позволяет использовать назначенные адреса в телефонии.
<image src="https://github.com/anny-nov/2022_2023-ip-telephony-k34212-novozhilova-a-v/blob/main/lab2/img/6.png">
Рисунок 5 - Создание пула адресов

7. Были установлены настройки сервиса телефонии: задано максимально возможное количество телефонов и номеров, указан источник IP-адресов, настроено автоматическое распределение линий (см. Рисунок 7).
<image src="https://github.com/anny-nov/2022_2023-ip-telephony-k34212-novozhilova-a-v/blob/main/lab2/img/7.png">
Рисунок 5 - Настройки телефонии

8. Телефоны были включены в сеть питания (см. Рисунок 8)
<image src="https://github.com/anny-nov/2022_2023-ip-telephony-k34212-novozhilova-a-v/blob/main/lab2/img/8.png">
Рисунок 5 - Подключение телефонов к блоку питания

9. Каждому телефону был назначен внутренний номер (см. Рисунок 9).
<image src="https://github.com/anny-nov/2022_2023-ip-telephony-k34212-novozhilova-a-v/blob/main/lab2/img/9.png">
Рисунок 9 - Назначение номеров

10. В результате настройки все телефоны могут связываться друг с другом по внутренней линии (см.Рисунок 10)
<image src="https://github.com/anny-nov/2022_2023-ip-telephony-k34212-novozhilova-a-v/blob/main/lab2/img/10.png">
Рисунок 10 - Проверка связности

<h5>Часть 2</h5>

1. К схеме из предыдущего упражнение были добавлены стационарные компьютеры, которые подключены к телефонам (см. Рисунок 11).
<image src="https://github.com/anny-nov/2022_2023-ip-telephony-k34212-novozhilova-a-v/blob/main/lab2/img/11.png">
Рисунок 11 - Вторая схема

2. На коммутаторе были созданы виртуальные локальные сети для разграничения сети, которая связывает коммутатор и роутер, телефонной сети и компьютерной сети (см. Рисунок 12).
<image src="https://github.com/anny-nov/2022_2023-ip-telephony-k34212-novozhilova-a-v/blob/main/lab2/img/12.png">
Рисунок 12 - Создание VLAN

3. Интерфейсы коммутатора, подключенные к телефонам,были переведены в режим access с поддержкой двух VLAN: одна вирутальная сеть указывается как голосовая, вторая - как стандартная (см. Рисунок 13).
<image src="https://github.com/anny-nov/2022_2023-ip-telephony-k34212-novozhilova-a-v/blob/main/lab2/img/13.png">
Рисунок 13 - Настройка интерфейсов

4. Интерфейс коммутатора, подключенный к роутеру, был настроен как транк, пропускающий трафик из всех VLAN (см. Рисунок 14)
<image src="https://github.com/anny-nov/2022_2023-ip-telephony-k34212-novozhilova-a-v/blob/main/lab2/img/14.png">
Рисунок 14 - Настройка транк-интерфейса

5. На роутере были настроены подинтерфейсы для интерфейса Fa0/0, каждый из которых соответствует определенной VLAN (см. Рисунок 15)
<image src="https://github.com/anny-nov/2022_2023-ip-telephony-k34212-novozhilova-a-v/blob/main/lab2/img/15.png">
Рисунок 15 - Создание дополнительных интерфейсов

6. Были добавлены раздельные пулы IP-адресов для каждой отдельно взятой виртуальной подсети (см. Риунок 16).
<image src="https://github.com/anny-nov/2022_2023-ip-telephony-k34212-novozhilova-a-v/blob/main/lab2/img/16.png">
Риунок 16 - Настройка пулов

7. Телеофния была настроена заново, изменен IP-адрес DHCP-сервера для получения адресов (чтобы адреса соответствовали нужной виртуальной подсети), заново назначены внутренние телефонные номера (см. Рисунок 17).
<image src="https://github.com/anny-nov/2022_2023-ip-telephony-k34212-novozhilova-a-v/blob/main/lab2/img/17.png">
Рисунок 11 - Повторная настройка телефонии

8. В результате настройки все устройства получили IР-адреса внутри соответствующих VLAN. Проведена проверка доступности с помощью пингов с роутера (см. Рисунок 18) и станционарного компьютера (см. Рисунок 19).
<image src="https://github.com/anny-nov/2022_2023-ip-telephony-k34212-novozhilova-a-v/blob/main/lab2/img/19.png">
Рисунок 18 - Результаты пингов с роутера
<image src="https://github.com/anny-nov/2022_2023-ip-telephony-k34212-novozhilova-a-v/blob/main/lab2/img/21.png">
Рисунок 18 - Результаты пингов с компьютера

9. Также проведена проверка связности телефон друг с другом (см. Рисунок 20).
<image src="https://github.com/anny-nov/2022_2023-ip-telephony-k34212-novozhilova-a-v/blob/main/lab2/img/20.png">
Рисунок 20 - Проверка связи


**Выводы**: В результате выполнения лабораторной работы было изучено построение сети IP-телефонии с помощью маршрутизатора Cisco 2811, коммутатора Cisco catalyst 3560 и IP телефонов Cisco 7960.
