# Шаблон Go-проекта для домашних заданий

Шаблон для домашних заданий [Академии Бэкенда 2024](https://edu.tinkoff.ru/all-activities/courses/870efa9d-7067-4713-97ae-7db256b73eab).

Цель данного репозитория – познакомить вас с процессом разработки приложений на Go с использованием наиболее распространенных практик, инструментов и библиотек.

## Структура проекта

Это шаблон проекта, основанный на лучших практиках структурирования Go кода приложения. Проект содержит в себе следующие компоненты:

- `cmd` – директория, содержащая исполняемые файлы приложения. В данном шаблоне есть только один исполняемый файл `run`, который запускает приложение. Хорошей практикой является название пакета, содержащего `main.go` так же, как и название исполняемого файла. Таким образом в каждом домашнем задании вам будет необходимо изменять название пакета `run` на название, подходящее для вашего приложения.
- `internal` – директория, содержащая внутренние пакеты приложения. Внутренние пакеты не могут быть импортированы другими пакетами вне проекта.
  - `application` - пакет, в котором содержатся юзкейсы приложения.
  - `domain` - пакет, в котором содержатся модели приложения.
  - `infrastructure` - пакет, в котором содержатся инфраструктурные компоненты приложения(работа с выводом пользователю, работа с диском, работа с сетью и т.д.).
- `pkg` – директория, содержащая пакеты, которые могут быть импортированы другими пакетами вне проекта. Общей рекомендацией является то, что пакеты, содержащиеся в `pkg` должны быть независимыми от остальных пакетов проекта.