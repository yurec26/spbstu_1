
### Домашняя работа 1.
___

#### 1. Процессор инструментальной платформы.

1) Модель процессора: **AMD Ryzen 7 5700U with Radeon Graphics**.
2)  Технический процесс, по которому изготовлен процессор: **7-nanometer process**.
3)  Архитектура: **x86-64** (corrected).
4)  Микроархитектура: **Zen 2 microarchitecture**. 
5)  Кодовое имя микроархитектуры: **Lucienne**.
6)  Последний расширенный набор инструкций, поддерживаемый процессором: **_AVX2_.** (corrected)
7)  Число ядер:
	1. Производительных: **8 шт**.
	2. Число потоков обрабатываемых на производи-
           тельных ядрах, в лучшем случае: **16 (по 2 потока на ядро).**
	3. Эффективных: **NIL**.
	4. число потоков, обрабатываемых на эффективных
	   ядрах, в лучшем случае: **N/A**.
8)  Объём СОЗУ (кэш-памяти) каждого уровня:
	  - Level 1: **512 KiB (64 KiB/core)**: 
		   +  L1l$ : 256 KiB (8x32 KiB),
		   +  L1D$ : 256 KiB (8x32 KiB),
	  - Level 2: **4 MiB (512 KiB/core)**.
	  - Level 3: **8 MiB**.
9)  Cвязность кэш-памяти последнего уровня (общая/не общая
    для какого числа ядер): **не общая**.  (corrected)
10)  Диаграмма всех уровней кэш-памяти:    
 
![report.jpg](https://raw.githubusercontent.com/yurec26/spbstu_1/master/%D1%81%D0%B2%D1%8F%D0%B7%D0%BD%D0%BE%D1%81%D1%82%D1%8C%20%D0%BA%D1%8D%D1%88%D0%B0.jpg)


11)  Процессор – чистый / не чистый многоядерный процессор? : **не чистый**. (corrected)
12)  Объём ОЗУ : **16 GiB**.
13) - Число каналов ОЗУ и на какой объём ОЗУ оно рас-
    пространяется : **2(dual channel)**; 
    - Максимальная конфигурация ОЗУ: **2*32 GiB**.
___

#### 3. Название установленного дистрибутива, его версия: 
        Debian GNU/Linux 12 (bookworm).
#### 4. Используемый менеджер окон: 
        i3.
___

#### 5. Сложности, возникшие при создании инструментальной платформы, и способы их преодоления:

1. *Проблема:* не удавалось настроить быструю смену языка ввода рус-англ.
   *Решение:* выяснилось, что утилиты ibus и setxkbmap конфликтуют в своих конфигурационных файлах. После удаления утилиты ibus проблема решилась.

2.  *Проблема:* Ряд аналогичных по своей сути проблем, связанных с настройкой окружения оконного менеджера i3: привязка клавиш повышения/понижения громкости/яркости и настройка и функциональности, добавление модулей в конфигурационный файл polybar, настройка клавиши PrintScreen и т.д.
   *Решение:* все подобные проблемы решались примерно следующим алгоритмом: 
    -  вызов утилиты xev для четкого определения названия клавиши в системе.
    -  загрузка нужной утилиты, отвечающей за необходимую функциональность.
    -  определение нужной команды утилиты для исполнения в терминале.
    -  добавление в конфигурационный файл `~/.config/i3/config` необходимой строчки для вызыва утилиты при включении системы или привязки ранее найденной команды к нужной клавише.


