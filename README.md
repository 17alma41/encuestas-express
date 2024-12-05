# Backend encuestas NDT

Necesitamos crear un backend con las siguientes carcaterísticas:

1. Servir archivos estáticos (index, login, visualizaciones de datos...)
2. Almacenar:
    - users
    - reviews

## Base de datos

Utilizaremos SQLite, con dos tablas, `users` y `reviews`.

- users
    - name
    - password

- reviews
    - rating
    - message

## Api 

###  POST /api/reviews

Endpoint para recibir los datos del usuario, los mandaremos por el body en formato JSON.

```json
{
    "rating": "good",
    "message": "anything"
}
```

**Validaciones en rating**, solo pueden llegar tres valores posibles:
- good
- neutral
- bad

**Validaciones en message**:
- Máximo 256 carácteres