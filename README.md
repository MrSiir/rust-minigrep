# Minigrep

Minigrep es una implementación sencilla de una herramienta de búsqueda en archivos, es un programa de ejemplo del capitulo 12 del libro _The Rust Programming Language_ (https://doc.rust-lang.org/book/ch12-00-an-io-project.html) titulado _An I/O Project: Building a Command Line Program_.

## Requisitos

- [Rust](https://www.rust-lang.org/) instalado en tu sistema.

## Instalación

Clona este repositorio y compila el proyecto:

```bash
git clone https://github.com/MrSiir/rust-minigrep
cd minigrep
cargo build
```

## Uso

Ejecuta el programa pasando los argumentos en el siguiente formato:

```bash
cargo run -- <QUERY> <FILE_PATH>
```

Donde:

- `<QUERY>` es la cadena que deseas buscar.
- `<FILE_PATH>` es la ruta del archivo donde deseas buscar.

### Ejemplo

Supongamos que tienes un archivo llamado `example.txt` con el siguiente contenido:

```
Rust es un lenguaje de programación rápido.
Amo trabajar con Rust.
Escribir software en Rust es divertido.
```

Para buscar la palabra "Rust", ejecuta:

```bash
cargo run -- Rust example.txt
```

El programa devolverá:

```
Rust es un lenguaje de programación rápido.
Amo trabajar con Rust.
Escribir software en Rust es divertido.
```

### Ignorar mayúsculas/minúsculas

Para realizar una búsqueda insensible a mayúsculas, establece la variable de entorno `IGNORE_CASE` antes de ejecutar el programa:

```bash
IGNORE_CASE=1 cargo run -- rust example.txt
```

Esto devolverá las mismas líneas que en el ejemplo anterior.

## Estructura del proyecto

- **`main.rs`**: Punto de entrada principal del programa.
- **`lib.rs`**: Contiene la lógica principal, incluyendo:
  - Construcción de la configuración (`Config`).
  - Función `run` para ejecutar el programa.
  - Funciones `search` y `search_case_insensitive` para realizar las búsquedas.

## Pruebas

Para ejecutar las pruebas, utiliza el siguiente comando:

```bash
cargo test
```

Esto verificará que las funciones `search` y `search_case_insensitive` funcionan correctamente.

## Licencia

Este proyecto está licenciado bajo [MIT License](LICENSE).

Este fichero ha sido generado por ChatGPT.
