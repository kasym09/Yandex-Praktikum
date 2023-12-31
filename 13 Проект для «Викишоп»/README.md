https://nbviewer.org/github/kasym09/Yandex-Praktikum/blob/main/13%20%D0%9F%D1%80%D0%BE%D0%B5%D0%BA%D1%82%20%D0%B4%D0%BB%D1%8F%20%C2%AB%D0%92%D0%B8%D0%BA%D0%B8%D1%88%D0%BE%D0%BF%C2%BB/13%20%D0%9F%D1%80%D0%BE%D0%B5%D0%BA%D1%82%20%D0%B4%D0%BB%D1%8F%20%C2%AB%D0%92%D0%B8%D0%BA%D0%B8%D1%88%D0%BE%D0%BF%C2%BB.ipynb
# Проект для «Викишоп»

# Описание проекта
Интернет-магазин «Викишоп» запускает новый сервис. Теперь пользователи могут редактировать и дополнять описания товаров, как в вики-сообществах. То есть клиенты предлагают свои правки и комментируют изменения других. Магазину нужен инструмент, который будет искать токсичные комментарии и отправлять их на модерацию. 
Обучите модель классифицировать комментарии на позитивные и негативные. В вашем распоряжении набор данных с разметкой о токсичности правок.
Постройте модель со значением метрики качества F1 не меньше 0.75. 

## Выводы
Для исследования интернет-магазина "Викишоп" был проведен анализ, который выявил, что 90% записей не содержат токсичного контента. Мы также выполнили предварительную обработку текста с помощью регулярных выражений и подготовили данные для последующего анализа. В дальнейшем, мы выбрали три модели, создали для них пайплайны и с применением кросс-валидации нашли оптимальные гиперпараметры и оценили метрику F1. После этого мы произвели выбор лучших моделей для дальнейшего тестирования, и из них лучшей оказалась модель логистической регрессии, с результатом F1 0.77, что говорит о высокой точности предсказаний данной модели. Это означает, что модель логистической регрессии способна хорошо разделять токсичные и нетоксичные тексты, и метрика F1 в 0.77 подтверждает высокую сбалансированность между полнотой и точностью предсказаний.
