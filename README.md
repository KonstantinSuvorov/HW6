# Автоматизация тестирования мобильных приложений

## Практическая работа 6 

Закрепить знания о паттернах проектирования и способах их реализации.

## Что нужно сделать

Реализовать в проекте следующие паттерны:
    ●PageObject/ScreenObject.
    ●Decorator.
    ●Factory.
    ●Strategy.
Скачайте папку Homework с проектом в Git. В этом проекте уже реализован
небольшой тест с подробными комментариями каждого шага.
Последовательно выполните следующие действия:
1. Реализуйте паттерн ScreenObject, оставив в тесте только вызовы
методов Screen-классов и методы isDisplayed().
2. Добавьте логирование в метод afterFindBy(), реализуя интерфейс
AppiumWebDriverEventListener (паттерн «Декоратор»). Свойства element
в логах лучше не использовать, поскольку он порождает ошибку
UndeclaredThrowableException.
3. Класс DriverFactory измените таким образом, чтобы он отдавал вам тип
драйвера в зависимости от запускаемой платформы — Android или iOS
(паттерн «Фабрика»).
4. Реализуйте два вида стратегии перехода с экрана корзины на главную.
Первый способ — через элемент таббара, второй способ — через кнопку
«На главную». В тест добавьте вызов любой из этих стратегий (паттерн
«Стратегия»).

## Советы и рекомендации
    ● Обратите внимание, что в этом проекте используется библиотека JUnit
5. Поэтому все проверки используются не из класса Assert, а из класса
Assertions. Вместо аннотаций Before и After используются аннотации
BeforeAll и AfterAll.
Для всех Screen-классов создайте основной класс Screen, чтобы
инициализировать драйвер и элементы в одном месте.
    ● Вы можете также создать класс BaseTest, реализовать наследование
вашего тестового класса от класса BaseTest и вынести туда логику
создания и закрытия драйвера. Таким образом, вы оставите в тестовом
классе исключительно тесты (следование принципу единой
ответственности).

## Что оценивается
    ● Код компилируется и запускается.
    ● Решение чётко соответствует заданным условиям.
    ● Паттерны реализованы правильно.
