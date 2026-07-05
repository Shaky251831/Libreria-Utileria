Proyecto: Librería de Utilería JS.

**Alumna:** [Marquez Agustin Briseida]  
**Curso:** 2026 Verano 7 a 10 - Programación Web  

---

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


##  Instalación.

Para utilizar esta librería debemos de poner esta línea de codigo dentro de la página de HTML para que función.

```html
<script src="js/utileria.js"></script>

---
// 1. Validar formato de correo electrónico
function validarCorreo(correo) {
    const regex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
    return regex.test(correo);
}

// 2. Solo letras (mayúsculas/minúsculas, acepta espacios y vocales acentuadas)
function soloLetras(texto) {
    const regex = /^[a-zA-ZáéíóúÁÉÍÓÚñÑ\s]+$/;
    return regex.test(texto);
}

// 3. Valida la longitud máxima de dígitos de un número
function validarLongitud(numero, maxLongitud) {
    return String(numero).length <= maxLongitud;
}

// 4. Calcula edad exacta a partir de una fecha de nacimiento (YYYY-MM-DD)
function calcularEdad(fechaNacimiento) {
    if (!fechaNacimiento) return 0;
    const hoy = new Date();
    const cumpleanos = new Date(fechaNacimiento);
    let edad = hoy.getFullYear() - cumpleanos.getFullYear();
    const mes = hoy.getMonth() - cumpleanos.getMonth();
    
    if (mes < 0 || (mes === 0 && hoy.getDate() < cumpleanos.getDate())) {
        edad--;
    }
    return edad;
}

// 5. Valida si es mayor de edad (18 años o más)
function esMayorDeEdad(fechaNacimiento) {
    return calcularEdad(fechaNacimiento) >= 18;
}

// 6. Requiere mayúscula, minúscula, número, carácter especial y mínimo 8 caracteres
function validarPassword(password) {
    const tieneMayuscula = /[A-Z]/.test(password);
    const tieneMinuscula = /[a-z]/.test(password);
    const tieneNumero = /[0-9]/.test(password);
    const tieneEspecial = /[\W_]/.test(password);
    const largoCorrecto = password.length >= 8;

    return tieneMayuscula && tieneMinuscula && tieneNumero && tieneEspecial && largoCorrecto;
}

// --- Las 2 Funciones que agregue ---

// 1. Limpiar espacios extra al inicio, final y duplicados en medio
function limpiarEspacios(texto) {
    return texto.trim().replace(/\s+/g, ' ');
}

// 2.- Capitalizar la primera letra de cada palabra (Formato de Nombre Propio)
function capitalizarTexto(texto) {
    return texto.toLowerCase().replace(/\b\w/g, l => l.toUpperCase());
}

----
## Capturas de pantalla
<img width="589" height="310" alt="Imagen2" src="https://github.com/user-attachments/assets/a00805eb-3ea7-4d32-93b1-09fe5ff83d54" />
<img width="589" height="310" alt="Imagen1" src="https://github.com/user-attachments/assets/b32de371-8fc6-4c33-80f8-d0a203f77a62" />

