https://nbviewer.org/github/kasym09/Yandex-Praktikum/blob/main/%D0%9E%D0%BF%D1%80%D0%B5%D0%B4%D0%B5%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5%20%D0%B2%D0%BE%D0%B7%D1%80%D0%B0%D1%81%D1%82%D0%B0%20%D0%BF%D0%BE%D0%BA%D1%83%D0%BF%D0%B0%D1%82%D0%B5%D0%BB%D0%B5%D0%B9/customer%20age%20detection.ipynb
# Описание исследования
Сетевой супермаркет «Хлеб-Соль» внедряет систему компьютерного зрения для обработки фотографий покупателей. Фотофиксация в прикассовой зоне поможет определять возраст клиентов, чтобы:

Анализировать покупки и предлагать товары, которые могут заинтересовать покупателей этой возрастной группы; Контролировать добросовестность кассиров при продаже алкоголя.

Построим модель, которая по фотографии определит приблизительный возраст человека.

# Исходные данные
В нашем распоряжении набор фотографий людей с указанием возраста. 7591 фото.

## Анализ обученной модели
Проект использует архитектуру ResNet50 с блоками сверточных слоев, предобученную на изображениях, и алгоритм обучения нейронной сети Adam. Это позволяет существенно сократить время обучения до 7.5 минут при использовании GPU. Значение метрики MAE на тестовой выборке составляет 7.0417. Это значение можно интерпретировать как погрешность предсказанного возраста в пределах ± 7.04 лет.

Этот подход позволяет определить, к какой возрастной группе можно отнести человека. Это полезно для формирования рекомендаций по товарам. Однако, он не подходит для точного определения совершеннолетия покупателя, так как с текущей погрешностью будут часто возникать ложные срабатывания и ошибки. Для задачи определения совершеннолетия, возможно, потребуется отдельная модель, которая будет классифицировать людей на две категории.

Обучение модели проходит в течение первых 5 эпох, что заметно по динамике функции ошибки и метрик. Последующие эпохи (5-10) позволяют незначительно улучшить результаты предсказаний. Можно остановить обучение после 5 эпох (минимум), но при наличии ресурсов можно попробовать обучать дольше. Однако, решение о длительности обучения также зависит от приоритетов заказчика: "скорость" или "качество".

В дальнейшем, исходя из уточнений и потребностей заказчика, можно внести изменения в параметры и структуру модели для улучшения ее производительности.
