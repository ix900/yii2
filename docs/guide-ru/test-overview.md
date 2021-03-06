Тестирование
============

Тестирование является важной составляющей разработки программного обеспечения. Мы проводим тестирование непрерывно, осознаем мы это или нет. Например, когда мы пишем класс на языке PHP, мы можем отлаживать его шаг за шагом или просто использовать `echo` или `die` для проверки, что реализация работает в соответствии с намеченным планом. В случае веб приложения, мы вводим некоторые тестовые данные в форму для того, чтобы убедиться, что страница взаимодействует с нами, как ожидается.

Процесс тестирования может быть автоматизирован так, что каждый раз, когда нам нужно что-то проверить, мы просто должны 
вызвать код, который сделает это за нас. Код, который проверяет, что результат совпадает с тем, что мы планировали, называется тестом, а процесс создания тестов и их последующего использования - автоматизированным тестированием, что и является главной темой данного раздела.

Разработка с тестами
--------------------

Разработка через тестирование (TDD) и разработка через поведение (BDD) - это подходы разработки программного обеспечения, в рамках которых поведение части кода или целая фича описывается в виде набора сценариев или тестов ДО написания фактического кода и только
затем создается реализация. Тем самым мы можем использовать данные тесты для проверки, что достигается заданное поведение.

Процесс разработки фичи следующий:

- Создать новый тест, описывающий функцию, которая будет реализована.
- Запустить новый тест и убедиться, что он терпит неудачу. Это ожидаемо, т.к. на данный момент еще нет конкретной реализации.
- Написать простой код, чтобы новый тест отрабатывал без ошибок.
- Запустить все тесты и убедиться, что они отрабатывают без ошибок
- Улучшить код и убедиться, что все тесты все еще отрабатывают без ошибок

После того как это завершено, процесс повторяется снова для другой фичи или улучшения. Если существующая фича должна быть изменена, то и тесты также должны быть изменены.

> Tip: Если вы чувствуете, что вы теряете время выполняя много мелких и простых итераций, попробуйте покрыть это
> вашим тестовым сценарием перед следующим выполнением тестов. Если вы слишком много отлаживаете, попробуйте сделать обратное.

Написание тестов до реализации конкретного функционала позволяет нам сосредоточиться на том, что мы хотим достичь и полностью
погрузиться в "как это сделать" впоследствии. 

Обычно это приводит к лучшим абстракциям и более легкой поддержке тестов, когда речь идет о корректировке фичи или уменьшении связанности компонентов.

Таким образом, плюсы этого подхода следующие:

- Позволяет вам сосредоточиться на одной вещи, что в свою очередь приводит к улучшению планирования и реализации.
- Более подробное покрытие тестами функционала. Таким образом, если все тесты отрабатывают без ошибок, скорее всего, ничего не сломано.

В долгосрочной перспективе это, как правило, дает вам хороший эффект экономии времени.

> Tip: Если вы хотите узнать больше о принципах сбора требования программного обеспечения и моделирования
> предметной области, рекомендуем изучить [Проблемно-ориентированное проектирование (DDD)](https://en.wikipedia.org/wiki/Domain-driven_design).

Когда и как тестировать
-----------------------

Принцип разработки, описанный выше, имеет смысл применять для долгосрочных и относительно сложных проектов, в то время как для простых это может быть излишним. Есть несколько показателей того, когда данный подход уместен:

- Проект уже большой и сложный.
- Требования к проекту начинают усложняться. Проект постоянно растет.
- Долгосрочный проект.
- Цена ошибки очень высока

Нет ничего плохого в создании тестов, покрывающих поведение существующей реализации.

- Legacy-проект который постоянно обновляется.
- Вам поручили работу над проектом, в котором нет ни одного теста.

В некоторых случаях автоматизированное тестирование может быть излишним:

- Проект простой и не станет более сложным.
- Это одноразовый проект, который больше не будет дорабатываться.

Тем не менее, если у вас есть время, было бы хорошо автоматизировать тестирование и в этих случаях.

Что почитать
------------

- Экстремальное программирование. Разработка через тестирование / Кент Бек. ISBN: 0321146530.
