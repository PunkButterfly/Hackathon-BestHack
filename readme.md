# Хакатон BestHack 2022

В этом репозитории описана вся исследовательская работа, которую мы провели в рамках хакатона BestHack 2022 от МГТУ в составе команды **punk_butterfly**.

## Задание от команды BestHack

На выбор было две [задачи](https://github.com/PunkButterfly/Hackathon-BestHack/blob/master/%D0%97%D0%B0%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5.pdf). Нам понравилась идея задания №2, поэтому было решено браться за нее.

### Задание

Необходимо решить одну из задач «Цифровой
реанимации». В представленном датасете имеются медицинские параметры
пациентов, больных раком. Необходимо классифицировать на основе этих
данных – пациент жив или погиб. 

Для этого задания заранее подготовлен [baseline](https://github.com/PunkButterfly/Hackathon-BestHack/blob/master/Baseline.ipynb) с точностью 50%.

### Сложности, с которыми предстоит столкнуться

* Медицинские данные полны терминологии, которую необходимо изучить
для проработки вопроса;
* Низкая корреляция данных с таргетом, возможно, придется создавать новые
фичи;
* Признаков (фич) много, необходимо выбрать те, которые способны дать
максимальный результат.

### Данные к задаче:

* [Датасет](https://docs.google.com/spreadsheets/d/1VwH563kjcQmE3mYbplnnrnKcSY7xyLA7/edit?usp=sharing&ouid=112656509446736153199&rtpof=true&sd=true) с размеченными таргетами, состоящий из 259 записей (пациентов);
* [Датасет](https://docs.google.com/spreadsheets/d/1wAWWCQr5AvIpSkBbUAghzZiZI8RCidlI/edit?usp=sharing&ouid=112656509446736153199&rtpof=true&sd=true) из 112 записей, которые необходимо предсказать.

> Качество модели будет оцениваться по метрике __balanced accuracy__.

## Наши результаты

Последовательность наших действий подробно описана в итоговом [ноутбуке](https://github.com/PunkButterfly/Hackathon-BestHack/blob/master/Data_analysis.ipynb), состоящем из выбранных нами лучших подходов. К сожалению, мы ошиблись, когда решили использовать некую ~~ф??гню~~ эвристику, вместо методов кластеризации. Данный подход на private выборке дал качество всего 0,67, из-за чего мы не прошли в финал. Но задание было очень увлекательным и веселым :)

## Навигация по файлам
* [Задание](https://github.com/PunkButterfly/Hackathon-BestHack/blob/master/%D0%97%D0%B0%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5.pdf) - формулировка задачи от организаторов хакатона;
* [Data_analysis](https://github.com/PunkButterfly/Hackathon-BestHack/blob/master/Data_analysis.ipynb) - ноутбук с исследованием данных и используемых моделей (все подробно описано);
* [Prediction](https://github.com/PunkButterfly/Hackathon-BestHack/blob/master/Prediction.ipynb) - ноутбук для предикта;
> Чтобы запустить, нужно удалить первую ячейку (она для подключения к гугл диску), и поменять путь до файлов в третьей ячейке.
Результатом работы программы будет файл __Result.csv__.
* [Result.csv](https://github.com/PunkButterfly/Hackathon-BestHack/blob/master/Result.csv) - файл с предиктами для Test_unlabled;
* [Презентация решения](https://github.com/PunkButterfly/Hackathon-BestHack/blob/master/%D0%9F%D1%80%D0%B5%D0%B7%D0%B5%D0%BD%D1%82%D0%B0%D1%86%D0%B8%D1%8F%20%D1%80%D0%B5%D1%88%D0%B5%D0%BD%D0%B8%D1%8F.pdf) - краткое описание проделанной работы;
* [Baseline](https://github.com/PunkButterfly/Hackathon-BestHack/blob/master/Baseline.ipynb) - решение, предложенное организаторами.
