<h1 align="center">Login Laravel</h1>

<p align="center">
  Sistema de autenticación completo construido con Laravel 9 y Laravel Breeze.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Laravel-9-FF2D20?logo=laravel&logoColor=white" alt="Laravel 9">
  <img src="https://img.shields.io/badge/PHP-8.0+-777BB4?logo=php&logoColor=white" alt="PHP 8">
  <img src="https://img.shields.io/badge/Tailwind_CSS-06B6D4?logo=tailwindcss&logoColor=white" alt="Tailwind CSS">
  <img src="https://img.shields.io/badge/MySQL-4479A1?logo=mysql&logoColor=white" alt="MySQL">
  <img src="https://img.shields.io/badge/Vite-646CFF?logo=vite&logoColor=white" alt="Vite">
</p>

---

## Descripción

Aplicación web que implementa el flujo completo de autenticación de usuarios con **Laravel 9** y **Laravel Breeze**, usando vistas Blade y estilos con Tailwind CSS.

## Funcionalidades

- Registro de usuarios
- Inicio y cierre de sesión
- Recuperación y restablecimiento de contraseña por correo
- Verificación de correo electrónico
- Confirmación de contraseña para acciones sensibles
- Panel (*dashboard*) protegido con middleware `auth` y `verified`
- Perfil de usuario: editar datos, cambiar contraseña y eliminar la cuenta

## Estructura relevante

```
app/Http/Controllers/
├── Auth/                 # Controladores de autenticación (Breeze)
└── ProfileController.php # Edición y eliminación del perfil
resources/views/
├── auth/                 # Login, registro, recuperación de contraseña...
├── components/           # Componentes Blade reutilizables
├── layouts/              # Plantillas base
├── profile/              # Vistas del perfil
└── dashboard.blade.php
routes/
├── web.php               # Rutas de la aplicación
└── auth.php              # Rutas de autenticación
```

## Instalación y ejecución

### Requisitos

- PHP 8.0.2 o superior
- [Composer](https://getcomposer.org/)
- [Node.js](https://nodejs.org/) y npm
- MySQL (o XAMPP / MariaDB)

### Pasos

```bash
# 1. Clonar el repositorio
git clone https://github.com/belxoch12/laravel-autenticacion.git
cd laravel-autenticacion

# 2. Instalar dependencias
composer install
npm install

# 3. Configurar el entorno
cp .env.example .env
php artisan key:generate
```

4. Edita `.env` con los datos de tu base de datos (`DB_DATABASE`, `DB_USERNAME`, `DB_PASSWORD`).

```bash
# 5. Crear las tablas
php artisan migrate

# 6. Compilar los assets y levantar el servidor
npm run dev
php artisan serve
```

Abre `http://localhost:8000` en el navegador.

## Tecnologías

- **Backend:** Laravel 9, PHP 8, Laravel Breeze, Laravel Sanctum
- **Frontend:** Blade, Tailwind CSS, Alpine.js, Vite
- **Base de datos:** MySQL

## Autoría

Desarrollado por [belxoch12](https://github.com/belxoch12).
