\# импорт разных библиотек необходимых для работы программы



from pathlib import Path

import random

import string

import time



\# переменная папки /opt/app и переменная файла log.txt

dir = Path("/opt/app") 

file = dir / "log.txt" 



\# создание папки /opt/app и создание файла log.txt в папке /opt/app



dir.mkdir(parents=True, exist\_ok=True) 

file.touch(exist\_ok=True) 



\# переменная строк



lines = string.ascii\_letters + string.digits 



\# цикл генерации строк длиной от 1 до 20



while True:

&#x20;   length = random.randint(1, 20)

&#x20;   line = "".join(random.choices(lines, a=length))

&#x20;   

&#x20;   # открытие файла на запись и добавление новых строк

&#x20;   

&#x20;   with open(file, 'a') as f:

&#x20;       f.write(line + "\\n")

&#x20;   

&#x20;   # временной интервал между генерацией строк

&#x20;   

&#x20;   time.sleep(17)

