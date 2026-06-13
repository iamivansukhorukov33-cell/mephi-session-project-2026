# mephi-session-project-2026

Сессионный проект по администрированию рабочей станции под управлением GNU/Linux.

## Описание

В рамках проекта была установлена и настроена Fedora 43 Server в виртуальной машине UTM на macOS.

Цель проекта — выполнить базовую настройку Linux-сервера: сеть, hostname, web-сервер nginx, файловую систему, SELinux, пользователей, права доступа, capabilities для tcpdump и ограничения входа для root.

## Основные настройки

- ОС: Fedora Linux 43 Server Edition
- Архитектура: ARM64 / aarch64
- Hostname: `mephi-2026.domain.local`
- Статический IP: `192.168.1.100/24`
- Gateway: `192.168.1.1`
- DNS: `8.8.8.8`
- Web-сервер: `nginx`
- Web-root: `/data/mephi-web`
- Тестовая страница: `Hello from Student: M255648`
- SELinux: `Enforcing`
- Пользователь для администрирования: `mephi-admin`
- Группа: `mephi-devs`
- Пакет: `tcpdump-4.99.6-2.fc43.aarch64.rpm`

## Файлы проекта

| Файл | Назначение |
|---|---|
| `project_history.txt` | История выполненных команд и проверок |
| `network_check.txt` | Проверка сетевой связности |
| `nginx_recent_logs.txt` | Логи nginx |
| `fstab.txt` | Содержимое `/etc/fstab` |
| `selinux_status.txt` | Статус SELinux |
| `file_contexts.txt` | SELinux-контексты для web-директории |
| `tcpdump_capabilities.txt` | Capabilities для tcpdump |
| `permissions.txt` | Права доступа к `/data` и `/data/mephi-web` |
| `users_groups.txt` | Пользователи и группы |
| `index.html` | Тестовая web-страница |
| `curl_output.txt` | Результаты проверки web-сервера через curl |
| `mephi-nginx-screenshot.png` | Скриншот проверки nginx |
| `tcpdump-4.99.6-2.fc43.aarch64.rpm` | Скачанный RPM-пакет tcpdump |

## Проверка nginx

Web-сервер nginx настроен на отдачу страницы из директории `/data/mephi-web`.

Проверка выполнялась командами:

```bash
curl http://localhost
curl http://192.168.64.2
```

Ожидаемый результат:

```text
Hello from Student: M255648
```

## Итог

Проект выполнен в соответствии с требованиями задания.

Все необходимые артефакты загружены в данный репозиторий.
