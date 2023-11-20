# ENTREGA 4

## Guía de Instalación y Configuración de Aplicaciones Ionic con Capacitor

Ionic es un marco de desarrollo de código abierto para la creación de aplicaciones móviles y web utilizando tecnologías web estándar como HTML, CSS y JavaScript/TypeScript. Ionic es una opción popular para el desarrollo de aplicaciones móviles y web, especialmente para aquellos que desean aprovechar las tecnologías web existentes y desplegar aplicaciones en múltiples plataformas de manera eficiente.

## 1. Instalación de Ionic CLI

Para comenzar, abre la línea de comandos y ejecuta el siguiente comando para instalar globalmente Ionic CLI:

```bash
npm install -g @ionic/cli
```

## 2. Crear la Aplicación

Dirígete al directorio donde deseas crear la aplicación utilizando el comando `cd nombreCarpeta`. A continuación, ejecuta el siguiente comando para crear la aplicación:

```bash
ionic start myApp blank --type=react
```

## 3. Añadir Capacitor

Ingresa al directorio de la aplicación recién creada:

```bash
cd myApp
```

Añade Capacitor a la aplicación con el siguiente comando:

```bash
ionic cap add android
```

## 4. Abrir la Aplicación con Capacitor

Abre la aplicación en Android Studio utilizando el siguiente comando:

```bash
ionic cap open android
```

Asegúrate de habilitar las integraciones de Ionic con Capacitor mediante el siguiente comando:

```bash
ionic integrations enable capacitor
```

## 5. Configuración de Gradle y Variables de Entorno

### Agregar Gradle al PATH de Windows

1. Descarga Gradle desde el sitio oficial y extrae la carpeta comprimida. 
**Gradle:**
   - [Gradle - Sitio Oficial](https://gradle.org/)

2. Copia la ruta de la carpeta "bin" de Gradle.

3. Edita las variables de entorno en Windows y añade la ruta copiada a la variable PATH.

   - Si la variable ya existe, haz doble clic y luego en "Nuevo", añade la ruta.

### Crear la Variable JAVA_HOME

1. Abre la línea de comandos en `Windows\System32`.

2. Ejecuta el siguiente comando para crear la variable `JAVA_HOME`:

   ```bash
   setx /m JAVA_HOME "Ruta_jdk"
   ```
   En caso no tengas Java Development Kit descárgalo del sitio oficial:
   **OpenJDK (Java Development Kit):**
   - [OpenJDK - Sitio Oficial](https://openjdk.java.net/)
   
3. Comprueba que la variable se haya creado correctamente:

   ```bash
   echo %JAVA_HOME%
   ```

## 6. Ejecutar la Aplicación

Abre la línea de comandos en el directorio de la aplicación y ejecuta la aplicación en Android:

```bash
ionic cap run android
```

## 7. Instalación de Gradle for Java en Visual Studio Code

Si trabajas con Visual Studio Code, instala la extensión "Gradle for Java" para facilitar el desarrollo y la gestión de dependencias Gradle.

# Guía de Instalación de Visual Studio Code

Visual Studio Code (VS Code) es un entorno de desarrollo integrado (IDE) gratuito y de código abierto desarrollado por Microsoft. Visual Studio Code es un editor de código ligero pero potente que se ha vuelto muy popular entre los desarrolladores debido a su flexibilidad, extensibilidad y amplio soporte para diversos lenguajes de programación.

## 1. Descargar e Instalar Visual Studio Code

Dirígete al [sitio oficial de Visual Studio Code](https://code.visualstudio.com/) y descarga la versión.

## 2. Instalación de Visual Studio Code

Ejecuta el archivo de instalación descargado. Durante la instalación, asegúrate de marcar la opción "Agregar a la variable de entorno PATH" para facilitar el acceso a VS Code desde la línea de comandos.

# Guía de Instalación de Android Studio

Android Studio es el entorno de desarrollo oficial para la creación de aplicaciones Android. Android Studio es una herramienta integral que brinda a los desarrolladores todas las herramientas necesarias para diseñar, desarrollar, depurar y optimizar aplicaciones Android de manera eficiente.

## 1. Descargar e Instalar Android Studio

Dirígete al [sitio oficial de Android Studio](https://developer.android.com/studio) y descarga la última versión.

## 2. Instalación de Android Studio

Ejecuta el archivo de instalación descargado y sigue el asistente de instalación. Durante la instalación, asegúrate de seleccionar "Android Virtual Device" (AVD) para utilizar emuladores.

## 3. Configuración de Android Studio

Abre Android Studio y sigue el asistente de configuración inicial. Esto incluirá la instalación de componentes esenciales, configuración del SDK de Android y la descarga de cualquier actualización disponible.

## 4. Crear un Dispositivo Virtual

Abre Android Studio, accede a "AVD Manager" y crea un nuevo dispositivo virtual.

## Diagrama de despliegue

![Diagrama despligue](https://github.com/darroyo2/PM2023-Entrega4/blob/main/DeploymentDiagram2.jpg)

## Requisitos no Funcionales

### 1. Disponibilidad
En términos de disponibilidad, la aplicación móvil se beneficiará de la arquitectura distribuida y la implementación en Replit para el backend. Replit utiliza Node.js para la lógica del servidor, asegurando que la plataforma esté siempre accesible. La capacidad de Replit para gestionar múltiples instancias de forma automática proporciona una mayor disponibilidad, permitiendo a los usuarios acceder a la plataforma en cualquier momento del día.

### 2. Seguridad
La seguridad es una prioridad ya que se busca almacenar de manera segura la información confidencial de los usuarios. Firebase Crashlytics puede proporcionar informes detallados en caso de fallos, permitiendo una respuesta rápida a posibles amenazas y garantizando la integridad del sistema. Además, la lógica de seguridad en el backend implementada en Node.js en Replit contribuirá a la protección contra posibles vulnerabilidades y ataques cibernéticos.

### 3. Calidad
La calidad de la aplicación se garantiza mediante la integración de Firebase Analytics, que proporciona información detallada sobre el uso de la aplicación. Esta información puede utilizarse para evaluar la eficacia y eficiencia de las características implementadas. A través de la recopilación de datos, se asegura que la aplicación cumpla con las expectativas y requisitos de los usuarios, proporcionando una experiencia de usuario satisfactoria en el contexto de un gimnasio.

### 4. Escalabilidad
La escalabilidad del sistema está respaldada por Replit, que permite manejar un aumento en la carga de trabajo. La capacidad de Replit para escalar automáticamente en función de la demanda asegura que la aplicación pueda admitir un mayor número de usuarios sin degradación del rendimiento. Esto es esencial para una aplicación de gimnasio, donde la demanda puede aumentar con el tiempo.

### 5. Usabilidad
La usabilidad de la aplicación se centra en una interfaz intuitiva y fácil de navegar. La combinación de Firebase Analytics y Firebase Crashlytics también proporciona información valiosa para mejorar continuamente la usabilidad de la aplicación, asegurando que los usuarios puedan programar entrenamientos y acceder a la información de manera sencilla.

### 6. Eficiencia
La eficiencia se logra mediante el uso de tecnologías como Firebase Analytics para evaluar el rendimiento de las características implementadas. Además, Replit, al utilizar Node.js en el backend, contribuye a un procesamiento eficiente de datos y tiempos de carga rápidos. La eficiencia en el uso de los recursos del sistema es fundamental para garantizar un rendimiento óptimo en la aplicación móvil del gimnasio.

## Diagrama de casos de uso

![Diagrama caso uso](https://github.com/darroyo2/PM2023-Entrega4/blob/main/Casos%20de%20Uso.jpg)

## Descripción de casos de uso

### 1. **Acceder al sistema (login):**
   - *Descripción:* Este caso de uso permite a los usuarios autenticarse en la aplicación. Los usuarios ingresarán su nombre de usuario y contraseña para acceder a sus cuentas personales. Si la autenticación es exitosa, se les dará acceso a las funciones y datos relacionados con su perfil.

![login](https://github.com/darroyo2/PM2023-Entrega4/blob/main/login.png)

### 2. **Cambiar contraseña:**
   - *Descripción:* Este caso de uso permite a los usuarios cambiar su contraseña actual por una nueva. Los usuarios deberán proporcionar su DNI y su correo electrónico y luego ingresar la nueva contraseña. Después, el sistema enviará un mensaje notificando al usuario sobre el éxito o cualquier problema relacionado con el cambio de contraseña.

![cambiar contraseña](https://github.com/darroyo2/PM2023-Entrega4/blob/main/cambiar%20contrase%C3%B1a.png)

### 3. **Mostrar Rutina:**
   - *Descripción:* Este caso de uso está dirigido a los alumnos y les permite visualizar la rutina de ejercicios asignada. La aplicación mostrará la lista de ejercicios con sus imágenes respectivas.

![rutina](https://github.com/darroyo2/PM2023-Entrega4/blob/main/rutina.png)

### 4. **Mostrar Ejercicios:**
   - *Descripción:* Este caso de uso proporciona a los alumnos la capacidad de ver todos los ejercicios disponibles en la aplicación. Puede mostrar una lista completa de ejercicios con sus respectivas imágenes.
     
![ejercicios](https://github.com/darroyo2/PM2023-Entrega4/blob/main/todos%20los%20ejercicios.png)

### 5. **Mostrar Integrantes:**
   - *Descripción:* Este caso de uso permite a los usuarios ver la lista de integrantes del grupo de desarrollo. Puede mostrar información básica sobre cada integrante, como nombre y código. Se mostrará dicho diálogo mediante un botón en el menú superior.
     
![integrantes](https://github.com/darroyo2/PM2023-Entrega4/blob/main/integrantes.png)
