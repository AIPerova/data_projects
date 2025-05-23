# Прогнозирование спроса на такси

## 🚖 Задача
Прогнозирование количества заказов такси на следующий час для оптимизации работы водителей

----

## 🔍 Данные
- Исторические данные о заказах в аэропортах
- Временной ряд с ресемплированием по 1 часу
- Тестовая выборка: 10% от исходных данных

----

## 🛠️ Моделирование

### Лучшая модель
```python
from catboost import CatBoostRegressor

best_model = CatBoostRegressor(
    depth=5,
    iterations=200,
    learning_rate=0.1,
    verbose=0
)
```
### Ключевые признаки:
 - lag_48 (сдвиг на 48 часов)
 - lag_1 (сдвиг на 1 час)

### 📊 Результаты
| Модель |	RMSE |	Соответствие критерию (<48) |
|---------|----------|-------------------|
| CatBoost	| 42	| ✅ |
| Prophet	| 45	| ✅ |
| RandomForest	| 47	| ✅ |
|LinearRegression |	53	| ❌ |

----

## 🚀 Рекомендации
Улучшение данных:
 - Добавить календарные признаки (праздники)
 - Учесть информацию о рейсах
   
Развитие модели:
 - Эксперименты с оконными статистиками
 - Добавление внешних данных (погода)
   
Операционные улучшения:
 - Система оповещения водителей за 2 часа
 - Динамическое ценообразование
