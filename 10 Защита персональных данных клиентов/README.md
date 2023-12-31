https://nbviewer.org/github/kasym09/Yandex-Praktikum/blob/main/10%20%D0%97%D0%B0%D1%89%D0%B8%D1%82%D0%B0%20%D0%BF%D0%B5%D1%80%D1%81%D0%BE%D0%BD%D0%B0%D0%BB%D1%8C%D0%BD%D1%8B%D1%85%20%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D1%85%20%D0%BA%D0%BB%D0%B8%D0%B5%D0%BD%D1%82%D0%BE%D0%B2/10%20%D0%97%D0%B0%D1%89%D0%B8%D1%82%D0%B0%20%D0%BF%D0%B5%D1%80%D1%81%D0%BE%D0%BD%D0%B0%D0%BB%D1%8C%D0%BD%D1%8B%D1%85%20%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D1%85%20%D0%BA%D0%BB%D0%B8%D0%B5%D0%BD%D1%82%D0%BE%D0%B2.ipynb
# 10 Защита персональных данных клиентов

Вам нужно защитить данные клиентов страховой компании «Хоть потоп». Разработайте такой метод преобразования данных, чтобы по ним было сложно восстановить персональную информацию. Обоснуйте корректность его работы.

Нужно защитить данные, чтобы при преобразовании качество моделей машинного обучения не ухудшилось. Подбирать наилучшую модель не требуется.

# Описание данных
Набор данных находится в файле /datasets/insurance.csv.
Признаки: пол, возраст и зарплата застрахованного, количество членов его семьи.
Целевой признак: количество страховых выплат клиенту за последние 5 лет.

#### Вывод:
 После успешного выполнения операции умножения признаков на обратную матрицу и обучения модели линейной регрессии, мы можем сказать, что данные пользователей были успешно защищены. Применение этого преобразования не привело к потере качества модели, и мы смогли достичь двух целей: обеспечить безопасность персональных данных и сохранить эффективность модели.
