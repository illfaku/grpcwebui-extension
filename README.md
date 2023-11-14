# grpcwebui-extension

![request form](assets/images/screenshot-request-form.png "Request form screenshot")

## Установка плагина
1. Скачайте этот репозиторий [https://github.com/victorivanovspb/grpcwebui-extension/](https://github.com/victorivanovspb/grpcwebui-extension/).
2. Переключите свой браузер Chrome в режим разработчика на странице "Расширений" (chrome://extensions/)
3. Загрузите в браузер распакованное расширение (кнопка "Загрузить распакованное расширение" на странице "Расширений").
4. Включите плагин.
5. Перейдите на страницу с grpc-web-ui приложением (если в бэкстейдже, то нужно перейти на **standalone**-страницу апихи).
6. PROFIT

## Что нужно улучшить
* Шапка:
  * рядом с Service name и Method name добавить возможность выбирать Namespace и Service в нем (слева) и указывать окружение dev/test/prod (справа).
* Request Form:
  * Было бы удобно выбирать параметры кликом не только на сам чекбокс, но и на название параметра (чтобы сильно не целиться мышкой).
  * Для енумок (repeated) чуть наслаивается текст про модель на кнопку "Add item".
  * (на подумать) Указывать Request Timeout практичнее в секундах (как сейчас) или милисекундах?
* Raw Request:
  * Нужна json-валидация по схеме.
  * Кнопки справа (plain, pretty, etc.) сделать больше по размеру (чтобы легче было попасть по ним).
  * При раскрытии окна (plain) прикрутить управление с клавиатуры - по Esc закрывать форму; если хватит сил, можно вообще на все кнопки прикрутить быстрые клавиши (например, Ctrl+P (plain), Ctrl+B (beautify), Ctrl-C (copy) и т.д.); клик в сторону также мог бы закрывать раскрытую форму.
  * Plain и Pretty можно объединить в одну кнопку (и одно общее действие), поскольку оба они раскрывают одну и ту же форму. Либо бьютифировать сразу в форме Raw Request, без раскрытия, либо просто убрать plain.
  * В раскрытом окне plain можно тоже добавить кнопку copy.
  * По нажатию на copy не выводить всплывающее окно, на котором еще дополнительно требуется нажимать OK, а уведомлять об успешном копировании каким-нибудь всплывающим уведомлением. Есть ощущение, что сделать Ctrl-A, Ctrl-C быстрее, чем сейчас вести мышью к copy, а потом к OK ).
  * Сделать валидацию на корректность запроса; убрать валидацию при переключении на другую вкладку (Request Form, Response и другие).
  * Сделать конвертирование camelCase в snake_case (например, для легкого копирования и вставки тела запроса в Postman).
* Response:
  * Те же замечания, что и для Raw Request.
  * В раскрытом окне plain кнопка {collapse} написана в фигурных скобках.
* History: 
  * Крестики для удаления записей расположить справа.
  * Кнопку Clear History перенести тоже вправо (над крестиками).
  * Выделять запрос, на который наведена мышь, цветом (например, серым).
  * В раскрытом запросе добавить кнопку copy.

*За предложения по улучшению отдельная благодарность [Стрельцову Михаилу (QA)](https://github.com/stoksik).*
