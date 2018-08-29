# Теория Тестирования

## Основные термины
**Обеспечение качества (Quality Assurance)** - это совокупность мероприятий, охватывающих все технологические этапы разработки, выпуска и эксплуатации ПО, предпринимаемых на разных стадиях жизненного цикла ПО, для обеспечения требуемого уровня качества выпускаемого продукта.

**Качество программного обеспечения (Software Quality)** — это совокупность характеристик программного обеспечения, относящихся к его способности удовлетворять установленные и предполагаемые потребности.

**Контроль качества (Quality Control)** - это совокупность действий, проводимых над продуктом в процессе разработки, для получения информации о его актуальном состоянии.

**Тестирование программного обеспечения (Software Testing)** — проверка соответствия между реальным и ожидаемым поведением программы, осуществляемая на конечном наборе тестов, выбранном определенным образом. В более широком смысле, тестирование — это одна из техник контроля качества, включающая в себя:
- Планированию работ (Test Management).
- Проектирование тестов (Test Design).
- Выполнение тестирования (Test Execution).
- Анализ полученных результатов (Test Analysis).

**Верификация (verification)** - это процесс оценки системы или её компонентов с целью определения удовлетворяют ли результаты текущего этапа разработки условиям, сформированным в начале этого этапа (выполняются ли наши цели, сроки, задачи по разработке проекта, определенные в начале текущей фазы).

**Валидация (validation)** - это определение соответствия разрабатываемого ПО ожиданиям и потребностям пользователя, требованиям к системе.

**Тест план (Test Plan)** — это документ, описывающий весь объем работ по тестированию, начиная с описания объекта, стратегии, расписания, критериев начала и окончания тестирования, до необходимого в процессе работы оборудования, специальных знаний, а также оценки рисков с вариантами их разрешения. Отвечает на вопросы:
- Что надо тестировать?
- Что будете тестировать?
- Как будете тестировать?
- Когда будете тестировать?
- Критерии начала тестирования.
- Критерии окончания тестирования.

**Тест дизайн** — это этап процесса тестирования ПО, на котором проектируются и создаются тестовые случаи (тест кейсы), в соответствии с определёнными ранее критериями качества и целями тестирования.

**Матрица соответствия требований (Traceability matrix)** — это двумерная таблица, содержащая соответсвие функциональных требований (functional requirements) продукта и подготовленных тестовых сценариев (test cases). В заголовках колонок таблицы расположены требования, а в заголовках строк — тестовые сценарии. На пересечении — отметка, означающая, что требование текущей колонки покрыто тестовым сценарием текущей строки.

**Тестовый случай (Test Case)** — это артефакт, описывающий совокупность шагов, конкретных условий и параметров, необходимых для проверки реализации тестируемой функции или её части.

**Чек-лист (check list)** — это документ, описывающий что должно быть протестировано. При этом чек-лист может быть абсолютно разного уровня детализации. На сколько детальным будет чек-лист зависит от требований к отчетности, уровня знания продукта сотрудниками и сложности продукта.

## Техники тест дизайна
- **Эквивалентное Разделение (Equivalence Partitioning — EP)**. Как пример, у вас есть диапазон допустимых значений от 1 до 10, вы должны выбрать одно верное значение внутри интервала, скажем, 5, и одно неверное значение вне интервала — 0.

- **Анализ Граничных Значений (Boundary Value Analysis — BVA)**. Если взять пример выше, в качестве значений для позитивного тестирования выберем минимальную и максимальную границы (1 и 10), и значения больше и меньше границ (0 и 11). Анализ Граничный значений может быть применен к полям, записям, файлам, или к любого рода сущностям имеющим ограничения.

- **Причина / Следствие (Cause/Effect — CE)**. Это, как правило, ввод комбинаций условий (причин), для получения ответа от системы (Следствие). Например, вы проверяете возможность добавлять клиента, используя определенную экранную форму. Для этого вам необходимо будет ввести несколько полей, таких как «Имя», «Адрес», «Номер Телефона» а затем, нажать кнопку «Добавить» — это «Причина». После нажатия кнопки «Добавить», система добавляет клиента в базу данных и показывает его номер на экране — это «Следствие».

- **Предугадывание ошибки (Error Guessing — EG)**. Это когда тестировщик использует свои знания системы и способность к интерпретации спецификации на предмет того, чтобы «предугадать» при каких входных условиях система может выдать ошибку. Например, спецификация говорит: «пользователь должен ввести код». Тестировщик будет думать: «Что, если я не введу код?», «Что, если я введу неправильный код? », и так далее.

- **Исчерпывающее тестирование (Exhaustive Testing — ET)**. В пределах этой техники вы должны проверить все возможные комбинации входных значений, и в принципе, это должно найти все проблемы. На практике применение этого метода не представляется возможным, из-за огромного количества входных значений.

- **Парное тестирование (Pairwise Testing)**. Это техника формирования наборов тестовых данных состоящая в формировании таких наборов данных, в которых каждое тестируемое значение каждого из проверяемых параметров хотя бы единожды сочетается с каждым тестируемым значением всех остальных проверяемых параметров.

## Цели тестирования
- Повысить вероятность того, что приложение, предназначенное для тестирования, будет работать правильно при любых обстоятельствах.
- Повысить вероятность того, что приложение, предназначенное для тестирования, будет соответствовать всем описанным требованиям.
- Предоставление актуальной информации о состоянии продукта на данный момент.

## Тестирования производительности
- Нагрузочное тестирование (Performance and Load Testing).
- Стрессовое тестирование (Stress Testing).
- Тестирование стабильности или надежности (Stability / Reliability Testing).
- Объемное тестирование (Volume Testing).