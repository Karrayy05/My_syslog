# mysyslog

Проект mysyslog – это библиотека для логирования данных в различных форматах.

## Структура проекта

- libmysyslog: основная библиотека для логирования.
- libmysyslog-text: драйвер для вывода логов в текстовом формате.
- libmysyslog-json: драйвер для вывода логов в формате JSON.
- mysyslog-client: клиентское приложение для тестирования библиотеки.
- mysyslog-daemon: демон, работающий в фоновом режиме и записывающий логи.

## Особенности

- Поддерживаемые уровни журналирования: DEBUG, INFO, WARN, ERROR, CRITICAL.
- Поддерживаемые форматы вывода: текстовый формат и JSON.

## Сборка проекта с помощью Makefile

- make all: собирает все цели.
- make clean: удаляет все временные и объектные файлы, создаваемые при компиляции, возвращая исходные тексты к изначальному виду.
- make deb: собирает deb-пакет для программы.

## Использование

- mysyslog client: запуск клиентского приложения:  
  ./mysyslog-client -n "test message" -l INFO -d text -f /var/log/mysyslog.log

- mysyslog daemon: настройка конфигурации в /etc/mysyslog/mysyslog.cfg  
  и запуск демона:  
  sudo systemctl start mysyslog-daemon
