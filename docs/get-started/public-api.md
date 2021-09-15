# Публичное API

**API** предоставляет Вам возможность взаимодействовать с ботом за пределами наших официальных сервисов. Ниже Вы найдете небольшую справку, которая будет описывать задачу каждого эндпоинта.

Стоить приметить, что на текущий момент API находится в разработке. Поэтому, существует только **2** публичных эндпоинта, которые может использовать каждый. В будущем возможности API будут значительно расширятся.

### Получить статистику бота <div style='display: inline;'><p style=' margin-left: 5px; display: inline-block; background-color: #3884FF; width: 70px; border-radius: 20px; padding: 5px; text-align:center;'>GET</p></div>

??? success "Ответ в случае успеха"
    ```
    {"status":"200", "message":"all is ok", "guilds":"666", "users":"6666"}
    ```
??? failure "ответ если бот оффлайн."
    ```
    {"code":"418","message":"No coffee today :("}
    ```
Примеры:
=== "Python"
    ``` python3
    import requests
    result=requests.get('https://kuzaku.ml/api/v1/statistic/')
    print(result.text)
    ```
=== "Javascript"

    ``` javascript
    const Http = new XMLHttpRequest();
    const url='https://kuzaku.ml/api/v1/statistic/';
    Http.open("GET", url);
    Http.send();

    Http.onreadystatechange = (e) => {
        console.log(Http.responseText)
    }
    ```

### Пингануть бота <div style='display: inline;'><p style=' margin-left: 5px; display: inline-block; background-color: #3884FF; width: 70px; border-radius: 20px; padding: 5px; text-align:center;'>GET</p></div>

??? success "Ответ в случае успеха"
    ```
    {"status":"200", "message":"all is ok"}
    ```
??? failure "ответ если бот оффлайн."
    ```
    {"code":"418","message":"No coffee today :("}
    ```
Примеры:
=== "Python"
    ``` python3
    import requests
    result=requests.get('https://kuzaku.ml/api/v1/ping/')
    print(result.text)
    ```
=== "Javascript"

    ``` javascript
    const Http = new XMLHttpRequest();
    const url='https://kuzaku.ml/api/v1/ping/';
    Http.open("GET", url);
    Http.send();

    Http.onreadystatechange = (e) => {
        console.log(Http.responseText)
    }
    ```



