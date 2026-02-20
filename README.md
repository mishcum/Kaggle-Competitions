## 📊 Kaggle Competitions Repository

Этот репозиторий содержит мои решения и эксперименты для различных соревнований на платформе Kaggle.
Каждая папка соответствует отдельному соревнованию.

## 🏆 Соревнования

| Соревнование | Задача | Тип задачи | Метод оценивания | Baseline | Baseline score | Итоговое решение | Итоговый score | Leaderbord | Методы |
| ------------ | ------ | ---------- | ---------------- | -------- | -------------- | ---------------- | -------------- | ---------- | ------ |
| [Spaceship Titanic](https://www.kaggle.com/competitions/spaceship-titanic) | Предсказать, какие пассажиры попадут в другое измерение | Бинарная классификация | Accuracy | Random Forest | 0.77 | LogisticRegression над тремя бустингами - CatBoost, XGB, LGBM | 0.80593 | 234 / 1693 | EDA, Feature Engineering, Ансамблирование |
| [Digit Recognizer](https://www.kaggle.com/competitions/digit-recognizer/overview) | Классификация цифр на изображении | Многклассовая классификация | Accuracy | Random Forest | 0.97 | CNN | 0.99003 | 359 / 940 | EDA, Data Augmentation |
| [House Prices - Advanced Regression Techniques](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques) | Предсказание цены дома | Регрессия | RMSE | Catboost | 0.12744 | Ridge над тремя бустингами - CatBoost, XGB, LGBM | 0.12305 | 491 / 5066 | EDA, Feature Engineering, Подбор гиперпараметров, Ансамблирование |
| Human Activity Recognition with Smartphones | Классификация активности, которую выполняет человек | Многоклассовая классификация | Accuracy | LogisticRegression | 0.825 | - | - | - | EDA, Data visualization |
| [Diamonds](https://www.kaggle.com/competitions/diamonds-ds-ft-2109/leaderboard?tab=public) | Предсказание стоимости бриллиантов | Регрессия | RMSE | LassoRegression | 1208.80042 | CatBoost | 521.00491 | After deadline | EDA, Feature Engineering, Отчистка данных, Подбор гиперпараметров |
| [Titanic - Machine Learning from Disaster](https://www.kaggle.com/competitions/titanic) | Предсказать, выжил ли человек на Титанике | Бинарная классификация | Accuracy | LogisticRegression | 0.75837 | XGBoost | 0.77033 | 9453 / 14831 | EDA, Feature Engineering |
| [Natural Language Processing with Disaster Tweets](https://www.kaggle.com/competitions/nlp-getting-started) | Предсказать, какие твиты о катастрофах, а какие нет | Бинарная классификация текстов | F1 | LogisticRegression | 0.78884 | twitter-roberta-base fine tuning | 0.82439 | 153 / 872 | EDA, Fine Tuning |
| [Dogs vs. Cats Redux: Kernels Edition](https://www.kaggle.com/competitions/dogs-vs-cats-redux-kernels-edition/overview) | Определить: кошка или собака на фото | Бинарная классификация | LogLoss | ResNet fine tuning | 0.06202 | ResNet fine tuning (calibrated) | 0.06130 | Unranked (after deadline) | Fine Tuning, Deep Learning |
| [LLM Classification Finetuning](https://www.kaggle.com/competitions/llm-classification-finetuning) | На основании промпта и ответов двух моделей определить, какая из моделей дала лучший ответ (возможна ничья) | Классификация | LogLoss | Bert-base fine tuning | 1.08338 | in progress | in_progress | 144 / 229 | NLP, Fine Tuning |
---

## 🛠️ Используемые технологии

* 🐍 Python 3.10+
* 📊 pandas, numpy, matplotlib, seaborn, plotly
* 🤖 scikit-learn, CatBoost, XGBoost, LightGBM, PyTorch, Transformers, Optuna

---

## 🧭 Подход к решению

Для большинства соревнований я использую общий пайплайн:
1. 📊 **EDA** — первичный анализ данных, поиск закономерностей, визуализация
2. 🧼 **Feature Engineering** — создание и отбор признаков
3. ⚡ **Baseline Model** — простая модель
4. 🧠 **Model Improvement** — бустинги, ансамбли, нейронки
5. 🧪 **Validation** — кросс-валидация, проверка стабильности
6. 🚀 **Submission** — сабмит в Kaggle и трекинг результатов

