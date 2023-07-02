# План тестирования возможности записаться на обучение профессии «Тестировщик ПО»

## Перечень автоматизируемых сценариев:
#### Предусловие
Переход к форме записи на курс "Тестировщик ПО":
- Открыть стартовую страницу сайта Нетология (https://netology.ru/)
- Существует несколько способов перехода к форме записи на курс:
1. В левом верхнем углу нажать на **"Каталог курсов"**, нажать на категорию **"Программирование"**, нажать на категорию **"Тестировщик ПО"**, нажать на кнопку **"Записаться"**, псле чего происходит спуск вниз по страницу к форме записи на курс.

2. ***Если пользователь зарегестирован!*** В левом верхнем углу нажать на **"Каталог курсов"**, нажать на категорию **"Программирование"**, нажать на категорию **"Тестировщик ПО"**, нажать на кнопку **"Записаться"** в верхнем правом углу рядом с профилем, псле чего происходит спуск вниз по страницу к форме записи на курс.

3. На главной странице веб-сайта Нетология нажать на категорию **"Программирование"**,нажать на профессию **"Тестировщик ПО"**, нажать на кнопку **"Записаться"**, псле чего происходит спуск вниз по страницу к форме записи на курс.

4. На главной странице веб-сайта Нетология нажать на категорию **"Программирование"**, в поле поиска ***"Какой курс вам нужен?"*** ввести **"Тестировщик ПО"**, нажать на курс **"Тестировщик ПО"**, нажать на кнопку **"Записаться"**, псле чего происходит спуск вниз по страницу к форме записи на курс.

#### Тестовые сценарии

**Позитивные сценарии**

Пользователь *не авторизирован* на сайте:
- Ввести валидное значение в поле **«Имя»** (Имя из 2-3х символов, очень длинное имя, двойное имя, имя с разными регистрами, с буквой Ё)
- Ввести валидное значение в поле **номера телефона** (в формате 89239996633 или +8 (923) 999-66-33)
- Ввести валидное значение в поле **«Электронная почта»** (Почти на латинице, почты на кириллице, почты использующие спец.знаки)

**Ожидаемый результат** - Сообщение на электронную почту с подтверждением заявки.

Пользователь *авторизирован* на сайте:
- Ввести валидное значение в поле **«Имя»** (Имя из 2-3х символов, очень длинное имя, двойное имя, имя с разными регистрами, с буквой Ё)
- Ввести валидное значение в поле **номера телефона** (в формате 89239996633 или +8 (923) 999-66-33)

**Ожидаемый результат** - Сообщение на электронную почту с подтверждением заявки.

**Негативные сценарии**

1. Оставить поле|поля пустыми. ***Ожидаемый результат:*** поле|поля подсвечиваются с ошибкой **«Обязательное поле»**.
2. Ввести не валидное значение в поле **«Имя»** (один символ, цифры, спец.свимволы, имя дленнее 128 символов, пробел вместо имени, использование букв языков отличных от кириллицы) ***Ожидаемый результат:*** поле «Имя» подсвечивается красным, сообщение об ошибке: *«Должно состоять из букв»*
3. Ввести не валидное значение в поле **номера телефона** (симловы отличные от цифр или `+()-`, номер длинной менее|более 11 цифр) 
**Ожидаемый результат:** поле **номера телефона** подсвечивается красным, сообщение об ошибке: **«Номер в формате +9 (999) 999-99-99»**.
4. Ввесьти не валидное значение в поле **«Электронная почта»** (Длина почты более 320 символов, почта без знака `@`, импользование пробелов, отсутствие точки в домене, почта без имени|домена, не валидный домен)
**Ожидемый результат:** поле **«Электронный адрес»** подсвечивается красным, сообщение об ошибке: **«Неверный email»**.

#### Перечень используемых инструментов

- **IntelliJ IDEA** - интегрированная среда разработки ПО для многих языков программирования. Удобная среда для написания авто-тестов.
- **Java 11** - объектно-ориентированный язык программирования, оптимальный для написания автотестов.
- **JUnit 5** - инструмент тестирования, среда модульного тестирования для языка программирования *Java*.
- **Gradle** - мощная и простая система автоматической сборки проектов и отчетности, которая используется для упрощения работы с *Java*.
- **Selenide** - это фреймворк для автоматизированного тестирования веб-приложений на основе *Selenium WebDriver*, дающий следующие преимущества: изящный API, поддержка AJAX для стабильных тестов, мощные селекторы, простая конфигурация.
- **Faker** - это библиотека, которая позволяет генерировать случайные данные. С ее помощью можно заполнить таблицы в базе данных, построить корректные XML-документы, сформировать JSON-ответы для REST.

#### Перечень необходимых разрешений, данных и доступов

- Разрешение на проведение автоматизированного тестирование на сайте [«Нетология»](https://netology.ru/).
- Техническая документация, для правильного составления тест-кейсов.

#### Перечень и описание возможных рисков при автоматизации

- Высокая частота обновления дизайна|функционала сайта может привести к падению автотестов
- Ложные срабытывания по отправке фор увеличивающие нагрузку по обработке данных.

#### Перечень необходимых специалистов для автоматизации

Данное задание можно назначит начинающему специалисту автоматизированного тестирования, знакового с перечнем используемых инструментов.

#### Перечень необходимых специалистов для автоматизации

Для осуществелния тест-плана по автоматизации, потребуется от 5 до 8 рабочих часа.