# В работе реализован однослойный линейный классификатор - перцептрон. Для начала необходимо установить библиотеки из папки requirements.txt
# Реализованы следующие флаги при запуске: +1
# usage: ft_perceptron.py [-h] [-t] [-p] [--plot] [--valid-size VALID_SIZE] [-lr LEARNING_RATE] [-e EPOCHS]
#                         [--batch-size BATCH_SIZE] [--train-path TRAIN_PATH] [--test-path TEST_PATH]
# optional arguments:
  -h, --help            show this help message and exit
  -t, --train           train mode
  -p, --predict         predict mode
  --plot                visualization
  --valid-size VALID_SIZE
                        split validation size (0-1)
  -lr LEARNING_RATE, --learning-rate LEARNING_RATE
  -e EPOCHS, --epochs EPOCHS
                        number epochs
  --batch-size BATCH_SIZE
  --train-path TRAIN_PATH, --train-filename TRAIN_PATH
                        train dataset filename
  --test-path TEST_PATH, --test-filename TEST_PATH
                        test dataset filename
Проект полностью логируется в режимах обучения и тестирования. 
Также реализован режим отображения изменения loss во время обучения. +1
Также во время обучения можно остановить процесс, что позволит сохранить модель с текущими весами. То есть это остановит процесс обучения, но при этом не сломает саму модель. +1
Можно передать в аргументах количество эпох для обучения, также задать learning_rate, и  batch_size, а также размер датасета для вадидации valid_size. +1

0. Создан pull request c полным описанием проделанной работы. +1
1. Сделан отчет по каждому пункту из задания. +1
2. Проведен EDA анализ. Ноутбук лежит в папке ноутбукс. Также реализована программа по формированию отчета в pdf формате. +1
Запускать под средой в папке scripts - python3 gen_eda_report.py или ./eda.sh +1
Отчет сохранится в папку pics
3. Написана функция/класс для тренировки модели, вызов оформлен как утилита командной строки, записана в readme инструкцию по запуску
Создана функция для тренировки модели train. Вызов осуществляется следующей командой:
python3 ft_perceptron.py или в корне ./train.sh +3
4. Написана функция/класс predict (вызов оформлен как утилита командной строки), которая примет на вход артефакт/ы от обучения, тестовую выборку (без меток) и запишет предикт по заданному пути, инструкция по вызову записана в readme
Создана функция для тестирования модели predict. Вызов осуществляется следующей командой:
python3 ft_perceptron.py --predict или в корне ./test.sh +3
5. Проект имеет модульную структуру +2
6. Использованы логгеры. Все процессы логируются в файл file.log +2
# 7. ------ Написаны тесты на отдельные модули и на прогон обучения и predict (3 балла)
# 8. ------ Для тестов генерируются синтетические данные, приближенные к реальным (2 балла)
9. Обучение модели конфигурируется с помощью конфигов в json или yaml, закоммитьте как минимум 2 корректные конфигурации, с помощью которых можно обучить модель (разные модели, стратегии split, preprocessing)
Json файл с весами и pkl модедью загружается в папку data в файл в папке data model.json. +3 
# 10. ----- Используются датаклассы для сущностей из конфига, а не голые dict (2 балла)
# 11. ----- Напишите кастомный трансформер и протестируйте его (3 балла) https://towardsdatascience.com/pipelines-custom-transformers-in-scikit-learn-the-step-by-step-guide-with-python-code-4a7d9b068156
# 12. ----- В проекте зафиксированы все зависимости (1 балл)
# 13. ----- Настроен CI для прогона тестов, линтера на основе github actions (3 балла). Пример с пары: https://github.com/demo-ml-cicd/ml-python-package
14. Залогируйте метрики
Метрики логируюся в файл file.log +1


Итого с учетом дополнительных фитч, которые прикручены в проекте, я насчитал 21 балл
