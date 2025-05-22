# 🧭 Localizador de Marcadores Interactivo

## 🏅 Nota estimada: **9 / 10**

> Este proyecto demuestra una integración sólida de geolocalización, lógica condicional y manejo de cuestionarios dinámicos. Está bien estructurado, es interactivo, y tiene un propósito educativo claro.  
>  
> La única posible mejora sería añadir persistencia (para guardar el progreso entre sesiones), validación visual de respuestas correctas o erróneas, o un mapa con los puntos.

---

## 📌 Descripción del proyecto

Este proyecto es una aplicación web que permite localizar distintos **marcadores geográficos** (lugares físicos concretos), y al llegar a uno, lanza un **cuestionario personalizado con tres preguntas**. El sistema detecta automáticamente el marcador más cercano a la ubicación del usuario y guía en qué dirección debe moverse.

Una vez completado un cuestionario, se elimina ese marcador del ciclo y se pasa automáticamente al siguiente marcador más cercano.

---

## 🎯 Funcionalidades principales

- ✅ Detección automática de ubicación del usuario.
- ✅ Cálculo en tiempo real del marcador más cercano.
- ✅ Guía visual con dirección aproximada (N/E/S/O).
- ✅ Preguntas únicas por marcador (3 por cada uno).
- ✅ Evita repetir marcadores ya visitados.
- ✅ Cuestionario visual e interactivo.
- ✅ Diseño responsive y limpio.

---

## 📂 Estructura del proyecto

```
📁 localizador-marcadores/
├── index.html         ← Página principal con todo el HTML, CSS y JS
├── marcadores.json    ← Contiene todos los marcadores y preguntas
```

---

## 🔧 Archivos importantes

### ✅ index.html

Contiene toda la lógica del proyecto:

- HTML para mostrar la distancia, la dirección, y el cuestionario.
- CSS embebido para estilo limpio, moderno y centrado.
- JS para:
  - Cargar los datos de `marcadores.json`.
  - Calcular la distancia con el usuario.
  - Determinar si se ha llegado a un marcador.
  - Lanzar un cuestionario y evitar repetirlo.

---

### ✅ marcadores.json

Contiene los datos de cada marcador. Ejemplo:

```json
{
  "titulo": "Lugar Emblemático",
  "posicion": {
    "lat": 38.84298,
    "lng": 0.10763
  },
  "preguntas": [
    {
      "pregunta": "¿Qué ves?",
      "opciones": ["Una catedral", "Una iglesia", "Un colegio", "Un castillo"],
      "correcta": 4
    },
    ...
  ]
}
```

Cada marcador tiene 3 preguntas, todas con múltiples opciones. La respuesta correcta se indica con un número del 1 al 4.

---

## 💡 Tecnología usada

- **HTML5**
- **JavaScript ES6**
- **CSS básico**
- **API de Geolocalización**
- **JSON para estructura de datos**

---

## 🛠 Mejoras posibles

- Guardar progreso en `localStorage` para que no se borren los marcadores visitados al cerrar la página.
- Añadir un pequeño mapa (Google Maps / Leaflet.js).
- Mostrar si la respuesta es correcta o no.
- Añadir sonidos o animaciones de feedback.
- Mejorar accesibilidad y soporte offline.

---

## 👏 Autor y créditos

Realizado por **[Tu nombre aquí]**  
Trabajo realizado como parte del módulo **DAW / Geolocalización interactiva**.
