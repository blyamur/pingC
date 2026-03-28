# pingC

Python script for continuous ping monitoring with colored status indicators and logging.  
Скрипт на Python для постоянного мониторинга доступности ресурсов с цветными статусами и логированием.

Updated 17/12/2025

---

## Features / Особенности
- **Pings multiple hosts** from a configurable list  
  **Пингует несколько хостов** из настраиваемого списка
- **Color-coded status** (Online, Freeze, Sleep, Offline)  
  **Цветовые статусы** (Онлайн, Задержка, Сон, Оффлайн)
- **Automatic logging** of failures to a text file  
  **Автоматическое логирование** проблем в текстовый файл
- **Sound and visual alerts** on Windows when a host is down  
  **Звуковые и визуальные оповещения** в Windows при недоступности хоста
- **Adjustable check interval**  
  **Настраиваемый интервал** проверки

---

## Quick Start / Быстрый старт

### 1. Install dependencies / Установите зависимости

```
pip install pythonping
pip install datetime
pip install time
pip install os
pip install PyAutoGUI
pip install colorama
```

### 2. Prepare settings.xml / Подготовьте settings.xml
Create a file settings.xml in the following format (one host per line):

Создайте файл settings.xml в формате (по одному хосту на строку):

```
ya.ru: Яндекс
8.8.8.8: Google DNS
github.com: GitHub
192.168.1.1: Router
```

### 3. Run the script / Запустите скрипт
   
```
python pingC.py
```

### Configuration / Настройка

#### 1. Hosts list / Список хостов
Edit the settings.xml file in the format:

Измените файл settings.xml в формате:

```
address_or_ip: Display Name

адрес_или_ip: Отображаемое имя
```

#### 2. Check interval / Интервал проверки

Adjust in the script (line 11):

Настройте в скрипте (строка 11):

```
sleep_interval = 30  # seconds / секунды
```

### Notes / Примечания
```
Windows: Run as administrator (required for ping)
Windows: Запускайте от имени администратора (требуется для ping)
```
```
Logs: The error_logs.txt file is created automatically in the script directory
Логи: Файл error_logs.txt создаётся автоматически в папке со скриптом
```
```
Exit: Use Ctrl+C to exit the script
Выход: Используйте Ctrl+C для выхода из скрипта
```
```
Columns: Display columns automatically adjust to fit the longest hostname/IP
Колонки: Колонки отображения автоматически подстраиваются под самый длинный хост/IP
```

###  Status Indicators / Индикаторы статуса
Color / Цвет	Status / Статус	Ping / Пинг	Description / Описание

🟢 GREEN	ONLINE	< 35 ms	Good connection / Хорошее соединение

🔵 CYAN	FREEZE	35–60 ms	Minor delay / Небольшая задержка

🟡 YELLOW	SLEEP	60–300 ms	Significant delay / Значительная задержка

🔴 RED	OFFLINE	> 300 ms	Connection lost / Соединение потеряно



### Example Output / Пример вывода
[![pingC](https://raw.githubusercontent.com/blyamur/pingC/refs/heads/master/pingc.jpg)](https://github.com/blyamur/pingC)

### File Structure / Структура файлов
``` 
pingC/
├── pingC.py              # Main script / Основной скрипт
├── settings.xml          # Hosts configuration / Конфигурация хостов
├── error_logs.txt        # Error log (auto-created) / Лог ошибок (создаётся автоматически)
└── README.md            # This file / Этот файл
```

###  Requirements / Требования
```
Python 3.6+
Modules / Модули:
pythonping (for ping functionality / для пинга)
colorama (for colored output / для цветного вывода)
pyautogui (for Windows alerts / для оповещений в Windows)
```

###  Troubleshooting / Решение проблем

```
Problem: Script doesn't run / Скрипт не запускается
Solution: Make sure all dependencies are installed:
Решение: Убедитесь, что все зависимости установлены:
```
``` 
pip install pythonping colorama pyautogui
Problem: No ping results / Нет результатов пинга
Solution: Run as administrator on Windows
Решение: Запустите от имени администратора в Windows
```
```
Problem: settings.xml not found / settings.xml не найден
Solution: Create the file in the same directory as the script
Решение: Создайте файл в той же папке, что и скрипт
```

### Copyrights and Licenses
Not for commercial use.


### Did you find this useful?! | Вы нашли это  полезным ?!

Happy to hear that :) *If You want to help me, you can buy me a cup of coffee :coffee: ( [yoomoney](https://yoomoney.ru/to/41001158104834) or [ko-fi](https://ko-fi.com/monseg) )* 

> Рад это слышать :) Если вы хотите мне помочь, вы можете угостить меня чашечкой кофе 

*Thanks for reading :heart_eyes_cat:*
> Спасибо за чтение!


© 2025
