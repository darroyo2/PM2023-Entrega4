# PM2023-Entrega4
# Guía de Instalación y Configuración de Aplicaciones Ionic con Capacitor

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


