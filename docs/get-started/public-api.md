# Публичное API

**API** предоставляет Вам возможность взаимодействовать с ботом за пределами наших официальных сервисов. Ниже Вы найдете небольшую справку, которая будет описывать задачу каждого эндпоинта.

Стоить приметить, что на текущий момент API находится в разработке. Поэтому, существует только **2** публичных эндпоинта, которые может использовать каждый. В будущем возможности API будут значительно расширятся.

### Получить статистику бота 

| url      | Метод                          |
| :---------- | :----------------------------------- |
| `https://kuzaku.ml/api/v1/statistic/`       | `GET`  |

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

### Пингануть бота

| url      | Метод                          |
| :---------- | :----------------------------------- |
| `https://kuzaku.ml/api/v1/ping/`       | `GET`  |

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



