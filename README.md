# Описание репозитория

## Обо мне
Привет! Меня зовут Кузнецова Екатерина. Я окончила МГТУ им. Баумана по направлению Прикладная математика с
красным дипломом и активно развиваюсь в сфере Data Science. 
Этот репозиторий создан для демонстрации моих проектов, и я буду рада обратной связи или вопросам! 
# Проект: [ Кластеризация торговых точек ](https://github.com/keatrean/projects/blob/master/clustering_project/main_code.ipynb)
В этом коммерческом проекте я решала задачу кластеризации торговых точек компании, 
занимающейся производстовом и розничной дистрибьюцией продуктов питания. 
Основная цель заключалась в разделении точек на группы по структуре спроса на товары.

**Цель:** Создание групп торговых точек с похожими характеристиками спроса, чтобы облегчить анализ и 
улучшить маркетинговые стратегии.

**Процесс:** Проект не включает детального обоснования всех принятых решений, однако описывает основные этапы и дает общее представление о
процессе кластеризации.

**Используемые технологии и инструменты**
Python: Основной язык разработки.
Библиотеки: scikit-learn для алгоритмов кластеризации, 
pandas для работы с данными, matplotlib и seaborn для визуализации.

# swearwords_detection
# Проект: [ Классификация текста для обнаружения нецензурной лексики ](https://github.com/keatrean/projects/blob/master/swearwords_detection.ipynb)

**Notebook**: `swearwords_detection.ipynb` - код для обучения модели бинарной классификации текста. Модель основана на дообученной модели `rubert-base-cased` с использованием библиотеки Hugging Face.


## Содержание

- [Обзор проекта](#обзор-проекта)
- [Данные](#данные)
- [Модель](#модель)
- [Использование](#использование)



## Обзор проекта

Цель проекта — построить классификатор текста, способный определять, содержит ли текст нецензурную лексику. Задача бинарной классификации:
- `1`: Текст содержит нецензурную лексику.
- `0`: Текст не содержит нецензурной лексики.

Модель дообучена на предобученной модели `rubert-base-cased` от Hugging Face. Процесс дообучения использует библиотеку `transformers`.

## Данные

- **train.csv**: Датасет для обучения модели, содержащий примеры текста с метками, где каждый пример помечен как содержащий или не содержащий нецензурную лексику. Файл включает следующие столбцы:
  - `ID`: Уникальный идентификатор записи.
  - `text`: Текст отзыва или комментария.
  - `label`: Бинарная метка, указывающая, содержит ли текст нецензурную лексику (0 — нет, 1 — есть).

- **test.csv**: Тестовый датасет, для которого модель будет предсказывать наличие нецензурной лексики.
## Модель

- **Model**: [Hugging Face Model Hub]
- (no links due to NDA).
 
## Использование 
```python
from transformers import AutoModelForSequenceClassification, AutoTokenizer

model = AutoModelForSequenceClassification.from_pretrained("")
tokenizer = AutoTokenizer.from_pretrained("")
```

# swearwords_extraction
#  Проект: [ Извлечение нецензурной лексики из текстов ](https://github.com/keatrean/projects/blob/master/get_swearwords.ipynb)
Цель проекта — построить модель, определяющую нецензурную лексику в текстах отзывов/комментариев. На вход получает строку с текстом, на выходе - строка с нецензурными словами, перечисленными через запятую, с маленькой буквы, в алфавитном порядке.

**Notebook**: `get_swearwords.ipynb` - код для обучения модели  классификации токенов и решения задачи NER. Модель основана на дообученной модели `rubert-base-cased-conversational` с использованием библиотеки Hugging Face. В начале строки проходят предварительную обработку при помощи регулярных выражений.


