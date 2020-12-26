# HADOOP
Проект создан для выполнения 1 лабораторной работы.


# Параметры системы
Python 2.7
Centos

# Запуск
Импортируем содержимое в hadoop-2.10.0
Запускаем сервисы hadoop, и выполняем код запуска bin/hadoop

```
bin/hadoop jar share/hadoop/tools/lib/hadoop-streaming-2.10.0.jar -D mapred.reduce.tasks=2 -D mapred.input.compress=true -D mapred.input.compression.codec=org.apache.hadoop.io.compress.SnappyCodec -D mapred.output.compress=true -D mapred.output.compression.codec=org.apache.hadoop.io.compress.SnappyCodec -file mapper.py -mapper mapper.py -file reducer.py -combiner reducer.py -file reducer.py -reducer reducer.py -input input/test.tar.gz -output 23
```

Запуск производится со следующими параметрами:
- reduce.tasks=2 - два reducerа
- mapred.input.compress=true - входные данные могут быть сжаты
- mapred.output.compression.codec=org.apache.hadoop.io.compress.SnappyCodec - выходные данные в snappy
- mappe.py - маппер
- combiner - комбайнер
- reducer - редьсер

# Результат
В ходе выполнения получаем файлы с максимальным словом в файле




