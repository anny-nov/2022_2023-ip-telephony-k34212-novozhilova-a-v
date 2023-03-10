<p> University: [ITMO University](https://itmo.ru/ru/)
<p> Faculty: [FICT](https://fict.itmo.ru)
<p> Course: [IP-telephony](https://github.com/itmo-ict-faculty/ip-telephony) <p>
<p> Year: 2022/2023
<p> Group: K34212
<p> Author: Novozhilova Anna Vladimirovna
<p> Lab: Lab1
<p> Date of create: 04.03.2023
<p> Date of finished: 05.03.2023

<h4>Отчёт о выполнении лабораторной работы</h4>
<h5>Часть 1</h5>

1. В этой части работы была создана схема сети, основанная на 4 коммутаторах, оединенных между собой. К каждому из коммутаторов подключены одно или несколько устройств (см. Рисунок 1).
<image src="https://github.com/anny-nov/2022_2023-ip-telephony-k34212-novozhilova-a-v/blob/main/lab1/img/1.png">
Рисунок 1 - Первая схема

2. Каждому компьютеру в этой сети был присвоен адрес из сети 192.168.0.0/24 (см. Рисунок 2).
<image src="https://github.com/anny-nov/2022_2023-ip-telephony-k34212-novozhilova-a-v/blob/main/lab1/img/2.png">
Рисунок 2 - Назначение адреса устройства

3. Для полноценной работы этой сети коммутаторы не нуждались в дополнительной настройке, однако с помощью командной строки была просмотрена их текущая конфигурация (см. Рисунок 3).
<image src="https://github.com/anny-nov/2022_2023-ip-telephony-k34212-novozhilova-a-v/blob/main/lab1/img/3.png">
Рисунок 3 - Конфигурация коммутатора

4. Поле этого любой компьютер сети может отправить пинг на любой другой компьютер и получить с него ответ (см. Рисунок 4).
<image src="https://github.com/anny-nov/2022_2023-ip-telephony-k34212-novozhilova-a-v/blob/main/lab1/img/4.png">
Рисунок 4 - Проверка связности

<h5>Часть 2</h5>

1. Была создана новая схема, в основе которой расположен маршрутизатор 2811, к нему подключен коммутатор, а к нему - два телефона, работающих по принципу IP-телефонии (см. Рисунок 5). Так как настройка сети еще не была проведена, связь между узлами не работает.
<image src="https://github.com/anny-nov/2022_2023-ip-telephony-k34212-novozhilova-a-v/blob/main/lab1/img/5.png">
Рисунок 5 - Вторая схема

2. Чтобы телефоны заработали, их необходимо подключить к блоку питания в разделе физического предтавления (см. Рисунок 6).
<image src="https://github.com/anny-nov/2022_2023-ip-telephony-k34212-novozhilova-a-v/blob/main/lab1/img/6.png">
Рисунок 6 - Подключение телефона к блоку питания

3. Роутеру было присвоено другое имя (см. Рисунок 7).
<image src="https://github.com/anny-nov/2022_2023-ip-telephony-k34212-novozhilova-a-v/blob/main/lab1/img/7.png">
Рисунок 7 - Смена имени роутера

4. Также интерфейс, связывающий маршрутизатор с коммутатором был приведен во включенное состояние, ему назначен IP-адрес и маска подсети (см. Рисунок 8)
<image src="https://github.com/anny-nov/2022_2023-ip-telephony-k34212-novozhilova-a-v/blob/main/lab1/img/8.png">
Рисунок 8 - Настройка интерфейса маршрутизатора

5. Затем был создан новый DHCP-пул phones, в который вошли все адреса из сети 192.168.0.0/24, не считая адрес маршрутизатора (см. Рисунок 9). Текущий маршрутизатор назначен дефолтным для этого пула, также включена опция 150, которая являетя обязательно для работы IP-телефонии.
<image src="https://github.com/anny-nov/2022_2023-ip-telephony-k34212-novozhilova-a-v/blob/main/lab1/img/9.png">
Рисунок 9 - Настройка DHCP

6. Был создан новый сервис IP-телефонии, вмещающий в себя 10 устройств и 10 телефонных номеров. Адреса для телефонов выдаются с дефолтного маршрутизатора (см. Риунок 10).
<image src="https://github.com/anny-nov/2022_2023-ip-telephony-k34212-novozhilova-a-v/blob/main/lab1/img/10.png">
Риунок 10 - Настройка VoIP

7. Маршрутизатор можно считать настроенным. Чтобы сеть работала, необходимо на коммутаторе включить поддержку VoIP-интерфейсов (см. Рисунок 11).
<image src="https://github.com/anny-nov/2022_2023-ip-telephony-k34212-novozhilova-a-v/blob/main/lab1/img/11.png">
Рисунок 11 - Настройка коммутатора

8. Телефонам в сети были выданы номера 111 и 222 соответственно (см. Рисунок 12).
<image src="https://github.com/anny-nov/2022_2023-ip-telephony-k34212-novozhilova-a-v/blob/main/lab1/img/12.png">
Рисунок 12 - Присвоение номеров

9. Теперь если через графический интерфейс позвонить с одного телефона на другой, соединение пройдет и будет подан соответствующий звуковой сигнал (см. Рисунок 13).
<image src="https://github.com/anny-nov/2022_2023-ip-telephony-k34212-novozhilova-a-v/blob/main/lab1/img/13.png">
Рисунок 13 - Проверка связи


**Выводы**: В результате выполнения лабораторной работы были собраны и настроены две схемы сети в Cisco Packet Tracer, освоены базовые принципы работы сетей на основе коммутаторов Cisco и сетей, ипользующих в работе технологию VoIP.
