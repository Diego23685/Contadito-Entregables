# Contadito

## Descripcion del Proyecto
Contadito es una aplicacion Fullstack disenada para la gestion de productos, clientes y almacenes en pequenas y medianas empresas (PYMES).
El sistema cuenta con un **backend** desarrollado en **.NET 8 con Entity Framework Core y MySQL**, y un **frontend movil** construido en **React Native con Expo**.
Su objetivo es proporcionar un control eficiente del inventario, clientes y almacenes, facilitando la administracion y toma de decisiones.

## Requerimientos Tecnicos

### Backend
- .NET 8 SDK
- MySQL 8 o superior (o base de datos en memoria para pruebas)
- Herramientas:
  - Visual Studio Code o Visual Studio
  - Postman o cURL para pruebas de API
  - Swagger UI (ya integrado)

### Frontend
- Node.js 18 o superior
- Expo CLI (`npm install -g expo-cli`)
- React Native (ultima version estable)
- Dispositivo fisico o emulador Android/iOS

## Instalacion

### 1. Clonar el repositorio
```bash
git clone https://github.com/Diego23685/contadito-fullstack
cd contadito-fullstack
```

### 2. Configurar el Backend
1. Ve a la carpeta del backend:
    ```bash
    cd backend
    ```
2. Crea la base de datos MySQL y actualiza `appsettings.json` con tu cadena de conexion:
    ```json
    "ConnectionStrings": {
      "MySql": "server=localhost;port=3306;database=contadito;user=root;password=tu_contrasena"
    }
    ```
3. Restaura dependencias y ejecuta:
    ```bash
    dotnet restore
    dotnet run
    ```
4. El backend estara disponible en:
   [http://127.0.0.1:5000](http://127.0.0.1:5000)
   Documentacion Swagger: [http://127.0.0.1:5000/swagger](http://127.0.0.1:5000/swagger)

### 3. Configurar el Frontend
1. Ve a la carpeta del frontend:
    ```bash
    cd frontend
    ```
2. Instala las dependencias:
    ```bash
    npm install
    ```
3. Inicia el proyecto:
    ```bash
    npx expo start
    ```
4. Usa un emulador o la app Expo Go en tu dispositivo movil para escanear el QR generado.

## Uso Basico
1. **Registrar un Tenant y Owner (dueno):**
   Envía un POST a `/auth/register-tenant` para crear la empresa y el usuario dueno.
2. **Iniciar sesion:**
   Envía un POST a `/auth/login` con el email y contrasena del usuario.
3. **Gestionar datos:**
   - **Productos:** CRUD en `/products`
   - **Clientes:** CRUD en `/customers`
   - **Almacenes:** CRUD en `/warehouses`
