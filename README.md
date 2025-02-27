# Proyecto con Proxy Inverso y SSL

## Configuración del entorno

Para que el proyecto funcione correctamente, necesitas crear un archivo `.env` en la raíz del proyecto con las credenciales de la base de datos.

### 📄 Creación del archivo `.env`
Crea un archivo `.env` en la raíz del proyecto con el siguiente contenido:

```env
MYSQL_ROOT_PASSWORD=root
MYSQL_DATABASE=JLL_BD
MYSQL_USER=alumnoDAW
MYSQL_PASSWORD=passJLL
```

Este archivo es importante porque almacena las credenciales de la base de datos sin exponerlas en `docker-compose.yml`.

## 🔧 Pasos para desplegar el proyecto
1. **Clonar el repositorio**:
   ```sh
   git clone <URL_DEL_REPO>
   cd <NOMBRE_DEL_PROYECTO>
   ```
2. **Crear el archivo `.env`** siguiendo la sección anterior.
3. **Construir y ejecutar los contenedores**:
   ```sh
   docker-compose up --build -d
   ```
4. **Acceder al proyecto**:
   - Frontend: `http://localhost:3000`
   - Backend: `http://localhost:8000`
   - phpMyAdmin: `https://localhost/phpmyadmin/`

## 🌐 Despliegue en AWS
Cuando despliegues el proyecto en AWS, recuerda actualizar la configuración del proxy inverso (`default.conf`) con la IP pública del servidor en `server_name`.
