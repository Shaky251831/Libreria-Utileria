<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/0150a062-c471-4119-8366-70cceae5b62c" /># Proyecto: Librería de Utilería JS.

**Alumna:** [Marquez Agustin Briseida]  
**Curso:** 2026 Verano 7 a 10 - Programación Web  

---
<img width="589" height="310" alt="Imagen1" src="https://github.com/user-attachments/assets/4dec587a-756c-4801-832f-f6fb4d1b97e5" /><img width="589" height="310" alt="Imagen2" src="https://github.com/user-attachments/assets/03a4f6ae-2cd1-442f-92af-fdd9a6830c88" />

Objetivo: Crear una librería JS funcional (sin frameworks, sin componentes visuales) que usarán en su formulario, modal y login.html
Este proyecto consiste en resolver validación de formularios, formateo seguro de datos y cálculos basados en fechas, garantizando la consistencia de la información antes de ser procesada o enviada a un servidor. 

El proyecto incluye 6 funciones:
1. ValidarCorreo(correo) → boolean — valida formato de correo electrónico
2. soloLetras(texto) → boolean — solo letras mayúsculas/minúsculas, acepta vocales acentuadas
3. validarLongitud(numero, maxLongitud) → boolean — valida longitud de un número
4. calcularEdad(fechaNacimiento) → número entero — calcula edad a partir de fecha de nacimiento
5. esMayorDeEdad(fechaNacimiento) → boolean — valida si es mayor de edad
6. validarPassword(password) → boolean — requiere mayúscula, minúscula, número, carácter especial y mínimo 8 caracteres

Tambien inlcuye las 2 funciones que son capitalizarTexto se refiere lo que el usuario escribe (incluso si lo escribió todo en minúsculas o todo en mayúsculas desordenadas) esto lo corrige.
La otra funcion es limpiarespacios esto se refiere quitar los espacios vacíos que quedan antes de la letra o al darle doble espacio en medio.

---

##  Instalación.

Para utilizar esta librería debemos de poner esta línea de codigo dentro de la página de HTML para que función.

```html
<script src="js/utileria.js"></script>


