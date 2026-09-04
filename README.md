# HtmlCAD 3D - Clon de Tinkercad en un solo archivo

Una aplicación completa de modelado CAD 3D paramétrico y booleano, autocontenida en un único archivo HTML (`index.html`) impulsada por **Babylon.js** y WebGL.

---

## 🌟 Características Principales

- **Arquitectura Monocódigo (Single-File):** Todo el HTML, CSS y lógica JavaScript residen en `index.html`. No requiere instalación de Node.js, compiladores ni servidores; basta con hacer doble clic en el archivo para abrirlo en cualquier navegador moderno.
- **Paradigma Tinkercad:**
  - **Primitivas Básicas:** Cubo, Cilindro, Esfera, Cono, Cuña/Rampa y Toroide/Tubo.
  - **Modo Sólido vs. Hueco:** Cualquier figura puede transformarse en una "perforación" (hueco translúcido con aristas técnicas).
  - **Operación Agrupar (Group / CSG):** Motor de geometría constructiva de sólidos (*Constructive Solid Geometry*) que fusiona sólidos y resta volúmenes huecos instantáneamente mediante operaciones booleanas.
  - **Operación Desagrupar (Ungroup):** Restaura las formas componentes originales conservando sus transformaciones previas.
- **Manipulación Directa y Gizmos:**
  - Manipuladores interactivos de Traslación (W), Rotación (E) y Escala (R).
  - Rejilla magnética milimétrica configurable (1 mm, 5 mm, 10 mm o desactivada).
  - Función **A Suelo (D)** para posar cualquier pieza exactamente sobre el plano de trabajo.
- **Cámara e Interfaz CAD:**
  - Control de órbita con botón izquierdo y paneo con botón derecho/rueda.
  - Botones de vista rápida: `TOP`, `FRONT`, `RIGHT`, `ISO`, y alternador de modo **Perspectiva / Ortográfica**.
  - Inspector contextual con edición de dimensiones numéricas y selector de colores.
- **Exportación e Intercambio:**
  - **STL (ASCII):** Archivos listos para impresión 3D directa en Cura, PrusaSlicer o Bambu Studio.
  - **OBJ:** Malla estándar para importar en Blender u otros programas de renderizado 3D.
  - **Guardar / Cargar JSON:** Serialización completa del proyecto CAD para continuar trabajando en cualquier momento.

---

## ⌨️ Atajos de Teclado

| Atajo | Acción |
| :--- | :--- |
| `Ctrl + G` | **Agrupar** objetos seleccionados (Unión + Diferencia booleana) |
| `Ctrl + Shift + G` | **Desagrupar** el grupo seleccionado |
| `Ctrl + D` | **Duplicar** objeto seleccionado |
| `Del` / `Backspace` | **Borrar** objeto seleccionado |
| `D` | **Soltar a la base** (Drop to Workplane) |
| `W` | Activar Gizmo de **Posición** |
| `E` | Activar Gizmo de **Rotación** |
| `R` | Activar Gizmo de **Escala** |
| `F` | **Enfocar cámara** en el objeto seleccionado |
| `Shift + Clic` | Selección múltiple de objetos |
| `Botón Secundario / Rueda` | Paneo (Desplazamiento de cámara) |
| `Botón Izquierdo` | Órbita 3D alrededor del modelo |

---

## 🚀 Cómo Ejecutar

Simplemente clona o descarga el repositorio y abre `index.html` en tu navegador:

```bash
git clone https://github.com/cdcespon/htmlcad.git
cd htmlcad
# Abre index.html directamente con tu navegador predeterminado:
start index.html   # En Windows
open index.html    # En macOS
xdg-open index.html # En Linux
```

---

## 🛠️ Tecnologías

- **Motor 3D:** [Babylon.js](https://www.babylonjs.com/) (WebGL2 / WebGPU)
- **Geometría Sólida:** `BABYLON.CSG` para operaciones booleanas analíticas
- **UI:** CSS3 nativo moderno con variables y soporte responsive
- **Tipografía:** Google Fonts (`Inter`, `JetBrains Mono`)
