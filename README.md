# 🏴‍☠️ OverTheWire Bandit Solutions & Writeups

Моя личная база знаний и шпаргалка по прохождению комнат **Bandit** на платформе **OverTheWire**. Содержит логику решений, концепции Linux CLI и команды для уровней 0–34.

---

## 🛠 Общие параметры подключения
* **Хост:** `bandit.labs.overthewire.org`
* **Порт:** `2220`

---

## 📚 Прохождение уровней

* **Level 0 ➔ 1:** Подключение по SSH (`ssh bandit0@... -p 2220`).
* **Level 1 ➔ 2:** Чтение файла с дефисом (`cat ./-`). Пароль: `[PASSWORD_FROM_LEVEL_1]`
* **Level 2 ➔ 3:** Файл с пробелами (`cat "spaces in this filename"`). Пароль: `[PASSWORD_FROM_LEVEL_2]`
* **Level 3 ➔ 4:** Скрытый файл (`ls -a`, `cat .hidden`). Пароль: `[PASSWORD_FROM_LEVEL_3]`
* **Level 4 ➔ 5:** Текстовый файл среди бинарных (`file ./*`). Пароль: `[PASSWORD_FROM_LEVEL_4]`
* **Level 5 ➔ 6:** Поиск по размеру и правам (`find inhere/ -type f -size 1033c ! -executable`). Пароль: `[PASSWORD_FROM_LEVEL_5]`
* **Level 6 ➔ 7:** Поиск по владельцу от корня с подавлением ошибок (`find / -user bandit7 -group bandit6 -size 33c 2>/dev/null`). Пароль: `[PASSWORD_FROM_LEVEL_6]`
* **Level 7 ➔ 8:** Поиск слова `millionth` через `grep`. Пароль: `[PASSWORD_FROM_LEVEL_7]`
* **Level 8 ➔ 9:** Уникальная строка (`sort data.txt | uniq -u`). Пароль: `[PASSWORD_FROM_LEVEL_8]`
* **Level 9 ➔ 10:** Чтение бинарника (`strings data.txt | grep "=="`). Пароль: `[PASSWORD_FROM_LEVEL_9]`
* **Level 10 ➔ 11:** Декодирование Base64 (`base64 -d data.txt`). Пароль: `[PASSWORD_FROM_LEVEL_10]`
* **Level 11 ➔ 12:** ROT13 шифр (`tr 'A-Za-z' 'N-ZA-Mn-za-m'`). Пароль: `[PASSWORD_FROM_LEVEL_11]`
* **Level 12 ➔ 13:** Распаковка многократно сжатых архивов (`xxd`, `gzip`, `bzip2`). Пароль: `[PASSWORD_FROM_LEVEL_12]`
* **Level 13 ➔ 14:** Использование SSH-ключа (`ssh -i sshkey.private ...`).
* **Level 14 ➔ 15:** Отправка пароля на локальный порт через `nc`. Пароль: `[PASSWORD_FROM_LEVEL_14]`
* **Level 15 ➔ 16:** SSL/TLS соединение (`openssl s_client`). Пароль: `[PASSWORD_FROM_LEVEL_15]`
* **Level 16 ➔ 17:** Сканирование портов (`nmap`) и получение SSL-ключа.
* **Level 17 ➔ 18:** Сравнение файлов (`diff`). Пароль: `[PASSWORD_FROM_LEVEL_17]`
* **Level 18 ➔ 19:** Обход принудительного выхода по SSH. Пароль: `[PASSWORD_FROM_LEVEL_18]`
* **Level 19 ➔ 20:** SUID-бинарник (`./bandit20-do`). Пароль: `[PASSWORD_FROM_LEVEL_19]`
* **Level 20 ➔ 21:** Сетевое взаимодействие с `suconnect`. Пароль: `[PASSWORD_FROM_LEVEL_20]`
* **Level 21 ➔ 22:** Анализ `cron`-задач. Пароль: `[PASSWORD_FROM_LEVEL_21]`
* **Level 22 ➔ 23:** Генерация MD5-хеша для имени файла. Пароль: `[PASSWORD_FROM_LEVEL_22]`
* **Level 23 ➔ 24:** Создание скрипта для `cron`. Пароль: `[PASSWORD_FROM_LEVEL_23]`
* **Level 24 ➔ 25:** Брутфорс PIN-кода в цикле. Пароль: `[PASSWORD_FROM_LEVEL_24]`
* **Level 25 ➔ 26:** Побег из кастомной оболочки через `more` и `vi`.
* **Level 26 ➔ 27:** SUID-бинарник. Пароль: `[PASSWORD_FROM_LEVEL_26]`
* **Level 27 ➔ 28:** Клонирование Git-репозитория. Пароль: `[PASSWORD_FROM_LEVEL_27]`
* **Level 28 ➔ 29:** История коммитов (`git log -p`). Пароль: `[PASSWORD_FROM_LEVEL_28]`
* **Level 29 ➔ 30:** Переключение по веткам Git. Пароль: `[PASSWORD_FROM_LEVEL_29]`
* **Level 30 ➔ 31:** Использование тегов Git (`git tag`). Пароль: `[PASSWORD_FROM_LEVEL_30]`
* **Level 31 ➔ 32:** Push в удаленный репозиторий.
* **Level 32 ➔ 33:** Побег из `UPPERCASE shell` через параметры `$0`. Пароль: `[PASSWORD_FROM_LEVEL_32]`
* **Level 33 ➔ 34:** Финальный уровень.

*Полный исходный код со всеми деталями команд и теорией доступен в репозитории.*
