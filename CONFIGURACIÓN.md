# ⚙️ CONFIGURACION VISUAL DEL SITIO WEB  
### 🏷️ Proyecto: Power Group — Marca Gamer de Compuoriente Import And Expor Ltda.  
**Versión actual:** 1.0  
**Desarrollado por:** JSFRAY  
**Derechos reservados:** Power Group  

---

## 🧩 Componentes Principales del Código

---

### 1️⃣ MODAL  
**¿Qué es?**  
Una ventana emergente que aparece sobre todo el contenido.  

**¿Para qué sirve?**  
Cuando haces clic en una imagen de producto, se abre el modal mostrando la imagen ampliada en el centro de la pantalla con fondo oscuro.  

**Elementos que lo componen:**  
- `.modal` → Contenedor de fondo oscuro  
- `.modal-content` → Imagen ampliada  
- `.close` → Botón “X” para cerrar  

**Ejemplo:**  
Haces clic en la foto de un chasis → se abre grande en pantalla completa → presionas X o ESC para cerrar.  

---

### 2️⃣ CAROUSEL (Carrusel)  
**¿Qué es?**  
Un deslizador de imágenes, como una galería que se mueve horizontalmente.  

**¿Para qué sirve?**  
Mostrar varias fotos del mismo producto sin ocupar mucho espacio. Las imágenes se deslizan de izquierda a derecha.  

**Elementos que lo componen:**  
- `.carousel-container` → Contenedor general  
- `.carousel-images` → Imágenes en fila horizontal  
- `.carousel-btn.prev-btn` → Flecha ◄ (imagen anterior)  
- `.carousel-btn.next-btn` → Flecha ► (imagen siguiente)  
- `.carousel-dots` → Círculos inferiores  
- `.dot` → Cada círculo individual  

**Ejemplo:**  
Un producto tiene 3 fotos → aparecen círculos ⚫⚫⚫ → haces clic en las flechas o círculos para ver cada imagen.  

---

### 3️⃣ GRID  
**¿Qué es?**  
Un sistema de cuadrícula que organiza las tarjetas automáticamente.  

**¿Para qué sirve?**  
Coloca las tarjetas de productos en filas y columnas, adaptándose al tamaño de pantalla.  

**Elementos:**  
- `.chasis-grid`  
- `.escritorio-grid`  
- `.enfriamiento-grid`  
- `.productos-grid`  

**Ejemplo:**  
En PC verás 3-4 productos por fila, en tablet 2, en móvil 1.  

---

### 4️⃣ CARD (Tarjeta)  
**¿Qué es?**  
Cada recuadro individual de producto.  

**¿Para qué sirve?**  
Mostrar la información de un producto: fotos, nombre, características.  

**Elementos:**  
- `.chasis-card`  
- `.escritorio-card`  
- `.enfriamiento-card`  
- `.productos-card`  

**Ejemplo:**  
Cada caja que contiene un chasis es una “card”.  

---

### 5️⃣ RIBBON (Cinta diagonal)  
**¿Qué es?**  
Una etiqueta decorativa diagonal.  

**¿Para qué sirve?**  
Marcar productos como “NUEVO” con un banner llamativo.  

**Elemento:**  
- `.ribbon-diagonal`  

**Ejemplo:**  
La cinta dorada con texto rojo “NUEVO” en la esquina superior izquierda.  

---

### 6️⃣ SEARCH CONTAINER (Buscador)  
**¿Qué es?**  
Una barra de búsqueda.  

**¿Para qué sirve?**  
Filtrar productos escribiendo palabras clave.  

**Elemento:**  
- `.search-container`  
- `#searchInput`  

**Ejemplo:**  
Escribes “W82” y solo aparecen los chasis W82 Black y White.  

---

### 7️⃣ INFO (Información del producto)  
**¿Qué es?**  
El texto descriptivo debajo de las imágenes.  

**¿Para qué sirve?**  
Mostrar las especificaciones y características del producto.  

**Elementos:**  
- `.chasis-info`  
- `.escritorio-info`  
- `.enfriamiento-info`  
- `.productos-info`  

**Ejemplo:**  
“• Fuente de poder POWER GROUP 350W”  

---

### 8️⃣ DOTS (Círculos indicadores)  
**¿Qué es?**  
Pequeños círculos debajo del carrusel.  

**¿Para qué sirve?**  
Indicar cuántas imágenes hay y cuál estás viendo actualmente.  

**Elementos:**  
- `.carousel-dots`  
- `.dot`  
- `.dot.active` → Círculo con efecto RGB  

**Ejemplo:**  
⚫🟢⚫ → estás viendo la imagen 2 de 3.  

-------------------------------------------------------------------------

### 9️⃣ SECTION (Sección)  
**¿Qué es?**  
Contenedor que agrupa productos por categoría.  

**¿Para qué sirve?**  
Separar chasis, escritorios, enfriamiento y otros productos.  

**Elementos:**
```html
<section id="chasis">
<section id="escritorios">
<section id="enfriamiento">
<section id="productos">

# 📚 Guía Completa: Agregar Secciones y Productos

## 📑 Índice
1. [Cómo Crear una Nueva Sección](#parte-1-crear-nueva-sección)
2. [Cómo Agregar un Producto](#parte-2-agregar-un-producto)
3. [Checklist de Verificación](#checklist-final)

---

# PARTE 1: CREAR NUEVA SECCIÓN

## 🎯 Objetivo
Crear una sección completamente nueva (por ejemplo: "Monitores Power Group")

---

## 📝 PASO 1: Crear el HTML de la Sección

### 1.1 Ubicación en el código
Busca en tu HTML donde terminan las secciones existentes. Verás algo así:

```html
</section>
<section class="espacio-final"></section>

<!-- MODAL -->
<div id="imgModal" class="modal">
```

**Inserta tu nueva sección ANTES de `<section class="espacio-final">`**

---

### 1.2 Estructura completa a copiar

```html
<!-- === SECCIÓN DE MONITORES === -->
<section id="monitores">
  <h1>Monitores Power Group</h1>

  <div class="monitores-grid">
    <!-- Aquí irán las tarjetas de productos -->
  </div>
</section>
```

| Elemento                         | Qué hace                   | Importante                            |
| -------------------------------- | -------------------------- | ------------------------------------- |
| `<section id="monitores">`       | Contenedor principal       | El `id` debe ser único y sin espacios |
| `<h1>Monitores Power Group</h1>` | Título de la sección       | Aparece centrado y grande             |
| `<div class="monitores-grid">`   | Contenedor de las tarjetas | La clase debe terminar en `-grid`     |

---

## 🎨 PASO 2: Crear los Estilos CSS

### 2.1 Ubicación en el código

Busca en la sección `<style>` donde dice:

```css
.productos-info {
  /* estilos... */
}

/* === AJUSTE FINAL... */
```

**Inserta tus estilos ANTES de `/* === AJUSTE FINAL... */`**

---

### 2.2 Estilos a copiar y personalizar

```css
/* === MONITORES POWER GROUP === */
.monitores-card {
  position: relative;
  max-width: 320px;
  margin: 0 auto;
  background-color: #151515;
  border-radius: 15px;
  transition: all 0.3s ease;
  cursor: pointer;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  padding: 15px;
  overflow: hidden;
}

.monitores-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 0 25px rgba(0, 196, 255, 1);
}

.monitores-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 30px;
  justify-content: center;
  align-items: start;
  padding: 0 5vw 60px 5vw;
}

.monitores-grid.uno {
  justify-items: center;
}

.monitores-info {
  font-size: 0.75rem;
  line-height: 1.45;
  color: #ccc;
  margin-top: 12px;
}

.monitores-info strong {
  color: white;
  font-size: 1rem;
  font-weight: 600;
  text-align: left;
  display: inline;
  margin: 0;
  padding: 0;
}

.monitores-card .carousel-dots {
  margin-bottom: 12px;
}
```

**🔧 Personalización:**

* Cambia `monitores` por el nombre de tu sección
* Ajusta `max-width` para el tamaño de las tarjetas
* Cambia el color del efecto hover según tu estilo

---

## ⚙️ PASO 4: Actualizar el JavaScript

### 4.1 Actualizar el selector de tarjetas

```javascript
const cards = document.querySelectorAll('.chasis-card, .escritorio-card, .enfriamiento-card, .productos-card, .monitores-card');
```

---

### 4.2 Actualizar la función de centrado

```javascript
const visiblesMonitores = Array.from(document.querySelectorAll('.monitores-card')).filter(c => c.style.display !== 'none');
const monitoresGrid = document.querySelector('.monitores-grid');
if (monitoresGrid) monitoresGrid.classList.toggle('uno', visiblesMonitores.length === 1);
```

---

### 4.3 Agregar palabras clave al buscador (Opcional)

```javascript
const keywords = {
  chasis: ['chasis', 'torre', 'case', 'gabinete'],
  escritorios: ['escritorio', 'mesa', 'desk', 'setup'],
  enfriamiento: ['enfriamiento', 'cooler', 'ventilador', 'fan'],
  productos: ['producto', 'accesorio', 'complemento'],
  monitores: ['monitor', 'pantalla', 'display', 'screen']
};
```

---

# PARTE 2: AGREGAR UN PRODUCTO

## 🎯 Objetivo

Agregar un producto nuevo a cualquier sección existente.

---

## 📝 PASO 1: Preparar las Imágenes

Sube tus imágenes a Cloudinary o tu hosting, y copia las URLs.

**Ejemplo:**

```
https://res.cloudinary.com/dbicntfy4/image/upload/v1761252257/producto1.png
https://res.cloudinary.com/dbicntfy4/image/upload/v1761252258/producto2.png
```

---

## 📝 PASO 2: Elegir la Plantilla Correcta

### 🖼️ Ejemplo con 2 imágenes

```html
<!-- Monitor Gaming MX-27 -->
<div class="monitores-card" data-name="Monitor MX 27 Gaming 144Hz">

  <div class="carousel-container">
    <div class="carousel-images">
      <img src="https://res.cloudinary.com/dbicntfy4/image/upload/v1761252257/monitor-mx27-frente.png" alt="Monitor Power Group MX-27 - Vista frontal">
      <img src="https://res.cloudinary.com/dbicntfy4/image/upload/v1761252258/monitor-mx27-lateral.png" alt="Monitor Power Group MX-27 - Vista lateral">
    </div>

    <button class="carousel-btn prev-btn">&#10094;</button>
    <button class="carousel-btn next-btn">&#10095;</button>
  </div>

  <div class="carousel-dots">
    <span class="dot active"></span>
    <span class="dot"></span>
  </div>

  <div class="monitores-info">
    <strong>Monitor Power Group MX-27 Gaming</strong><br>
    • Resolución Full HD 1920x1080<br>
    • Tasa de refresco 144Hz<br>
    • Panel IPS con tecnología FreeSync<br>
    • Tiempo de respuesta 1ms<br>
    • Puertos: HDMI 2.0, DisplayPort 1.4<br>
    • Medidas: 61 x 46 x 21 cm
  </div>
</div>
```

---

## ✅ CHECKLIST FINAL

### Para Nueva Sección:

* [ ] HTML de la sección creado
* [ ] CSS agregado
* [ ] JavaScript actualizado
* [ ] (Opcional) Palabras clave agregadas

### Para Nuevo Producto:

* [ ] Imágenes subidas y URLs correctas
* [ ] Plantilla elegida (1, 2 o 3 imágenes)
* [ ] `data-name` con palabras clave
* [ ] Dots coinciden con cantidad de imágenes
* [ ] Textos `alt` bien escritos
* [ ] Cinta "NUEVO" si aplica

---

## 🚨 Errores Comunes

**Imágenes no cambian:** Verifica que los dots coincidan con las imágenes.  
**Buscador no funciona:** Asegúrate de agregar las palabras clave correctas.  
**Estilos no aplican:** Comprueba que las clases coincidan entre HTML y CSS.  
**Imagen rota:** Revisa que la URL sea correcta y comience con `https://`.

---

## 🎓 Ejemplo Final

```html
<!-- === SECCIÓN DE TECLADOS === -->
<section id="teclados">
  <h1>Teclados Power Group</h1>
  <div class="teclados-grid">
    <div class="teclados-card" data-name="Teclado Mecanico KB 100 RGB Gaming">
      <div class="ribbon-diagonal">NUEVO</div>
      <div class="carousel-container">
        <div class="carousel-images">
          <img src="https://ejemplo.com/teclado-kb100-frente.png" alt="Teclado KB-100 - Vista frontal">
          <img src="https://ejemplo.com/teclado-kb100-lateral.png" alt="Teclado KB-100 - Vista lateral">
          <img src="https://ejemplo.com/teclado-kb100-rgb.png" alt="Teclado KB-100 - Iluminación RGB">
        </div>
        <button class="carousel-btn prev-btn">&#10094;</button>
        <button class="carousel-btn next-btn">&#10095;</button>
      </div>
      <div class="carousel-dots">
        <span class="dot active"></span>
        <span class="dot"></span>
        <span class="dot"></span>
      </div>
      <div class="teclados-info">
        <strong>Teclado Mecánico Power Group KB-100</strong><br>
        • Switches mecánicos Blue (táctiles y clicky)<br>
        • Iluminación RGB por tecla personalizable<br>
        • Teclas anti-ghosting completas<br>
        • Cable trenzado USB removible<br>
        • Medidas: 44 x 13 x 3.5 cm
      </div>
    </div>
  </div>
</section>
```

---------------------------------------------------------------------------------------------------------------------------------------------

# ⚙️ CONFIGURACIÓN DEL SCRIPT PRINCIPAL

Este script controla las **funciones interactivas** del sitio Power Group, incluyendo buscador, modales, carruseles y ajustes automáticos de diseño.

---

## 📑 ÍNDICE
1. [Estructura General del Script](#estructura-general)
2. [Buscador Mejorado](#buscador-mejorado)
3. [Ajuste Automático del Centrado](#ajuste-de-centrado)
4. [Modal Centrado (Imágenes Ampliadas)](#modal-centrado)
5. [Carrusel de Imágenes](#carrusel-de-imágenes)
6. [Ajuste Automático del Iframe (para GitHub Pages)](#ajuste-iframe)
7. [Resumen General](#resumen-general)

---

# 🧩 ESTRUCTURA GENERAL

```javascript
window.addEventListener('load', function() {
  // Todo el código principal se ejecuta cuando la página termina de cargar
});
```

**Explicación:**
- Usa `window.addEventListener('load')` para **esperar a que el sitio cargue completamente** antes de ejecutar los scripts.
- Esto evita errores al intentar acceder a elementos del DOM que aún no existen.

---

# 🔍 BUSCADOR MEJORADO

Este bloque permite que el buscador **filtre productos por nombre o por categoría**.

```javascript
const cards = document.querySelectorAll('.chasis-card, .escritorio-card, .enfriamiento-card, .productos-card');
const searchInput = document.getElementById('searchInput');

searchInput.addEventListener('input', function() {
  const filter = searchInput.value.toLowerCase();
  const sections = document.querySelectorAll('section');
  ...
});
```

**Qué hace:**
- Captura lo que el usuario escribe en el buscador.
- Revisa cada **sección** (chasis, escritorios, enfriamiento, productos...).
- Muestra solo las tarjetas (`card`) que coinciden con la búsqueda.

**Ejemplo de uso:**
- Si escribes “torre”, el buscador mostrará únicamente los productos dentro de la sección **Chasis** que tengan esa palabra clave.

**Diccionario de búsqueda:**
```javascript
const keywords = {
  chasis: ['chasis', 'torre', 'case', 'gabinete'],
  escritorios: ['escritorio', 'mesa', 'desk', 'setup'],
  enfriamiento: ['enfriamiento', 'cooler', 'ventilador', 'fan'],
  productos: ['producto', 'accesorio', 'complemento']
};
```
Sirve para asociar **palabras relacionadas** con cada categoría y mejorar la detección.

---

# 🧭 AJUSTE DE CENTRADO

Controla el **centrado automático de las tarjetas** cuando solo hay un producto visible en una sección (por ejemplo, después de una búsqueda).

```javascript
function ajustarCentrado() {
  const visiblesChasis = Array.from(document.querySelectorAll('.chasis-card')).filter(c => c.style.display !== 'none');
  const chasisGrid = document.getElementById('chasisGrid');
  if (chasisGrid) chasisGrid.classList.toggle('uno', visiblesChasis.length === 1);
  ...
}
```

**Qué hace:**
- Detecta cuántas tarjetas hay visibles en cada sección.
- Si solo hay una, aplica una clase `.uno` para **centrarla visualmente** en el medio del contenedor.

---

# 🖼️ MODAL CENTRADO (IMÁGENES AMPLIADAS)

Permite que al hacer clic sobre una imagen de producto, **se abra ampliada** en el centro de la pantalla, adaptándose al tamaño del grupo o fila.

```javascript
function openCenteredOnRow(clickedCard, imgSrc) {
  modal.style.display = 'flex';
  modalImg.src = imgSrc;
  ...
}
```

**Explicación:**
- Calcula la posición exacta del producto (`clickedCard`).
- Identifica todas las tarjetas en la misma fila.
- Muestra la imagen centrada **de acuerdo a la fila donde estaba** (efecto natural y profesional).
- Si el usuario está filtrando por buscador (pocos productos visibles), el zoom es mayor.

**Cierre del modal:**
```javascript
closeModal.onclick = closeCurrentModal;
window.addEventListener('click', e => { if (e.target === modal) closeCurrentModal(); });
window.addEventListener('keydown', e => { if (e.key === 'Escape') closeCurrentModal(); });
```
- Se puede cerrar con clic fuera de la imagen o presionando **ESC**.

---

# 🎠 CARRUSEL DE IMÁGENES

Permite desplazarse entre las imágenes de cada producto (botones o puntos).

```javascript
cards.forEach(card => {
  const carousel = card.querySelector('.carousel-images');
  const images = card.querySelectorAll('.carousel-images img');
  const dots = card.querySelectorAll('.carousel-dots .dot');
  const prevBtn = card.querySelector('.prev-btn');
  const nextBtn = card.querySelector('.next-btn');
  let index = 0;
  ...
});
```

**Qué hace:**
- Controla el **slide** de imágenes con botones (`prev`, `next`) o puntos (`dots`).
- La variable `index` mantiene el número de imagen actual.
- Usa transformaciones CSS (`translateX`) para mover la galería.

**Ejemplo:**
```html
<button class="carousel-btn prev-btn">&#10094;</button>
<button class="carousel-btn next-btn">&#10095;</button>
```
Permiten cambiar de imagen hacia atrás o adelante.

---

# 🌐 AJUSTE IFRAME (PARA GITHUB PAGES O EMBED)

Este bloque final permite que la página **se adapte automáticamente de altura** cuando está embebida en un iframe (por ejemplo, al mostrarse dentro de otro sitio o entorno de pruebas).

```javascript
window.addEventListener("load", function() {
  function sendHeight() {
    const height = document.body.scrollHeight;
    parent.postMessage({ type: "resize-iframe", height: height }, "*");
  }
  sendHeight();
  new ResizeObserver(sendHeight).observe(document.body);
});
```

**Qué hace:**
- Calcula la altura total de la página (`scrollHeight`).
- Envía ese valor al contenedor padre para **ajustar dinámicamente el tamaño del iframe** y evitar cortes o barras innecesarias.

---

# ✅ RESUMEN GENERAL

| Función | Descripción | Elementos Relacionados |
| -------- | ------------ | ---------------------- |
| **Buscador mejorado** | Filtra productos por nombre o categoría | `#searchInput`, `.card`, `section` |
| **Centrado automático** | Ajusta visualmente la posición de una sola tarjeta | `.uno`, `.grid` |
| **Modal centrado** | Amplía imágenes de producto | `#imgModal`, `.modalImage` |
| **Carrusel** | Cambia entre imágenes de cada producto | `.carousel-images`, `.dot`, `.btn` |
| **Ajuste de iframe** | Recalcula altura para contenedor externo | `ResizeObserver`, `postMessage()` |

---


# 🧠 NOTA FINAL

Este script fue **desarrollado por JSFRAY** para el sitio **Power Group**,  
marca gamer de **Compuoriente Import And Expor Ltda**,  
garantizando un funcionamiento fluido, adaptativo y optimizado en cada módulo del sitio.

# 🧩 Fin de la Guía

Esta guía te permite **crear nuevas secciones o agregar productos** dentro de tu sitio Power Group de manera ordenada y funcional.
