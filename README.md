## E-learning
В данном проекте реализован анализ обучающей платформы на основе данных о завершенных уроках


## Задачи
  1. Определить, сколько студентов успешно сдали только один курс.
  2. Выявить самый сложный и самый простой экзамен: найти курсы и экзамены в рамках курса, которые обладают самой низкой и самой высокой завершаемостью.
  3. Определить средний срок сдачи экзаменов по каждому предмету.
  4. Выявить ТОП-3 самых популярных предметов по количеству регистраций на них, а также предметов с самым большим оттоком.
  5. Выявить семестр с самой низкой завершаемостью курсов и самыми долгими средними сроками сдачи курсов в период с начала 2013 по конец 2014.
  6. Построить адаптированные RFM-кластеры студентов, где R - среднее время сдачи одного экзамена, F - завершаемость курсов, M - среднее количество баллов, получаемое за экзамен.


## Данные
* **assessments.csv** — файл c информацей об оценках.
  Обычно каждый предмет в семестре включает ряд тестов с оценками, за которыми следует заключительный экзаменационный тест (экзамен).
  * code_module — идентификационный код предмета
  * code_presentation — идентификационный код семестра
  * id_assessment — идентификационный код теста
  * assessment_type — тип теста (TMA - оценка преподавателя, СМА - компьютерная оценка, Exam - экзамен по курсу)
  * date — количество дней с момента начала семестра до даты окончательной сдачи теста
  * weight — вес теста в % в оценке за курс

* **courses.csv** — файл со списком предметов по семестрам.
  * code_module — идентификационный код предмета
  * code_presentation — идентификационный код семестра
  * module_presentation_length — продолжительность семестра в днях

* **studentAssessment.csv** — файл с результатами тестов студентов.
  * id_assessment — идентификационный код теста
  * id_student — идентификационный номер студента
  * date_submitted — дата сдачи теста студентом, измеряемая как количество дней с начала семестра
  * is_banked — факт перезачета теста с прошлого семестра (для студентов, вернувшихся из академического отпуска)
  * score — оценка учащегося в этом тесте в формате от 0 до 100 баллов

* **studentRegistration.csv** — этот файл содержит информацию о времени, когда студент зарегистрировался для прохождения курса в семестре.
  * code_module — идентификационный код предмета
  * code_presentation — идентификационный код семестра
  * id_student — идентификационный номер студента
  * date_registration — количество дней от начала семестра до даты регистрации студента
  * date_unregistration — дата отмены регистрации студента с предмета


## Реализация
* Провела предварительный анализ и предобработку данных.
* Проанализировала обучение студентов и завершаемость курсов.
* Построила адаптированную RFM-сегментацию студентов.
