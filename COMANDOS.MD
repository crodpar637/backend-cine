### Creación del proyecto
```
md proyecto
cd proyecto
npm init -y
```

### Libreria para gestionar ficheros ce configuración
```
npm install dotenv 
```

### Instalar nodemon 
```
npm install --save-dev nodemon
```

### Crear un script para desarrollo en package.json
```
 "scripts": {
    "start": "node index.js",
    "dev": "nodemon index.js",
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  ```

### Crear fichero .env.development con las variables de entorno de desarrollo
### Este es el fichero que se usa con npm run dev
### El fichero .env.production se usa con npm start
```
# Configuración de la base de datos
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=test
DB_NAME=bar
DB_PORT=3306
# Otras configuraciones
PORT=3000
```

### Instalación y configuración de librerías para manejar la base de datos
```
npm i mysql2 sequelize sequelize-auto
```

// Configurar ./config/sequelize.js y ./config/sequelize-auto.js con parámetros de bbdd
// Utilizar para ello los parámetros definidos en los ficheros de entorno .env

// Probar la conexion
```
node ./config/sequelize.js
```

//Generar los modelos a partir de la estructura de la base de datos (ingeniería inversa)
```
node ./config/sequelize-auto.js
```

### Instalar express, cors
```
npm i express cors
```

### Ejecutar proyecto
```
npm run dev
```

### Instalar librerías para montar un sistema de autentificación basado en JWT
```
npm install jsonwebtoken cookie-parser bcrypt
```

**1. Configurar el repositorio:**
   - Inicializa el repositorio si aún no lo has hecho:
     ```bash
     git init
     ```
   - Agrega y configura un archivo `.gitignore` en la carpeta raíz del proyecto :
     ```plaintext
     node_modules/
     desktop.ini
     ```
   - Añade los archivos al índice y realiza el primer commit:
     ```bash
     git add .
     git commit -m "Initial commit"
     ```
**2. Conectar con GitHub:**
   - Crea un repositorio en GitHub y conéctalo con tu proyecto local:
     ```bash
     git remote add origin <URL_DEL_REPOSITORIO>
     git branch -M main
     git push -u origin main
     ```
---
**3. Sincronización automática en GitHub:**
   - Para el entorno local configura VSCode con la opción **Auto Save** para guardar los archivos automáticamente.
   - Usa tareas en VSCode o comandos manuales para realizar `git add`, `commit` y `push` según sea necesario:
     ```bash
     git add .
     git commit -m "Auto save changes"
     git push
     ```

