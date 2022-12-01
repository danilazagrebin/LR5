# LR5
# АНАЛИЗ ДАННЫХ И ИСКУССТВЕННЫЙ ИНТЕЛЛЕКТ [in GameDev]
Отчет по лабораторной работе #5 выполнил:
- Загребин Данила Павлович
- РИ212702
Отметка о выполнении заданий (заполняется студентом):

| Задание | Выполнение | Баллы |
| ------ | ------ | ------ |
| Задание 1 | * | 60 |
| Задание 2 | * | 20 |
| Задание 3 | * | 20 |

знак "*" - задание выполнено; знак "#" - задание не выполнено;

Работу проверили:
- к.т.н., доцент Денисов Д.В.
- к.э.н., доцент Панов М.А.
- ст. преп., Фадеев В.О.

[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

Структура отчета

- Данные о работе: название работы, фио, группа, выполненные задания.
- Цель работы.
- Задание 1.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Задание 2.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Задание 3.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Выводы.
- ✨Magic ✨

## Цель работы
Научиться обучать ML-Agent на примере интеграции экономической системы в Unity проект

## Задание 1
### Измените параметры файла. yaml-агента и определить какие параметры и 
как влияют на обучение модели.

Ход работы:
- В созданном Unity-проекте были внесены изменения в файл yaml-агента:
Поменял в economic strength с 1 на 10
Данные из консоли
[INFO] Economic. Step: 5000. Time Elapsed: 75.437 s. No episode was completed since last summary. Training.
[INFO] Economic. Step: 10000. Time Elapsed: 95.690 s. Mean Reward: 1.000. Std of Reward: 0.000. Training. ELO: 1200.006.
[INFO] Economic. Step: 15000. Time Elapsed: 124.619 s. Mean Reward: 1.000. Std of Reward: 0.000. Training. ELO: 1200.018.
[INFO] Economic. Step: 20000. Time Elapsed: 154.822 s. No episode was completed since last summary. Training.
[INFO] Economic. Step: 25000. Time Elapsed: 177.429 s. Mean Reward: 1.000. Std of Reward: 0.000. Training. ELO: 1200.030.
[INFO] Economic. Step: 30000. Time Elapsed: 197.914 s. Mean Reward: 0.833. Std of Reward: 0.553. Training. ELO: 1199.292.
[INFO] Economic. Step: 35000. Time Elapsed: 220.908 s. No episode was completed since last summary. Training.
[INFO] Economic. Step: 40000. Time Elapsed: 255.577 s. Mean Reward: 1.000. Std of Reward: 0.000. Training. ELO: 1199.055.
[INFO] Economic. Step: 45000. Time Elapsed: 282.403 s. Mean Reward: 1.000. Std of Reward: 0.000. Training. ELO: 1199.067.



## Задание 2
### Построить графики зависимости количества эпох от ошибки обучения

![image](https://user-images.githubusercontent.com/114522298/204098701-8a099f8d-a076-4b9a-963a-972603aca33f.png)

Количество эпох обучения зависит от сложности логической операции, то есть чем сложнее задача, тем дольше нужно обучать модель, чтобы обработать как можнно больше вариантов решения. 

## Выводы

В лабораторной работе я познакомился с такой математической моделью как перцептрон, также я научился реализвывать его работу в среде Unity
на примере логических операторов: OR, AND, NAND, XOR.
| Plugin | README |
| ------ | ------ |
| Dropbox | [plugins/dropbox/README.md][PlDb] |
| GitHub | [plugins/github/README.md][PlGh] |
| Google Drive | [plugins/googledrive/README.md][PlGd] |
| OneDrive | [plugins/onedrive/README.md][PlOd] |
| Medium | [plugins/medium/README.md][PlMe] |
| Google Analytics | [plugins/googleanalytics/README.md][PlGa] |

## Powered by

**BigDigital Team: Denisov | Fadeev | Panov**
