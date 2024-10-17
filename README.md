# **Plataforma de Reseñas de Libros**

Esta es una plataforma de reseñas de libros construida con **Next.js** que permite a los usuarios consultar información sobre libros y dejar sus reseñas. El proyecto está diseñado con una **arquitectura modular y basada en capas**, lo que facilita su mantenibilidad y escalabilidad.

## **Índice**
- [Tecnologías](#tecnologías)
- [Estructura del proyecto](#estructura-del-proyecto)
- [Arquitectura](#arquitectura)
- [Instalación](#instalación)
- [Uso](#uso)
- [Contribución](#contribución)

## **Tecnologías**
Este proyecto utiliza las siguientes tecnologías:
- [Next.js](https://nextjs.org/) - Framework React para aplicaciones web.
- [React](https://reactjs.org/) - Biblioteca JavaScript para interfaces de usuario.
- [CSS Modules](https://github.com/css-modules/css-modules) - Módulos de CSS para estilos locales.
- [API Routes](https://nextjs.org/docs/api-routes/introduction) de Next.js para gestionar la API interna.

## **Estructura del proyecto**

La estructura de carpetas sigue una **arquitectura modular y por capas**, que organiza el código en módulos según su responsabilidad y separa las diferentes capas de la aplicación (presentación, lógica de negocio, infraestructura). 

```
/src
  /api                # Endpoints API para manejar las reseñas y los libros.
  /components         # Componentes React reutilizables.
    /common           # Componentes comunes a toda la aplicación.
    /book             # Componentes específicos de libros.
    /review           # Componentes específicos de reseñas.
  /hooks              # Hooks personalizados para obtener datos.
  /lib                # Lógica de infraestructura, como conexión a la API o a la base de datos.
  /pages              # Rutas y páginas de la aplicación.
    /api              # Rutas API de Next.js.
    /books            # Rutas relacionadas con los libros.
  /public             # Archivos estáticos, como imágenes.
  /services           # Servicios de lógica de negocio (manejadores de libros y reseñas).
  /styles             # Estilos globales y módulos CSS.
  /utils              # Funciones de utilidades y validaciones.
```

### **Explicación de las carpetas clave**:

- **/api**: Contiene los endpoints de API que manejan la lógica de backend para libros y reseñas, utilizando las API Routes de Next.js.
- **/components**: Los componentes están organizados de forma modular, agrupados por contexto (libros, reseñas, componentes comunes). Esto mejora la reutilización y el mantenimiento del código.
- **/hooks**: Contiene hooks personalizados para manejar lógica compleja o asíncrona, como la obtención de datos desde la API.
- **/lib**: Se usa para la lógica de infraestructura como clientes API o conexiones a bases de datos.
- **/services**: Aquí se implementa la lógica de negocio. Por ejemplo, `bookService.js` maneja la obtención de libros desde la base de datos o la API.
- **/pages**: Utilizada para las rutas de la aplicación. Next.js gestiona las rutas basándose en la estructura de esta carpeta. La carpeta `/pages/api` contiene las rutas API.
- **/public**: Almacena los archivos estáticos, como imágenes de portadas de libros.
- **/styles**: Contiene estilos globales y módulos CSS para aplicar estilos específicos a los componentes.
- **/utils**: Funciones utilitarias como validadores o constantes globales.

## **Arquitectura**
Este proyecto sigue una **arquitectura modular y basada en capas**. Cada parte del sistema está organizada según su responsabilidad y se divide en capas que cumplen funciones específicas.

### **Modularidad**:
El código está organizado en módulos independientes (carpetas como `components`, `hooks`, `services`, etc.). Esto permite:
- **Reutilización**: Los módulos pueden ser reutilizados en diferentes partes del proyecto.
- **Mantenibilidad**: Es más fácil mantener y actualizar el código.

### **Capas**:
El proyecto está dividido en las siguientes capas:
1. **Capa de Presentación**: Contiene los componentes de la interfaz de usuario. Estos componentes interactúan con la capa de aplicación a través de hooks.
2. **Capa de Aplicación**: Implementa la lógica de negocio y la interacción con las APIs. Los hooks personalizados y los servicios se encargan de gestionar la lógica de la aplicación.
3. **Capa de Infraestructura**: Maneja la interacción con bases de datos o APIs externas. La lógica de conexión a estas fuentes está contenida en la carpeta `lib` y en los endpoints de API en `pages/api`.

## **Instalación**

Sigue los siguientes pasos para ejecutar este proyecto localmente.

### **Requisitos previos**:
- [Node.js](https://nodejs.org/en/) (v16 o superior)
- [npm](https://www.npmjs.com/) o [yarn](https://yarnpkg.com/)

### **Pasos de instalación**:

1. Clona este repositorio:

   ```bash
   git clone https://github.com/tu-usuario/Book-Reviews-Platform.git
   ```

2. Ve al directorio del proyecto:

   ```bash
   cd Book-Reviews-Platform
   ```

3. Instala las dependencias:

   ```bash
   npm install
   # o
   yarn install
   ```

4. Inicia el servidor de desarrollo:

   ```bash
   npm run dev
   # o
   yarn dev
   ```

   El servidor se ejecutará en `http://localhost:3000`.

## **Uso**

### **Navegación**:
- Visita la página principal en `http://localhost:3000` para ver una lista de libros.
- Haz clic en cualquier libro para ver más detalles y las reseñas relacionadas.
- Escribe una reseña desde la página de detalles de un libro.

### **API**:
- `/api/books`: Devuelve la lista de libros.
- `/api/reviews`: Endpoint para agregar o obtener reseñas de libros.

## **Contribución**

Si deseas contribuir a este proyecto, por favor sigue estos pasos:

1. Haz un fork del proyecto.
2. Crea una nueva rama con tu feature o corrección de errores: `git checkout -b mi-feature`.
3. Haz commit de tus cambios: `git commit -m 'Agregué mi nueva feature'`.
4. Haz push a tu rama: `git push origin mi-feature`.
5. Abre un pull request en GitHub.
