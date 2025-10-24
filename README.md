**# Inventario con Lista Doblemente Enlazada Ordenada

Este es un proyecto simple que implementa un sistema básico de inventario utilizando una **lista doblemente enlazada ordenada** como estructura de datos principal. El inventario gestiona productos con los siguientes campos:
* Código (usado para el ordenamiento)
* Nombre
* Cantidad
* Costo

Toda la lógica está contenida en un único archivo `index.html`, que incluye el HTML para la interfaz, CSS para los estilos y JavaScript (ES6+) para la funcionalidad y la lógica de la estructura de datos.

---

## 🚀 Características

La interfaz permite al usuario realizar las siguientes operaciones sobre el inventario:

* **Agregar Producto**: Inserta un nuevo producto en la lista. La inserción se realiza en la posición correcta para mantener la lista ordenada por **código** (de menor a mayor). No se permiten códigos duplicados.
* **Buscar por Código**: Busca un producto usando su código. Esta búsqueda está **optimizada**: dado que la lista está ordenada, la búsqueda se detiene si el código actual en la iteración es mayor que el código buscado, evitando recorridos innecesarios.
* **Eliminar por Código**: Encuentra un producto por su código y lo elimina de la lista, reajustando los punteros `next` y `prev` correspondientes.
* **Listar (Ordenado)**: Muestra un listado de todos los productos en la consola de operaciones, recorriendo la lista desde `head` (primero) hasta `tail` (último).
* **Listar (Inverso)**: Muestra el listado recorriendo la lista en orden inverso, desde `tail` hasta `head`.
* **Extraer Primero**: Obtiene y elimina el primer elemento de la lista (`head`).
* **Extraer Último**: Obtiene y elimina el último elemento de la lista (`tail`).

Además, la interfaz cuenta con un `div` de "Detalle de Operaciones" que actúa como un log, mostrando el resultado de cada acción realizada (ej: "Producto agregado", "Error: código ya existe", "Producto no encontrado", etc.).

---

## 🏗️ Estructura de Datos

El núcleo del programa se basa en tres clases de JavaScript:

1.  **`Producto`**: Una clase simple que almacena los datos de cada ítem (código, nombre, cantidad, costo).
2.  **`Nodo`**: El bloque de construcción de la lista. Almacena `data` (una instancia de `Producto`) y dos punteros: `next` (apunta al siguiente nodo) y `prev` (apunta al nodo anterior).
3.  **`Inventario`**: La clase principal que gestiona la lista doblemente enlazada. Mantiene referencias al inicio (`head`) y al final (`tail`) de la lista y contiene todos los métodos de lógica de negocio (agregar, buscar, eliminar, etc.).

La principal característica es que el método `agregar` no solo añade al final, sino que recorre la lista para encontrar la posición correcta donde insertar el nuevo `Nodo` basándose en el `codigo` del producto, asegurando que la lista siempre permanezca ordenada.

---

## 💻 Tecnologías Utilizadas

* **HTML5**: Para la estructura de la interfaz y los campos de entrada.
* **CSS3**: Para los estilos de la página, el layout (usando Grid) y la apariencia de los botones y el log.
* **JavaScript (ES6+)**: Para toda la lógica de la estructura de datos (clases, nodos, punteros) y la manipulación del DOM.

---

## 🛠️ Cómo Usar

No se requiere instalación, dependencias ni un servidor web.

1.  Clona este repositorio o descarga el archivo `index.html`.
2.  Abre el archivo `index.html` en cualquier navegador web moderno (como Google Chrome, Firefox, Microsoft Edge, etc.).
3.  Interactúa con la interfaz para gestionar el inventario.**
