# Bosch Tool Finder — CAMEcuador PWA

## Descripción
Aplicativo PWA (Progressive Web App) de clase mundial para selección inteligente de herramientas eléctricas Bosch. Permite a los clientes encontrar la herramienta perfecta en menos de 2 minutos mediante 8 preguntas guiadas.

## Características
- ✅ **PWA completa**: Instalable en móvil/desktop, funciona offline
- ✅ **317 herramientas Bosch** del catálogo oficial CAMEcuador
- ✅ **Motor de matching inteligente**: Puntuación multivariable por uso, material, alimentación, voltaje, frecuencia, espacio y presupuesto
- ✅ **Diseño Bosch**: Paleta oficial azul #005CA9, tipografía Roboto Condensed
- ✅ **Responsive**: Optimizado para móvil y desktop
- ✅ **Accesibilidad**: WCAG AA, navegación por teclado, motion-reduce

## Estructura de archivos
```
bosch-finder/
├── index.html       # App completa (HTML + CSS + JS inline)
├── manifest.json    # Configuración PWA
├── sw.js            # Service Worker (offline)
├── icon-192.png     # Ícono PWA
├── icon-512.png     # Ícono PWA
└── README.md
```

## Deploy en GitHub Pages
1. Crear repositorio en GitHub (ej: `came-bosch-finder`)
2. Subir todos los archivos a la rama `main`
3. Ir a **Settings → Pages → Source: main / root**
4. La app estará disponible en: `https://[usuario].github.io/came-bosch-finder/`

## Preguntas del Quiz (8 preguntas)
1. Actividad principal (carpintería, construcción, metal, instalación, mixto)
2. Tarea específica (perforar, cortar, atornillar, lijar, demoler, otro)
3. Material de trabajo (madera, concreto, acero, cerámica, mixto)
4. Fuente de alimentación (batería, cable, indiferente)
5. Voltaje/Potencia (12V, 18V, alta potencia, indiferente)
6. Frecuencia de uso (ocasional, regular, profesional)
7. Entorno de trabajo (taller, obra, altura, espacios reducidos)
8. Rango de inversión (básico, intermedio, premium, sin restricción)

## Motor de Matching
Cada producto recibe puntos según:
- Coincidencia de uso y material (0-3 pts por criterio)
- Alimentación correcta (+3 pts)
- Voltaje/potencia adecuada (+2 pts)
- Frecuencia de uso (+2 pts)
- Entorno de trabajo (+2 pts)
- Rango de presupuesto (+2 pts)

Los resultados se desduplickan por modelo y muestran el Top 5.
