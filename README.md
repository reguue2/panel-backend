# Panel Backend

Este es el backend para un panel diseñado para contactar con negocios a través de la API de Meta. El backend ha sido configurado para ejecutarse en [Render](https://render.com/) debido a necesidades específicas del proyecto.

## Descripción

Este proyecto tiene como finalidad servir como un intermediario entre los usuarios y la API de Meta, permitiendo la interacción con los negocios mediante endpoints personalizados. La infraestructura está diseñada para asegurar alto rendimiento, flexibilidad y facilidad de despliegue.

### Características principales
- **Conexión con la API de Meta**: Gestión de interacciones y comunicación con empresas.
- **Despliegue en Render**: Beneficios de un entorno de trabajo escalable y confiable.
- **Modularidad**: Código estructurado en JavaScript para facilitar el mantenimiento y ampliación.

---

## Tecnologías utilizadas

- **Lenguaje principal**: JavaScript (99.9% del código).
- **Infraestructura de despliegue**: Render.
- **Herramientas adicionales**:
  - **Procfile**: Configuración de procesos para Render.

---

## Requisitos previos

Antes de empezar, asegúrate de tener lo siguiente instalado:

- **Node.js** (v16 o superior)
- **npm** (gestor de paquetes de Node.js)
- Una cuenta en [Render](https://render.com/)
- Credenciales para acceder a la API de Meta

---

## Instalación y configuración

Sigue estos pasos para configurar el backend en tu entorno local:

1. **Clona el repositorio**:
```bash
git clone https://github.com/reguue2/panel-backend.git
cd panel-backend
```

2. **Instala las dependencias**:
```bash
npm install
```

3. **Configura variables de entorno**:
Crea un archivo `.env` en la raíz del proyecto y configura las siguientes variables:
```
API_META_KEY=tu_clave_api_meta
DB_CONNECTION_STRING=tu_conexion_bd
PORT=3000
```

4. **Ejecuta el servidor localmente**:
```bash
npm start
```
Tu backend estará disponible en `http://localhost:3000`.

---

## Despliegue en Render

1. **Crea un nuevo servicio en Render**:
   - Selecciona el repositorio de GitHub `reguue2/panel-backend`.
   - Configura la rama principal para el despliegue.

2. **Configura los entornos**:
   - Añade las mismas variables de entorno especificadas en tu archivo `.env` durante el proceso de configuración del servicio en Render.

3. **Especifica el comando de inicio**:
   - Asegúrate de indicar el comando `npm start` en el campo correspondiente.

El servicio se desplegará automáticamente y estará disponible en la URL pública proporcionada por Render.

---

## API Endpoints

### Endpoints principales

- **`GET /businesses`**
  - Descripción: Obtiene una lista de negocios conectados con tu cuenta de Meta.
- **`POST /messages`**
  - Descripción: Envía mensajes a un negocio específico a través de la API.
  - Payload esperado:
    ```json
    {
      "businessId": "id_del_negocio",
      "message": "Tu mensaje aquí"
    }
    ```

---

## Contribuciones

Si deseas contribuir al proyecto, sigue estos pasos:

1. Haz un fork del repositorio.
2. Crea una nueva rama (`git checkout -b feature/tu-feature`).
3. Realiza commit con tus cambios (`git commit -m 'Añade nueva característica'`).
4. Haz push de tu rama (`git push origin feature/tu-feature`).
5. Crea un Pull Request.

---

## Licencia

Este proyecto se distribuye bajo la licencia MIT. Consulta el archivo [LICENSE](./LICENSE) para más detalles.

---

## Contacto

Si tienes preguntas o necesitas soporte con el proyecto, no dudes en abrir un issue en el repositorio o contactarme directamente a través de mi perfil de GitHub.