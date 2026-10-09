# ✈️ Agencia de Viajes

Sitio web para una agencia de viajes, renderizado desde el servidor con **Node.js**, **Express** y **Pug**. Muestra los próximos viajes con su información detallada y permite a los visitantes dejar testimoniales sobre sus experiencias.

Los datos se guardan en **MySQL** y se consultan con el ORM **Sequelize**.

![Captura del sitio](./docs/captura.png)

## ✨ Características

- **Página de inicio** con los tres próximos viajes, una promoción destacada y los últimos testimoniales.
- **Listado de viajes** con imagen, precio y fechas.
- **Detalle de cada viaje** con fechas de ida y vuelta, precio, lugares disponibles y descripción, en URLs amigables basadas en un *slug* (por ejemplo, `/viajes/viaje-italia`).
- **Testimoniales**: los visitantes pueden publicar el suyo mediante un formulario con validación en el servidor.
- **Página "Nosotros"** con información de la agencia.
- **Plantillas reutilizables con Pug**: layout principal, encabezado, pie de página y bloques compartidos.
- **Diseño responsivo** con Bootstrap.

## 🛠️ Tecnologías

- [Node.js](https://nodejs.org/) y [Express](https://expressjs.com/)
- [Pug](https://pugjs.org/) como motor de plantillas
- [MySQL](https://www.mysql.com/) con [Sequelize](https://sequelize.org/) y [mysql2](https://github.com/sidorares/node-mysql2)
- [Bootstrap](https://getbootstrap.com/) para los estilos
- [dotenv](https://github.com/motdotla/dotenv) para las variables de entorno
- [nodemon](https://nodemon.io/) para desarrollo

## 📋 Requisitos

- [Node.js](https://nodejs.org/) 18 o superior
- Un servidor MySQL 8, local o en la nube

## 🚀 Instalación y uso

1. Clona el repositorio:

   ```bash
   git clone https://github.com/SuemyDzib/agencia-viajes-node.git
   cd agenciaViajesNode
   ```

2. Instala las dependencias:

   ```bash
   npm install
   ```

3. Crea la base de datos e importa los datos de ejemplo, que incluyen las tablas `viajes` y `testimoniales`:

   ```bash
   mysql -u root -p -e "CREATE DATABASE agenciaviajes"
   mysql -u root -p agenciaviajes < agenciaviajes.sql
   ```

   También puedes hacerlo desde una herramienta gráfica como MySQL Workbench, abriendo y ejecutando el archivo `agenciaviajes.sql`.

4. Crea un archivo `.env` a partir del ejemplo y coloca la cadena de conexión a tu base de datos:

   ```bash
   cp .env.example .env
   ```

   ```env
   DATABASE_URL=mysql://usuario:password@localhost:3306/agenciaviajes
   ```

5. Inicia el servidor en modo desarrollo:

   ```bash
   npm run dev
   ```

6. Abre `http://localhost:3000` en tu navegador.

### Variables de entorno

| Variable       | Descripción                                                          |
| -------------- | -------------------------------------------------------------------- |
| `DATABASE_URL` | Cadena de conexión a MySQL con el formato `mysql://usuario:password@host:puerto/base_de_datos` |
| `PORT`         | Puerto del servidor (opcional, por defecto `3000`)                   |

## 👤 Autor

Desarrollado por **Suemy Dzib** – [@SuemyDzib](https://github.com/SuemyDzib) a través del curso de Udemy impartido por Juan de la Torre.