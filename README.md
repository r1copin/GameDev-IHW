# GameDev-IHW

Кадыкова Татьяна Алексеевна

## Комментарий
После отправки формы обнаружила, что я перешла порог выделенной памяти на большие файлы на github из-за неиспользованных в самой игре текстур и объектов, 
и в результате у меня не получилось дозалить нужные изменения. Попыталась исправить ситуацию, стерев коммит и загрузив только нужные файлы, но затея не удалась.
Прошу прощения, что так случилось и файлы игры не в репозитории, но вот ссылка на гугл диск с архивом:

https://drive.google.com/file/d/1Y11I0hmzAiij7n3qswP9a8Vp3u-DBtIR/view?usp=sharing

## Документация

### Генерация комнат
Комнаты имеют фиксированную структуру коридоров - змейка. 
В самих коридорах случайно генерируются ловушки из 3х видов на фиксированных позициях в коридоре (каждые 200ед, 4 ловушки на коридор).
Виды ловушек: двигающийся огненный шторм (динамическая), лазер из стены (статическая, высота лазера случайна), стена из мигающих лазеров (лазеры исчезают на некоторое время).
Двери открываются только с одной стороны, после прохода через дверь вернуться обратно не получится

### Отличия простой и сложной комнат
Коридоры сложной комнаты уже, площадь самой комнаты одинакова с простой. В простой комнате 4 коридора, в сложной 5. 
Скорость мигания стены из лазеров увеличивается (в простой каждые 2 секунды меняется состояние, в сложной каждую секунду), 
также статичные лазеры могут генерироваться немного выше, чем в простых). Сложная комната помечена капустой сверху двери.
В сложной комнате после 2 коридора есть проход в комнату с от 3 до 7 кочанов капусты, восстанавливающих здоровье.

### Дополнительно
Были взяты бесплатные паки для модели капусты, огненного шторма и магического кольца (используется при переходе между комнатами)
