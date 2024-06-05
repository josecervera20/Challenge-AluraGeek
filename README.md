# <p align="center">Challenge AluraGeek</p>

## Objetivo del Desafío
En este desafío, desarrollaremos una aplicación con las siguientes funcionalidades:

- **Listar productos.**
- **Agregar productos.**
- **Eliminar productos.**

## Servidor Local
Este proyecto incluye un servidor local configurado con **JSON Server** para simular una API REST. Para probar su funcionamiento, sigue estos pasos:

1. **Requisitos**:
    - Asegúrate de tener **Node.js** y **npm** instalados en tu entorno de desarrollo.

2. **Inicializa el Servidor Local**:
    - Ejecuta el siguiente comando en la terminal:
        ```
        npm init
        ```
    - También puedes usar `npm init -y` para evitar ingresar los datos manualmente.

3. **Crea el archivo `db.json`**:
    - Crea una carpeta llamada `database`.
    - Dentro de `database`, crea un archivo llamado `db.json` con la siguiente estructura:
        ```json
        {
            "products": [
                {
                    "name": "Nintendo 3DS",
                    "price": "1300",
                    "image_url": "https://m.media-amazon.com/images/I/61Vv8SmYssL._AC_SX679_.jpg",
                    "id": 1
                }
            ]
        }
        ```

4. **Instala JSON Server**:
    - Ejecuta el siguiente comando:
        ```
        npm install json-server
        ```
    - Esto creará la carpeta `node_modules` y agregará la dependencia al archivo `package.json`.

5. **Inicia el Servidor**:
    - Puedes modificar el archivo `package.json` agregando el siguiente script:
        ```json
        "start": "npx json-server --watch database/db.json --port 3000"
        ```
    - Luego, simplemente inicia el servidor JSON con:
        ```
        npm start
        ```
    - Esto permitirá acceder a la API REST simulada en [http://localhost:3000](http://localhost:3000). La ruta para los productos será:
        ```
        http://localhost:3000/products
        ```

### Ejemplos usando la API REST
- **GET** [http://localhost:3000/products](http://localhost:3000/products): devuelve una lista de todos los productos disponibles.
- **POST** [http://localhost:3000/products](http://localhost:3000/products): para agregar un nuevo producto a la lista.
- **DELETE** [http://localhost:3000/products/1](http://localhost:3000/products/1): para eliminar el producto con el ID 1 de la lista.
