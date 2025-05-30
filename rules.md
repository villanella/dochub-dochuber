# Правила работы с архитектурным репозиторием

1. При описании архитектурного решения в репозитории, необходимо указать, из каких компонентов оно состоит. Компоненты могут представлять из себя сервисы, вложенные в агрегирующий компонент. У каждого компонента есть тип сущности, например, db (database), component, collection и тп. Все компоненты должны быть описаны в файле components.yaml.
2. Каждый компонент должен иметь описание и метаданные, обеспечивающие автоматическую генерацию документации и диаграмм.
3. Идентификаторы компонентов должны быть осмысленными, многоуровневыми, отражать структуру приложения и использовать английские символы и нижние подчеркивания, а также точки для передачи уровней вложенности.
4. Для каждого компонента необходимо создавать файл в формате markdown. Файл будет содержать описание этого компонента. В subjects документа необходимо указать id компонента, который он описывает. 
5. При создании компонентов необходимо в разделе links указывать id зависимых компонентов. Например, при описании фронта веб-сервера, указываем ссылку на бэк, без которого фронт не может работать.
6. Дополнительно для компонента должны быть указаны аспекты - то есть функции, которые данный компонент реализует. Например, функцию аутентификации.
7. Аспекты должны описываться в файле aspects.yaml, иметь уникальный многоуровневый идентификатор с аналогичными требованиями к формату, как и любые другие идентификаторы в Докхабе (id компонента, например). 
8. Для каждого компонента должен быть создан контекст в файле contexts.yaml.
9. У каждого объекта нижних уровней - компонента, контекста, аспекта и т.п. должны быть определены родительские объекты верхнего уровня.
10. При описании решения, необходимо создать отдельный markdown-документ с общим описанием решения. В этом документе рекомендуется привести ссылки на зависимые документы - документы, в которых описаны компоненты решения. В документ должна быть включена визуальная схема решения или ссылка на такую схему

