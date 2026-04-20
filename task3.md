# импорт разных библиотек необходимых для работы программы

from pathlib import Path
import random
import string
import time

# переменная папки /opt/app и переменная файла log.txt
dir = Path("/opt/app") 
file = dir / "log.txt" 

# создание папки /opt/app и создание файла log.txt в папке /opt/app

dir.mkdir(parents=True, exist_ok=True) 
file.touch(exist_ok=True) 

# переменная строк

lines = string.ascii_letters + string.digits 

# цикл генерации строк длиной от 1 до 20

while True:
    length = random.randint(1, 20)
    line = "".join(random.choices(lines, a=length))
    
    # открытие файла на запись и добавление новых строк
    
    with open(file, 'a') as f:
        f.write(line + "\n")
    
    # временной интервал между генерацией строк
    
    time.sleep(17)