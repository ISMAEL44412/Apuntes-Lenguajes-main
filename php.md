- [Introduccion a PHP](#introduccion-a-php)
- [Instalación](#instalación)
  - [En Windows](#en-windows)
    - [Opción 1: Descargar PHP manualmente](#opción-1-descargar-php-manualmente)
    - [Opción 2: Usar XAMPP](#opción-2-usar-xampp)
  - [En macOS](#en-macos)
    - [Usando Homebrew](#usando-homebrew)
    - [Usando MacPorts](#usando-macports)
  - [En Linux (Ubuntu/Debian)](#en-linux-ubuntudebian)
    - [Con Apache](#con-apache)
    - [Con Nginx](#con-nginx)
  - [Verificar instalación](#verificar-instalación)
  - [Servidor web integrado](#servidor-web-integrado)
- [Sintaxis](#sintaxis)
  - [Variables](#variables)
    - [Reglas para variables en PHP](#reglas-para-las-variables-en-php)
    - [Ambito para escribir Variables](#ambito-para-escribir-variables)

# Introduccion a PHP

Es un lenguaje de programación de servidores y una potente herramienta para crear páginas web dinámicas e interactivas.

- Significa Hypertext Preprocessor (Preprocesador de hipertexto).
- Sus scripts se ejecutan en el servidor.

**PHP7** apartir de aqui se admiten nuevos operadores como el de nave espacial `<=>`.

## Instalación

### En Windows

#### Opción 1: Descargar PHP manualmente

1. **Descargar PHP**

   - Accede a [php.net/downloads](https://www.php.net/downloads)
   - Descarga la versión Thread Safe (TS) en formato ZIP
   - Recomendado: PHP 8.2 o superior

2. **Extraer archivos**

   - Extrae el archivo ZIP en una carpeta como `C:\php`

3. **Configurar el PATH**

   - Abre **Variables de entorno** (Busca en Inicio: "variables de entorno")
   - Ve a **Variables de entorno > PATH**
   - Agrega `C:\php` a la lista
   - Reinicia la terminal

4. **Verificar instalación**
   ```bash
   php -v
   ```

#### Opción 2: Usar XAMPP (Recomendado para principiantes)

1. Descarga **XAMPP** desde [apachefriends.org](https://www.apachefriends.org)
2. Ejecuta el instalador
3. Selecciona Apache, MySQL, PHP
4. Instala en `C:\xampp`
5. Inicia Apache y MySQL desde el panel de control de XAMPP
6. Verifica: abre `http://localhost` en tu navegador

### En macOS

#### Usando Homebrew

```bash
brew install php
php -v
```

#### Usando MacPorts

```bash
sudo port install php82
```

### En Linux (Ubuntu/Debian)

```bash
sudo apt update
sudo apt install php php-cli php-mysql php-curl php-json
php -v
```

#### Con Apache

```bash
sudo apt install php libapache2-mod-php
sudo systemctl restart apache2
```

#### Con Nginx

```bash
sudo apt install php-fpm php-mysql
sudo systemctl start php8.2-fpm
```

### Verificar instalación

```bash
# Ver versión de PHP
php -v

# Ver información de configuración
php -i

# Crear archivo de prueba
echo "<?php echo 'Hola PHP'; ?>" > test.php
php test.php
```

### Servidor web integrado

PHP incluye un servidor de desarrollo integrado:

```bash
# Inicia el servidor en localhost:8000
php -S localhost:8000

# Inicia en un puerto específico
php -S localhost:3000
```

Accede a `http://localhost:8000` en tu navegador.

# Sintaxis

Un script PHP comienza con `<?php` y finaliza con `?>`, su extención debe ser `.php` y sus instrucciónes finalizan con `;`.

Un comentario puede iniciar con `#` o `//`, y un comentario multiple-lineas inicia con `/*` y finaliza con `*/`

```php
<?php
# Codigo aqui
?>
```

## Variables

Una variable comienza con `$` seguido del nombre

```php
<?php
$x = 5;
$y = 'Jhonn';
?>
```

### Reglas para las variables en PHP

- Inicia con `$` seguido de su nombre.
- debe iniciar con una letra o con `_`.
- No puede comenzar con un número.
- Solo puede contener caracteres alfanúmericos `(Az, 0-9 y _)`.

### Ambito para escribir variables

Es la parte del script donde se puede hacer referencia a dicha variable o utilizarla.
Existen tres ámbitos diferentes:

- Local:
- Global
- Estático `static`

`Alcance Global`: Es una variable declarada fuera de una función y solo se puede acceder a ella fuera de una función.

```php
<?php
$x = 5;

function myTest() {
    echo "Variable x inside is : $x";
}
myTest();
echo "Variable x outside is : $x";
?>
```

`Alcance Local`: Es una variable declarada dentro de una función y solo se puede acceder a ella dentro de esa función

```php
<?php
function myTest() {
    $x = 5;
    echo "Variable x inside is : $x";
}
myTest();

echo "Variable x outside is : $x";
?>
```
