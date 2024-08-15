# Age Prediction Model for Crabs using Stacking Regressor

This project demonstrates a machine learning pipeline for predicting the age of crabs using various regression models, feature engineering, and a stacking regressor to enhance performance. The dataset contains multiple features related to the physical characteristics of crabs.

## Project Structure

- `train.csv`: Training dataset with labeled data.
- `test.csv`: Test dataset without labels.
- `my_submission.csv`: Final predictions on the test dataset.
- `README.md`: Project documentation.

## Libraries Used

- `pandas`
- `scikit-learn`
- `numpy`
- `warnings`

## Feature Engineering

The following new features were engineered:

- **Weight to Length Ratio**: `Weight / Length`
- **Volume**: `Length * Diameter * Height`
- **Shucked Weight Ratio**: `Shucked Weight / Weight`
- **Shell Weight Ratio**: `Shell Weight / Weight`
- **Shell Weight to Length Ratio**: `Shell Weight / Length`
- **Shell Weight to Diameter Ratio**: `Shell Weight / Diameter`
- **Total Weight Components**: `Shucked Weight + Viscera Weight + Shell Weight`
- **Shucked to Shell Weight Ratio**: `Shucked Weight / Shell Weight`
- **Viscera to Shell Weight Ratio**: `Viscera Weight / Shell Weight`

## Model Training

The models used in this project include:

1. **Ridge Regression**
2. **Lasso Regression**
3. **Huber Regressor**
4. **Theil-Sen Regressor**
5. **Linear Regression**

### Stacking Regressor

A stacking regressor was implemented with the models mentioned above as base estimators and `HuberRegressor` as the final estimator.

## Pipeline Details

Each model was configured with the following pipeline:

- **Robust Scaling**: To handle outliers.
- **Polynomial Features**: To capture non-linear relationships.

### Training and Evaluation

- The models were trained using the training dataset.
- The stacking regressor was evaluated using Mean Absolute Error (MAE) on a split validation set.
- The final model was trained on the entire training dataset and used to predict the `Age` in the test dataset.

## Submission

The final predictions are saved in `my_submission.csv`, which can be directly submitted to the competition or used for further analysis.

## How to Use

1. Clone the repository.
2. Place the `train.csv` and `test.csv` files in the root directory.
3. Run the Python script to generate predictions.
4. The predictions will be saved in `my_submission.csv`.

## Acknowledgments

- The dataset was provided for the purpose of predicting the age of crabs.
- Special thanks to the scikit-learn library for providing the tools to build this model.



# ################################################################################################################################################



# Модель предсказания возраста крабов с использованием стекинг-регрессора

Этот проект демонстрирует пайплайн машинного обучения для предсказания возраста крабов с использованием различных регрессионных моделей, инженерии признаков и стекинг-регрессора для улучшения точности. Датасет включает множество характеристик, связанных с физическими параметрами крабов.

## Структура проекта

- `train.csv`: Обучающий набор данных с метками.
- `test.csv`: Тестовый набор данных без меток.
- `my_submission.csv`: Финальные предсказания на тестовом наборе данных.
- `README.md`: Документация проекта.

## Используемые библиотеки

- `pandas`
- `scikit-learn`
- `numpy`
- `warnings`

## Инженерия признаков

Были созданы следующие новые признаки:

- **Соотношение веса к длине**: `Weight / Length`
- **Объем**: `Length * Diameter * Height`
- **Соотношение очищенного веса**: `Shucked Weight / Weight`
- **Соотношение веса раковины**: `Shell Weight / Weight`
- **Соотношение веса раковины к длине**: `Shell Weight / Length`
- **Соотношение веса раковины к диаметру**: `Shell Weight / Diameter`
- **Общий вес компонентов**: `Shucked Weight + Viscera Weight + Shell Weight`
- **Соотношение очищенного веса к весу раковины**: `Shucked Weight / Shell Weight`
- **Соотношение веса висцеральных органов к весу раковины**: `Viscera Weight / Shell Weight`

## Обучение моделей

В проекте использовались следующие модели:

1. **Ridge Regression**
2. **Lasso Regression**
3. **Huber Regressor**
4. **Theil-Sen Regressor**
5. **Linear Regression**

### Стекинг-регрессор

Был реализован стекинг-регрессор с указанными выше моделями в качестве базовых оценщиков и `HuberRegressor` в качестве финальной модели.

## Детали пайплайна

Каждая модель была настроена с использованием следующего пайплайна:

- **Robust Scaling**: Для обработки выбросов.
- **Полиномиальные признаки**: Для учета нелинейных зависимостей.

### Обучение и оценка

- Модели обучались на обучающем наборе данных.
- Стекинг-регрессор оценивался с использованием метрики Средней абсолютной ошибки (MAE) на раздельном валидационном наборе.
- Финальная модель была обучена на всем обучающем наборе данных и использована для предсказания возраста на тестовом наборе данных.

## Отправка результатов

Финальные предсказания сохраняются в `my_submission.csv`, который может быть непосредственно отправлен на соревнование или использован для дальнейшего анализа.

## Как использовать

1. Склонируйте репозиторий.
2. Разместите файлы `train.csv` и `test.csv` в корневом каталоге.
3. Запустите Python-скрипт для генерации предсказаний.
4. Предсказания будут сохранены в `my_submission.csv`.

## Благодарности

- Датасет был предоставлен для целей предсказания возраста крабов.
- Особая благодарность библиотеке scikit-learn за предоставленные инструменты для создания этой модели.



# ################################################################################################################################################



# Qisqichbaqalarning Yoshini Prognoz Qilish Modeli Stacking Regressor bilan

Ushbu loyiha qisqichbaqalarning yoshini prognoz qilish uchun turli regressiya modellari, xususiyatlar muhandisligi va stacking regressordan foydalangan holda oqilmli ishlov berish qatorini namoyish etadi. Ma'lumotlar to'plami qisqichbaqalarning fizik xususiyatlariga oid bir nechta ko'rsatkichlarni o'z ichiga oladi.

## Loyiha Tarkibi

- `train.csv`: Belgilangan ma'lumotlar bilan o'quv ma'lumotlar to'plami.
- `test.csv`: Belgilangan ma'lumotlarsiz test ma'lumotlar to'plami.
- `my_submission.csv`: Test ma'lumotlar to'plamidagi yakuniy prognozlar.
- `README.md`: Loyiha hujjati.

## Foydalanilgan Kutubxonalar

- `pandas`
- `scikit-learn`
- `numpy`
- `warnings`

## Xususiyatlar Muhandisligi

Quyidagi yangi xususiyatlar yaratildi:

- **Og'irlik va uzunlik nisbati**: `Weight / Length`
- **Hajm**: `Length * Diameter * Height`
- **Tozalangan vazn nisbati**: `Shucked Weight / Weight`
- **Qobiq og'irligi nisbati**: `Shell Weight / Weight`
- **Qobiq og'irligi va uzunlik nisbati**: `Shell Weight / Length`
- **Qobiq og'irligi va diametr nisbati**: `Shell Weight / Diameter`
- **Umumiy komponentlar og'irligi**: `Shucked Weight + Viscera Weight + Shell Weight`
- **Tozalangan og'irlik va qobiq og'irligi nisbati**: `Shucked Weight / Shell Weight`
- **Ichak va qobiq og'irligi nisbati**: `Viscera Weight / Shell Weight`

## Modellarni O'qitish

Loyihada quyidagi modellar ishlatilgan:

1. **Ridge Regression**
2. **Lasso Regression**
3. **Huber Regressor**
4. **Theil-Sen Regressor**
5. **Linear Regression**

### Stacking Regressor

Yuqorida ko'rsatilgan modellar asosiy baholovchi sifatida va `HuberRegressor` yakuniy baholovchi sifatida ishlatilgan stacking regressori amalga oshirildi.

## Oqimli Tafsilotlar

Har bir model quyidagi oqim bilan sozlangan:

- **Robust Scaling**: Outlierlarni boshqarish uchun.
- **Polinomial Xususiyatlar**: Nolin ravishdagi munosabatlarni aniqlash uchun.

### O'qitish va Baholash

- Modellar o'quv ma'lumotlar to'plamidan foydalangan holda o'qitildi.
- Stacking regressor bo'linmagan validatsiya to'plamida O'rtacha Mutlaq Xato (MAE) ko'rsatkichi yordamida baholandi.
- Yakuniy model butun o'quv ma'lumotlar to'plamida o'qitilib, test ma'lumotlar to'plamidagi `Yosh`ni prognoz qilish uchun ishlatildi.

## Natijalarni Yuborish

Yakuniy prognozlar `my_submission.csv` faylida saqlanadi, bu faylni to'g'ridan-to'g'ri musobaqaga yuborish yoki qo'shimcha tahlil uchun ishlatish mumkin.

## Qanday Foydalanish

1. Repozitoriyani klonlang.
2. `train.csv` va `test.csv` fayllarini ildiz katalogiga joylashtiring.
3. Prognozlarni yaratish uchun Python skriptini ishga tushiring.
4. Prognozlar `my_submission.csv` faylida saqlanadi.

## Minnatdorchilik

- Ma'lumotlar to'plami qisqichbaqalarning yoshini prognoz qilish maqsadida taqdim etilgan.
- Ushbu modelni yaratishda foydalangan vositalar uchun scikit-learn kutubxonasiga maxsus minnatdorchilik bildiramiz.
