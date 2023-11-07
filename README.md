# pcb-detection

## Описание
В данной работе предлагается использовать методы глубокого обучения для разспознавания компонентов, установленных на печатных платах. То есть, решается задачи детекции объектов.

Был собран датасет, состоящий из изображений одной печатной платы. В обучающей выборке 8 изображений, в тестовой - 4. На каждом изображении порядка 80 объектов. Датасет был размечен в Label Studio.

Классы в датасете:


* *R* - резистор
* *C* - конденсатор
* *A* - устройства и интегральные схемы
* *VD* - диод
* *RV* - подстроечный резистор

Использованные модели:
- Faster-RCNN
- RetinaNet
- YOLOv8m

## Используемые библиотеки
torch, torchvision, PIL, ultralytics, albumentations

## Итоги
Было обучено несколько моделей детекции, лучшими показателями обладает модель YOLOv8. Проект ещё находится на стадии разработки.

| <font size='5'>Модель</font> |  <font size='5'>MAP 50 | <font size='5'> MAP 50-95 |  <font size='5'>Время обработки на GPU|
|:--------:|:--------:|:--------:|:--------:|
|  <font size='3'>Faster-RCNN    | <font size='3'> 0.9868 | <font size='3'> 0.8173   |  <font size='3'>~ 125 мс  |
|   <font size='3'> RetinaNet    | <font size='3'>0.9979   |<font size='3'> 0.8713   |<font size='3'> ~ 130 мс  |
|   <font size='3'> YOLOv8    | <font size='3'>0.9950   |<font size='3'> 0.9080   |<font size='3'> ~ 37 мс  |


