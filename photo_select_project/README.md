# Поиск изображений по текстовому запросу

## 🎯 Цель проекта
Разработка модели для оценки соответствия изображений и текстов (0-1)

## 📊 Результаты
| Модель	| RMSE |	Время предсказания |
|---------|----------|-------------------|
| MLP	| 0.31	| 12ms |
| RandomForest |	0.35	| 8ms |
| CLIP (финальная) |	0.18 |	15ms |

## 🚀 Итоговое решение
Использована предобученная модель CLIP:
Точность: 82%
Среднее время обработки: 0.15 сек
Поддерживает 100+ языков

## 💡 Дальнейшее развитие
Увеличение обучающей выборки
Тонкая настройка CLIP
Оптимизация для мобильных устройств
