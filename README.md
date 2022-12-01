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
1) Поменял в economic strength с 1 на 10
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

Увеличение параметра strength привело к увеличению степени вознаграждения, а также повысило обучаемость модели.

2) Поменял num_epoch с 3 до 10 
Данные из консоли 
[INFO] Economic. Step: 5000. Time Elapsed: 42.273 s. No episode was completed since last summary. Training.

[INFO] Economic. Step: 10000. Time Elapsed: 67.037 s. Mean Reward: 0.000. Std of Reward: 1.000. Training. ELO: 1196.340.

[INFO] Economic. Step: 15000. Time Elapsed: 107.998 s. Mean Reward: 0.167. Std of Reward: 0.986. Training. ELO: 1191.519.

[INFO] Economic. Step: 20000. Time Elapsed: 129.559 s. No episode was completed since last summary. Training.

[INFO] Economic. Step: 25000. Time Elapsed: 157.050 s. Mean Reward: 0.167. Std of Reward: 0.986. Training. ELO: 1186.198.

[INFO] Economic. Step: 30000. Time Elapsed: 193.161 s. Mean Reward: 0.667. Std of Reward: 0.745. Training. ELO: 1182.795.

[INFO] Economic. Step: 35000. Time Elapsed: 250.326 s. No episode was completed since last summary. Training.

[INFO] Economic. Step: 40000. Time Elapsed: 294.855 s. Mean Reward: 0.500. Std of Reward: 0.866. Training. ELO: 1180.392.

Увеличение параметра num_epoch привело к увеличению количества опытов необходимых для обновления схемы обучения и не оказало существенного влияния на обучаемость модели.

3) Поменял epsilpon с 0.1 на 0.01
Данные консоли:
[INFO] Economic. Step: 5000. Time Elapsed: 73.559 s. No episode was completed since last summary. Training.

[INFO] Economic. Step: 10000. Time Elapsed: 94.626 s. Mean Reward: -0.333. Std of Reward: 0.943. Training. ELO: 1196.007.

[INFO] Economic. Step: 15000. Time Elapsed: 117.898 s. Mean Reward: 1.000. Std of Reward: 0.000. Training. ELO: 1192.019.

[INFO] Economic. Step: 20000. Time Elapsed: 140.573 s. No episode was completed since last summary. Training.

[INFO] Economic. Step: 25000. Time Elapsed: 164.051 s. Mean Reward: 1.000. Std of Reward: 0.000. Training. ELO: 1192.032.

[INFO] Economic. Step: 30000. Time Elapsed: 185.340 s. Mean Reward: 1.000. Std of Reward: 0.000. Training. ELO: 1192.044.

[INFO] Economic. Step: 35000. Time Elapsed: 207.775 s. No episode was completed since last summary. Training.

[INFO] Economic. Step: 40000. Time Elapsed: 229.698 s. Mean Reward: 1.000. Std of Reward: 0.000. Training. ELO: 1192.057.

Уменьшение параметра epsilon привело к уменьшению скорости изменения политики обучения и привело к увеличению скорости обучения

4) Поменял batch_size с 1024 на 2048

Данные консоли:
[INFO] Economic. Step: 5000. Time Elapsed: 43.582 s. No episode was completed since last summary. Training.

[INFO] Economic. Step: 10000. Time Elapsed: 71.032 s. Mean Reward: 0.000. Std of Reward: 1.000. Training. ELO: 1195.757.

[INFO] Economic. Step: 15000. Time Elapsed: 100.296 s. Mean Reward: 1.000. Std of Reward: 0.000. Training. ELO: 1194.019.

[INFO] Economic. Step: 20000. Time Elapsed: 121.376 s. No episode was completed since last summary. Training.

[INFO] Economic. Step: 25000. Time Elapsed: 143.708 s. Mean Reward: 1.000. Std of Reward: 0.000. Training. ELO: 1194.031.

[INFO] Economic. Step: 30000. Time Elapsed: 174.313 s. Mean Reward: 1.000. Std of Reward: 0.000. Training. ELO: 1194.044.

[INFO] Economic. Step: 35000. Time Elapsed: 195.152 s. No episode was completed since last summary. Training.

[INFO] Economic. Step: 40000. Time Elapsed: 215.962 s. Mean Reward: 1.000. Std of Reward: 0.000. Training. ELO: 1194.056

Увеличение параметра batch_size привело к увеличению попыток в одной итерации и положительно сказалось на динамике обучения модели

5) Поменял lambd с 0.95 на 0.5

Данные консоли:

[INFO] Economic. Step: 5000. Time Elapsed: 65.672 s. No episode was completed since last summary. Training.

[INFO] Economic. Step: 10000. Time Elapsed: 85.043 s. Mean Reward: 0.667. Std of Reward: 0.745. Training. ELO: 1198.923.

[INFO] Economic. Step: 15000. Time Elapsed: 107.166 s. Mean Reward: 0.500. Std of Reward: 0.866. Training. ELO: 1196.102.

[INFO] Economic. Step: 20000. Time Elapsed: 142.625 s. No episode was completed since last summary. Training.

[INFO] Economic. Step: 25000. Time Elapsed: 167.861 s. Mean Reward: 0.833. Std of Reward: 0.553. Training. ELO: 1194.864.

[INFO] Economic. Step: 30000. Time Elapsed: 187.189 s. Mean Reward: 0.500. Std of Reward: 0.866. Training. ELO: 1192.043.

[INFO] Economic. Step: 35000. Time Elapsed: 208.109 s. No episode was completed since last summary. Training.

[INFO] Economic. Step: 40000. Time Elapsed: 236.604 s. Mean Reward: 0.667. Std of Reward: 0.745. Training. ELO: 1189.473


Уменьшение параметра lambd не оказало положительного влияния на обучаемость модели


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
