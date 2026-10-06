# ⚛️ CyberLab POO VR: Laboratorio Inmersivo de Programación Orientada a Objetos

> **Innovación Educativa Universitaria STEM** | **Recurso Educativo Abierto (REA)** & **Recurso Digital Avanzado (RDA)**  
> Desarrollado con **A-Frame (WebXR/HTML5/JavaScript)** para una experiencia inmersiva accesible desde navegadores web estándar y visores VR (Meta Quest, Pico, HTC Vive, dispositivos móviles).

---

## 🎯 1. Fundamentación Pedagógica y Diseño Instruccional

Aprender **Programación Orientada a Objetos (POO)** suele presentar una barrera cognitiva inicial debido al alto grado de abstracción que requieren conceptos como *Clase*, *Instancia*, *Herencia* y *Mutabilidad de Estado*.

Este laboratorio virtual traslada la abstracción teórica a un **modelo mental visual y espacial 3D**, apoyado en la teoría del **aprendizaje experiencial de Kolb** y el **anclaje visual tridimensional**:

| Concepto POO | Metáfora Visual en VR | Interacción del Estudiante |
| :--- | :--- | :--- |
| **Clase (Molde / Plano)** | Diagrama de código holográfico azul (`class Vehiculo`). No tiene masa ni existe en el mundo físico aún. | El estudiante analiza los atributos (`color`, `escala`) y métodos (`acelerar()`). |
| **Operador `new` e Instanciación** | Rayo de síntesis láser sobre la plataforma central. | Al pulsar `new Vehiculo()`, el rayo materializa un vehículo 3D tangible en el pedestal. |
| **Objeto / Instancia en Heap** | Objeto 3D interactivo con dirección de memoria simulada (ej. `#0x8F42`). | El alumno examina el *Inspector de Memoria* que vuelca en tiempo real el estado de RAM. |
| **Herencia (`extends`)** | Árbol genealógico con código padre e hijo. Al instanciar subclases (`AutoDeportivo` o `Camion`), se visualiza qué partes son heredadas (chasis base) y cuáles son exclusivas (alerón/turbo o tolva de carga). | El estudiante comprueba cómo la subclase reutiliza el comportamiento base y añade nuevas capacidades. |
| **Mutación de Estado** | Selector de color en tiempo real (esferas 3D) y modificadores de escala (`+` / `-`). | Al modificar un atributo, la geometría del objeto cambia al instante, sin alterar el plano de la Clase original. |
| **Recolector de Basura (GC)** | Botón de destrucción de referencia en memoria (`delete GC`). | El objeto desaparece y la dirección de memoria vuelve a `Null`, demostrando el ciclo de vida del objeto. |

---

## 🚀 2. Guía de Ejecución

Esta aplicación fue construida bajo el principio de **cero dependencias locales**, lo que significa que no requiere instalación de Node.js, compiladores ni servidores dedicados.

### Opción A: Ejecución Directa (Doble Clic)
1. Abre el archivo [`index.html`](file:///Users/jhonmendex/Downloads/poo/index.html) directamente en cualquier navegador moderno (Google Chrome, Firefox, Microsoft Edge, Safari o Brave).

### Opción B: Servidor Local Rápido (Recomendado para VR en red local)
Si deseas proyectar a unas gafas Meta Quest conectadas a la misma red WiFi:
```bash
# Con Python 3:
python3 -m http.server 8000

# Con Node (npx):
npx serve .
```
Luego entra desde el navegador de las gafas VR a: `http://<IP-DE-TU-PC>:8000`.

---

## 🕹️ 3. Modos de Control y Accesibilidad

- **🖥️ Modo Escritorio (PC / Mac):**
  - **Mirar / Rotar cámara:** Clic y arrastrar con el mouse.
  - **Interactuar con botones:** Clic izquierdo sobre los botones 3D (el cursor circular detecta colisiones).
  - **Moverse en el laboratorio:** Teclas `W`, `A`, `S`, `D`.
  - **Guía 2D:** Panel de ayuda flotante en la esquina superior izquierda (se puede ocultar).
- **🥽 Modo Visor VR (Meta Quest / HTC / Pico):**
  - Pulsa el botón **"Enter VR"** en la esquina inferior derecha.
  - Usa los mandos 6DoF con puntero láser o el cursor de mirada para interactuar con los botones físicos y esferas de colores.
- **📱 Modo Smartphone / Google Cardboard:**
  - Soporte giroscópico con retícula central para selección por mirada.

---

## 🛠️ 4. Arquitectura Técnica

- **A-Frame v1.5.0:** Framework de realidad virtual WebXR basado en Three.js.
- **Entorno Procedural:** `aframe-environment-component` para renderizado del laboratorio estelar sin descargas pesadas de assets.
- **Motor de Audio Sintetizado (`SoundEngine`):** Utiliza la **Web Audio API** de HTML5 con osciladores sinusoidales y de diente de sierra para emitir feedback háptico/acústico sin depender de archivos de audio externos (eliminando errores de CORS o enlaces rotos).
- **Programación Orientada a Objetos en JS Real:** La lógica subyacente implementa clases ES6 puras (`Vehiculo`, `AutoDeportivo`, `Camion`) que gestionan la memoria y sincronizan sus valores con los componentes A-Frame.

---

## 📚 5. Licencia y Uso Académico

Este proyecto es un **Recurso Educativo Abierto (REA)** licenciado bajo los términos del archivo [`LICENSE`](file:///Users/jhonmendex/Downloads/poo/LICENSE), disponible para libre distribución, adaptación y uso en cátedras universitarias y talleres de informática y programación.
