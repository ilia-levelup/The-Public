

## Device API


### device.getAuth
Авторизация устройства.

###### Вызов: POST http://127.0.0.1:5000/device/getAuth

    {"serialNumber":"551fd0e4779e35859dfccd03397dc8a0"}

###### Ответ: JSON

    {"sessionID":"ca28a3cb2c6e6caca6453c6bb53478f2"}


### device.resetCode
Сброс промо-код.

###### Вызов: POST http://127.0.0.1:5000/device/resetCode

    {
            "sessionID":"551fd0e4779e35859dfccd03397dc8a0",
            "code":"1234-5678-9012-3456"
    }

###### Ответ: JSON
    
    {"status":"success"}


### device.tryCode
Запрос валидности промо-кода.

###### Вызов: POST http://127.0.0.1:5000/device/tryCode

    {
        "sessionID":"551fd0e4779e35859dfccd03397dc8a0",
        "code":"1234-5678-9012-3456"
    }

###### Ответ: JSON

    {"status":"success"}


## Коды ошибок

* 400 bad_request
* 401 forbidden 
* 403 unauthorized 
* 404 not_found
* 405 method_not_allowed 
* 500 server_error
* 501 not_implemented 
* 503 service_unavailable 
