# 📋 GUÍA: Cómo Agregar tu Logo a TERRANZA

## 🎯 Ubicación del Logo

El logo se encuentra en la **barra de navegación superior** (navbar), específicamente en la esquina superior izquierda.

## 📁 Archivo del Logo

Tu logo ya está disponible en:
```
/mnt/user-data/uploads/LOGO_EN_VERSION_NEGATIVO_SIN_FONDO.png
```

## 🔧 Opciones de Implementación

He configurado **3 opciones** para que elijas la que más te guste:

### Opción 1: LOGO + TEXTO (⭐ RECOMENDADA)
```html
<div class="logo">
    <img src="/mnt/user-data/uploads/LOGO_EN_VERSION_NEGATIVO_SIN_FONDO.png" alt="TERRANZA" class="logo-image">
    <span class="logo-text">TERRANZA</span>
</div>
```
✅ **Ventajas:**
- Combina identidad visual con texto
- Más fácil de reconocer
- Mejor para SEO
- Se ve profesional

### Opción 2: SOLO LOGO
```html
<div class="logo">
    <img src="/mnt/user-data/uploads/LOGO_EN_VERSION_NEGATIVO_SIN_FONDO.png" alt="TERRANZA" class="logo-image">
</div>
```
✅ **Ventajas:**
- Minimalista
- Más limpio
- Da protagonismo al logo

### Opción 3: SOLO TEXTO
```html
<div class="logo">
    <span class="logo-text">TERRANZA</span>
</div>
```
✅ **Ventajas:**
- Ultra minimalista
- Carga más rápido
- Funciona si no tienes logo aún

## 🎨 Características del Logo en el Sitio

### Tamaños Automáticos:
- **Desktop normal:** 50px de altura
- **Desktop scroll:** 40px (se reduce al hacer scroll)
- **Tablet:** 40px
- **Mobile:** 35px
- **Mobile scroll:** 30px

### Animaciones Incluidas:
- ✨ **Hover:** Se agranda ligeramente (scale 1.05)
- ✨ **Hover:** Aparece línea dorada debajo
- ✨ **Scroll:** Reduce tamaño suavemente
- ✨ **Transiciones:** Todas suaves (0.3s)

## 📝 Cómo Cambiar de Opción

Busca esta sección en el código HTML (línea ~831 aprox.):

```html
<div class="logo">
    <!-- Opción 1: Solo logo imagen -->
    <!-- <img src="ruta/logo.png" alt="TERRANZA" class="logo-image"> -->
    
    <!-- Opción 2: Logo + Texto (ACTIVA POR DEFECTO) -->
    <img src="/mnt/user-data/uploads/LOGO_EN_VERSION_NEGATIVO_SIN_FONDO.png" alt="TERRANZA" class="logo-image">
    <span class="logo-text">TERRANZA</span>
    
    <!-- Opción 3: Solo texto -->
    <!-- <span class="logo-text">TERRANZA</span> -->
</div>
```

**Para cambiar:**
1. Comenta (agrega `<!--` y `-->`) la opción que NO quieres
2. Descomenta (quita `<!--` y `-->`) la opción que SÍ quieres

## 🖼️ Si Quieres Usar Tu Propio Logo

### Paso 1: Sube tu logo
Guarda tu archivo de logo en el servidor o en la misma carpeta del HTML

### Paso 2: Cambia la ruta
Reemplaza:
```html
src="/mnt/user-data/uploads/LOGO_EN_VERSION_NEGATIVO_SIN_FONDO.png"
```

Por:
```html
src="ruta/a/tu/logo.png"
```

### Recomendaciones para el Logo:
- ✅ Formato: PNG con fondo transparente
- ✅ Color: Blanco o claro (el fondo del navbar es oscuro)
- ✅ Tamaño: Mínimo 200px de ancho para alta calidad
- ✅ Peso: Menos de 100KB para carga rápida
- ✅ Aspecto: Horizontal funciona mejor que vertical

## 🎨 Personalizar Tamaño del Logo

Si quieres cambiar el tamaño, edita estas líneas en el CSS:

```css
.logo-image {
    height: 50px;  /* ← Cambia este número */
    width: auto;
    object-fit: contain;
}

nav.scrolled .logo-image {
    height: 40px;  /* ← Cambia este número */
}
```

## 🚀 Ejemplos de Uso

### Logo Más Grande:
```css
.logo-image {
    height: 70px;  /* Más grande */
}
```

### Logo Más Pequeño:
```css
.logo-image {
    height: 35px;  /* Más pequeño */
}
```

### Sin Animación de Reducción al Scroll:
```css
nav.scrolled .logo-image {
    height: 50px;  /* Mismo tamaño siempre */
}
```

## 📱 Responsive

El logo ya está configurado para adaptarse automáticamente:

| Dispositivo | Tamaño Normal | Al Scroll |
|-------------|---------------|-----------|
| Desktop     | 50px          | 40px      |
| Tablet      | 40px          | 35px      |
| Mobile      | 35px          | 30px      |
| Mini Mobile | 35px          | 30px      |

## ✨ Efectos Especiales Incluidos

1. **Transición suave** al hacer scroll (navbar se achica)
2. **Hover effect** - el logo crece ligeramente
3. **Línea dorada** aparece debajo al pasar el mouse
4. **Cursor personalizado** cambia al pasar sobre el logo (solo desktop)

## 🔗 Logo como Link

El logo ya funciona como link al inicio. Si quieres que vaya a otra página:

```html
<a href="https://www.tudominio.com">
    <div class="logo">
        <img src="logo.png" alt="TERRANZA" class="logo-image">
        <span class="logo-text">TERRANZA</span>
    </div>
</a>
```

## 💡 Tips Pro

1. **Formato SVG:** Si tienes tu logo en SVG, úsalo. Escala perfectamente y pesa menos
2. **Versión Oscura/Clara:** Crea 2 versiones y cámbialas con JavaScript según el scroll
3. **Favicon:** No olvides agregar tu logo como favicon en el `<head>`
4. **Alt Text:** Siempre incluye alt="TERRANZA" para SEO

## 🎯 ¿Dónde está en el Código?

**Navegación:** Líneas ~831-840
**Estilos Logo:** Líneas ~155-190
**Responsive:** Líneas ~975-990, ~1020-1035

---

¡Ya está todo configurado! Solo tienes que elegir tu opción favorita. 🎨✨
