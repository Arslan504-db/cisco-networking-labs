# Лабораторные работы по сетям на Cisco

Практические работы по дисциплинам «Защита доступа в автоматизированных системах», «Сети и системы передачи информации» и «Информационная безопасность в сетях и телекоммуникациях». Направление 10.03.01 «Информационная безопасность».

## 🎯 Что сделано

Настроены и проверены в **Cisco Packet Tracer**:

### 🔹 Коммутация (L2)
- **VLAN** — создание, назначение портов, native VLAN
- **Транкинг** — 802.1Q, DTP, отключение автосогласования
- **Port Security** — ограничение MAC, violation mode (shutdown/restrict)
- **Защита STP** — PortFast, BPDU Guard, Root Guard
- **Отключение неиспользуемых портов**

### 🔹 Маршрутизация (L3)
- **Router-on-a-Stick** — маршрутизация между VLAN (подинтерфейсы 802.1Q)
- **Статическая маршрутизация**
- **Динамическая маршрутизация** — RIP v2, OSPF (area 0), EIGRP
- **Суммаризация маршрутов** (`ip summary-address`)
- **Перераспределение маршрутов** (`redistribute static`)

### 🔹 Сетевые сервисы
- **DHCP** — настройка DHCP-сервера на Cisco, исключение адресов
- **NAT** — статический, динамический с PAT (overload)
- **Переадресация портов** на маршрутизаторе Linksys

### 🔹 Безопасность
- **ACL** — стандартные, расширенные, именованные, нумерованные
  - Фильтрация по IP, протоколам (TCP, UDP, ICMP), портам (FTP, HTTP, HTTPS, Telnet)
  - Применение на интерфейсах (in/out)
- **IPS** — включение системы предотвращения вторжений на IOS
  - Настройка сигнатур, категорий, логирование в Syslog
- **AAA** — локальная аутентификация, TACACS+, RADIUS
- **ZPF** — зональный межсетевой экран (class-map, policy-map)
- **IPsec VPN** — site-to-site, ISAKMP policy, crypto map
- **Защищённый доступ** — пароли, SSH, шифрование паролей

### 🔹 Диагностика
- `ipconfig /all` — сетевые настройки
- `ping` — проверка связности
- `tracert` — трассировка маршрута
- `arp` — таблица ARP
- `route` — таблица маршрутизации
- `pathping` — задержки и потери

## 🧰 Стек

```
Cisco IOS        |  Packet Tracer  |  VLAN / 802.1Q
OSPF / EIGRP     |  ACL / NAT      |  IPsec VPN
ZPF / IPS / AAA  |  DHCP           |  Port Security
```

## 📸 Доказательства

### VLAN и транкинг
![VLAN](https://raw.githubusercontent.com/Arslan504-db/cisco-networking-labs/main/screenshot_vlan.png)

### ACL — конфигурация
![ACL](https://raw.githubusercontent.com/Arslan504-db/cisco-networking-labs/main/screenshot_acl.png)

### ACL — результат работы
![ACL Results](https://raw.githubusercontent.com/Arslan504-db/cisco-networking-labs/main/screenshot_acl_results.png)

### ACL — расширенный (Extended 199)
![ACL Extended](https://raw.githubusercontent.com/Arslan504-db/cisco-networking-labs/main/screenshot_acl_extended.png)

### NAT — трансляция адресов
![NAT](https://raw.githubusercontent.com/Arslan504-db/cisco-networking-labs/main/screenshot_nat.png)

### IPsec VPN — активный туннель
![VPN](https://raw.githubusercontent.com/Arslan504-db/cisco-networking-labs/main/screenshot_vpn.png)

## 📚 Что я узнал

- Как сегментировать сеть с помощью **VLAN**
- Как защитить L2 от атак (**Port Security, BPDU Guard, Root Guard**)
- Как настроить **маршрутизацию** (статику, OSPF, EIGRP)
- Как фильтровать трафик с помощью **ACL**
- Как работает **NAT** и **PAT**
- Как настроить **IPS**, **AAA**, **ZPF** и **IPsec VPN**
- Как диагностировать сеть утилитами **ping, tracert, arp, route, pathping**

## 🔗 Связанные проекты

- [Мини-SIEM на ELK](https://github.com/Arslan504-db/diploma-siem-education)
- [Мониторинг сетевого трафика](https://github.com/Arslan504-db/network-traffic-monitoring)
- [PKI на OpenSSL](https://github.com/Arslan504-db/pki-openssl-lab)
- [Пентест-лаборатория](https://github.com/Arslan504-db/pentest-lab-report)
