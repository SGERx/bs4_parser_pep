# Проект парсинга pep

## Технологии проекта

- Python — язык программирования.
- BeautifulSoup4 - библиотека для парсинга.
- Prettytable - библиотека для удобного отображения табличных данных.

### Функционал

- Парсер собирает данные о PEP-документах, сравнивает статусы и записывает их в CSV-файл,
также парсер собирает информацию о статусе версий, скачивает архив с документацией и собирает ссылки о новостях в Python.

### Режимы работы парсера:

- whats-new
- latest-versions
- download
- pep

### Как запустить проект:

Клонировать репозиторий:

```bash
git clone git@github.com:SGERx/bs4_parser_pep.git
```

Cоздать и активировать виртуальное окружение:

```bash
python3 -m venv env
source venv/Scripts/activate
```
Установить зависимости из файла requirements.txt:

```bash
python3 -m pip install --upgrade pip
pip install -r requirements.txt
```

Программа запускается из main.py директории ./src/:

```bash
python main.py [вариант парсера] [аргументы]
```

### Режимы работы
Сбор ссылок на статьи о нововведениях в Python:

```bash
python main.py whats-new
```
Сбор информации о версиях Python:

```bash
python main.py latest-versions
```
Скачивание архива с актуальной документацией:

```bash
python main.py download
```
Сбор статусов документов PEP и подсчёт статусов:

```bash
python main.py pep
```

### Аргументы командной строки
Полный список аргументов:

```bash
python main.py -h
```

```bash
usage: main.py [-h] [-c] [-o {pretty,file}] {whats-new,latest-versions,download,pep}

Парсер документации Python

positional arguments:
  {whats-new,latest-versions,download,pep}
                        Режимы работы парсера

optional arguments:
  -h, --help            show this help message and exit
  -c, --clear-cache     Очистка кеша
  -o {pretty,file}, --output {pretty,file}
                        Дополнительные способы вывода данных
```
