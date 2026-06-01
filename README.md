# Laboratorio: Carga Automática (Autoload) con PSR-4 en Laravel

## Información General

**Estudiante:** Maryennis Deans  
**Profesora:** Irina Fong  
**Asignatura:** IGS132  

---

## Fecha de Ejecución

31 de mayo de 2026

---

## Objetivo

Implementar el mecanismo de carga automática de clases utilizando el estándar PSR-4 mediante Composer dentro del framework Laravel, permitiendo una mejor organización del código y facilitando el mantenimiento de la aplicación.

---

## Requisitos Previos

Antes de ejecutar el laboratorio es necesario contar con:

- PHP 8.x o superior
- Composer instalado
- Laravel instalado
- Servidor local (XAMPP, Laragon o similar)
- Navegador web
- Base de datos MySQL

---

## Ecosistema de Laravel

Laravel es un framework de desarrollo web para PHP que sigue el patrón de arquitectura MVC (Modelo-Vista-Controlador). Proporciona herramientas modernas para la creación de aplicaciones web robustas y escalables.

Entre sus principales características se encuentran:

- Sistema de rutas.
- Migraciones para bases de datos.
- ORM Eloquent.
- Motor de plantillas Blade.
- Gestión de dependencias mediante Composer.
- Compatibilidad con estándares PSR.

Laravel permite desarrollar aplicaciones de forma organizada, segura y eficiente.

---

## Modelo MVC

Laravel utiliza el patrón de arquitectura MVC (Modelo-Vista-Controlador).

### Modelo (Model)

Representa los datos y la lógica de negocio de la aplicación. Gestiona la interacción con la base de datos utilizando Eloquent ORM.

### Vista (View)

Se encarga de mostrar la información al usuario mediante plantillas Blade.

### Controlador (Controller)

Recibe las solicitudes del usuario, procesa la información y comunica los modelos con las vistas.

---

## Principales Carpetas de Laravel

### app/

Contiene los modelos, controladores y demás clases principales de la aplicación.

### routes/

Contiene la definición de las rutas de acceso al sistema.

### resources/

Almacena vistas Blade, archivos CSS y JavaScript.

### database/

Contiene migraciones, seeders y factories.

### public/

Es el directorio público de acceso a la aplicación.

### config/

Almacena archivos de configuración del proyecto.

### vendor/

Contiene todas las dependencias instaladas mediante Composer y el sistema de carga automática PSR-4.

---

## Implementación de PSR-4 y Composer

Para este laboratorio se utilizó Composer para implementar la carga automática de clases siguiendo el estándar PSR-4.

### Configuración de composer.json

```json
{
    "autoload": {
        "psr-4": {
            "App\\": "app/"
        }
    }
}
```

### Generación del Autoload

Se ejecutó el siguiente comando:

```bash
composer dump-autoload
```

Este comando permite regenerar automáticamente los archivos de carga y registrar las nuevas clases creadas dentro del proyecto.

---

## Base de Datos

Se utilizó MySQL como sistema gestor de bases de datos.

### Configuración

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=nombre_base_datos
DB_USERNAME=root
DB_PASSWORD=
```

Las migraciones de Laravel permitieron crear y administrar la estructura de las tablas utilizadas por la aplicación.

---

## Resultados Obtenidos

Durante el desarrollo del laboratorio se logró:

- Implementar correctamente el estándar PSR-4.
- Utilizar Composer para gestionar las dependencias del proyecto.
- Automatizar la carga de clases sin utilizar include o require.
- Mantener una estructura organizada del código.
- Facilitar el mantenimiento y la escalabilidad de la aplicación.

---

## Imagen que Muestre el Resultado

Inserte aquí una captura de pantalla del resultado obtenido durante la ejecución del laboratorio.

```
<img width="842" height="260" alt="Captura de pantalla 2026-05-31 193905" src="https://github.com/user-attachments/assets/62970692-1943-4829-adfd-0710dbf70576" />

---

## Dificultades y Soluciones

### Dificultad 1

Las clases creadas no eran reconocidas automáticamente por Laravel.

**Solución:**

Ejecutar:

```bash
composer dump-autoload
```

para regenerar los archivos de carga automática.

### Dificultad 2

Errores relacionados con namespaces incorrectos.

**Solución:**

Verificar que los namespaces definidos en las clases coincidieran con la estructura configurada en PSR-4 dentro del archivo composer.json.

---

## Puntos de Referencia

- Documentación oficial de Laravel.
- Documentación oficial de Composer.
- Estándar PSR-4 de PHP-FIG.
- Material proporcionado por la profesora Irina Fong.

---

## Footer

Universidad Tecnológica de Panamá

Facultad de Ingeniería de Sistemas Computacionales

Asignatura: IGS132

Profesora: Irina Fong

Estudiante: Maryennis Deans
