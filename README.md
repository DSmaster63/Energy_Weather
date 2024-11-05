# Прогнозирование потребляемой энергии в зависимости от погоды
Человечество для комфортной жизни потребляет значительное количество энергии, причем оно может значительно варьироваться от изменения климатических условий в регионе.
________

**Описание данных:** В обучающей выборке представлены показатели прогноза погоды и факта на определенный диапазон дат (по часам). В тестовой выборке представлен такой же набор параметров, но 
на даты, идущие следом после последней даты обучающей выборки.    
________

**Задача:** Создать модель машинного обучения, которая предскажет потребление энергии в зависимости от показателей погоды и ее прогноза. 
________

**Цель:** С помощью модели машинного обучения необходимо прогнозировать энергопотребление региона в зависимости от имеющихся данных о погоде и прошлого энергопотребления 
________

**Используемые инструменты:**
* функции библиотеки Pandas;
* графики, гистограммы и тепловые карты, доступные в библиотеке matplotlib и seaborn;
* ресемплинг (resample), анализ по тренду, сезонности (statsmodels.tsa.seasonal.seasonal_decompose) и скользящему среднему(rolling);
* функции и модели библиотеки sklearn для работы с данными и регрессией (train_test_split, DecisionTreeRegressor, RandomForestRegressor, LinearRegression, DummyRegressor).
  В данной версии проекта показана работа только DecisionTreeRegressor, как наилучшей из перечисленных, исходя из предварительных версий;
* бустинговая модель lgbm. В данной версии проекта показана работа только lgbm, так как catboost показал результаты хуже в предварительных версиях;
* подбор оптимальных гиперпараметров моделей с помощью RandomizedSearchCV;
* построение диаграммы важности признаков.
________

**Полученные выводы:**
* MAE тестовой выборки составил 137.2, MAPE - 0.013;
* По графикам сравнения факта и прогноза четко наблюдается соблюдение сезонности моделью.