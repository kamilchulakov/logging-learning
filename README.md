## Ссылки
Прекрасные статьи на Хабр:
- [Java Logging: история кошмара](https://habr.com/ru/post/113145/)
- [Java logging. Hello World](https://habr.com/ru/post/247647/)

Wiki:
- SLF4J [по-русски](https://ru.wikipedia.org/wiki/Slf4J)
- SLF4J :uk:[по-американски](https://en.wikipedia.org/wiki/SLF4J)

Прикольные статейки:
- [Think again before adopting the commons-logging API](http://articles.qos.ch/thinkAgain.html) от разрабов Log4j
- [Логирование с Apache Commons Logging](https://urvanov.ru/2019/07/04/%D0%BB%D0%BE%D0%B3%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5-%D1%81-apache-commons-logging/)
- [Логирование с Slf4j и Logback](https://urvanov.ru/2019/07/08/%d0%bb%d0%be%d0%b3%d0%b8%d1%80%d0%be%d0%b2%d0%b0%d0%bd%d0%b8%d0%b5-%d1%81-slf4j-%d0%b8-logback/)

Baeldung:
- [A Guide To Logback](https://www.baeldung.com/logback)
- [Log4j 2 Plugins](https://www.baeldung.com/log4j2-plugins)

## Ceki Gulcu
Его [Github](https://github.com/ceki)

![Сики](https://avatars.githubusercontent.com/u/115476?v=4)

Founder of log4j, slf4j and logback projects. Currently working on slf4j and logback.

Я думал это прикол, но нет, он придумал все логгеры для жабы.
Мужика нужно уважать, всю жизнь этому посвятил.

## History (Кратко)

![history](https://urvanov.ru/wp-content/uploads/2019/07/xkcd927.png)

**Если я пишу API, значит нет реализации.**
- Первый способ логгирования был System.err.println()
- IBM придумала Log4j (Framework)
- IBM придумала JSR47 (API)
- JSR47 положили в JUL (Java Util Logging JDK 1.4)
- JDK 1.4 не позволяла использовать log4j для реализации JUL. Но Log4j уже использовали в enterprise JDK 1.3
- Люди хотели что-то стандартное, так появился проект JCL (Jakarta Commons Logging). Jakarta - это часть ASF
- JCL(API) был обёрткой для всего, чтобы было на тот момент. //aka Юнифицированный интерфейс, который бегал по classpath
- в 2006 Ceki Gulcu уходит из log4j, который не смог вытянуть logj2 для JDK 1.5 из альфы.
- Создаётся "обёртка всего" SLF4J(API) и Logback(Framework)

## Ситуация на 2011 год

- log4j — используют подсевшие на него изначально и не видящие необходимости перехода.
- JUL — тихо умирающий стандарт. Все, кто изначально пытался его использовать, переезжают на Logback.
- commons-logging — обычно задействован в legacy-библиотеках, которые очень боятся причинить неудобства пользователем, переехав на что-нибудь получше.
- SLF4J — очень популярен в библиотеках. Многие переехали на него, не выдержав ужасов commons-logging
- Logback — обычно современные high-performance серверы, которых не устраивает log4j.


![history](https://urvanov.ru/wp-content/uploads/2019/07/xkcd927.png)

## JUL (Java Util Logging)

![Дерьмо](https://api.polka.academy/storage/block/2123/line_preview_image-d20e4a12c3f93e3d58b2c4426a4eb265.jpeg)

## Log4j (Logging for Java)

![Дерьмо](https://i.ytimg.com/vi/DfExVhYk7w4/hqdefault.jpg)

## JCL (Jakarta Commons Logging)

![Дерьмо](https://онлайн-читать.рф/images/6159.jpg)

## SLF4J (Simple Logging Facade for Java)

![Оцени аву](https://www.appbrain.com/stats/libraries/square-icon/slf4j.png)

SLF4J (Simple Logging Facade for Java) — библиотека для протоколирования, ставящая своей целью предоставить максимально простой, но при этом мощный фасад для различных систем протоколирования на Java.

SLF4J предоставляет простой обобщённый интерфейс для систем протоколирования, не зависящий от конкретной реализации.
Даже лого об этом говорит... ахуенно.

SLF4J was created by Ceki Gülcü as a more reliable alternative to Jakarta Commons Logging framework. Research in 2013 on 10,000 GitHub projects found that the most popular Java library is SLF4J, along with JUnit, with 30.7% of projects using it.

## Log4j2 (Logging for Java v2)

![Пикча](https://logging.apache.org/log4j/2.x/images/logo.png)

В Log4j 2 отдельно выделен интерфейс API и сама реализация, в результате чего мы можем использовать API Log4j 2, но реализацию другого логера.

Вроде норм, а пишут, что нет.

Есть какие-то плагины, из-за этого я не могу нормально сравнивать с Logback.
