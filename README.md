# Проект: Аналитическая платформа для мониторинга COVID-19

## Описание
Этот проект предназначен для анализа рентгеновских снимков пациентов с диагнозами COVID-19, пневмонии и других заболеваний.

## Технологии
- Hadoop (HDFS)
- Apache Spark
- PySpark
- Dash (визуализация)
- Docker

## Установка
1. Запустите контейнеры: `docker-compose up -d`
2. Загрузите датасет covid-chestxray-dataset-master/`
3. Добавить файлы шрифта в рабочую папку (DBproject)4. 
5. Запустите Python-ячейки по порядку

## Необходимые права:
1. Создать каталоги для данных пользователей
hdfs dfs -mkdir -p /user/jovyan/covid_dataset/images
hdfs dfs -mkdir -p /user/jovyan/covid_dataset/metadata
hdfs dfs -mkdir -p /user/jovyan/covid_dataset/processed

2. Установить владельца каталогов на пользователя jovyan
hdfs dfs -chown -R jovyan:jovyan /user/jovyan/covid_dataset

3. Установить права доступа 775 (rwxrwxr-x) рекурсивно
hdfs dfs -chmod -R 775 /user/jovyan/covid_dataset

4. Единожды установить максимальные права для тестирования (возможно, позже уменьшите)
hdfs dfs -chmod -R 777 /user/jovyan/covid_dataset

5. Проверить наличие каталога /user/hive (скорее всего отсутствует)
hdfs dfs -ls /user/hive

6. Проверить наличие каталога /user/hive/warehouse
hdfs dfs -ls /user/hive/warehouse

7. Создать каталог warehouse в нужном месте, согласно настройкам Spark
hdfs dfs -mkdir -p /user/jovyan/warehouse

8. Установить владельца на jovyan
hdfs dfs -chown -R jovyan:jovyan /user/jovyan/warehouse

9. Установить права доступа 775 для warehouse
hdfs dfs -chmod -R 775 /user/jovyan/warehouse


## Структура
- DBHW.ipynb
- docker-compose.yml
- LiberationSans.ttf Для вывода отчета на русском языке
-/home/user/DBproject/
