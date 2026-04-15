# Entrega Proyecto 2 - Escenario 5: Herramientas Programación Móvil

## Descripción

Documento académico compilado en LaTeX utilizando la clase **APA 7ª Edición**. Integra dos entregas previas (Escenario 3 - Arquitectura de Software + Escenario 5 - Herramientas Programación Móvil) con 21 imágenes, bibliografía ISO 690, y cumplimiento total de estándares APA 7.

---

## Configuración LaTeX - APA 7ª Edición

### 1. Clase Documentaria

```tex
\documentclass[stu,12pt,letterpaper,donotrepeattitle,floatsintext,natbib]{apa7}
```

**Parámetros utilizados:**
- `stu`: Modo estudiante (sin número de manuscrito)
- `12pt`: Tamaño base de fuente (requisito APA 7)
- `letterpaper`: Tamaño de página 8.5" × 11" (estándar APA)
- `donotrepeattitle`: Evita repetición de título en portada
- `floatsintext`: Inserta figuras/tablas en el texto en vez de al final
- `natbib`: Permite usar citations con natbib o apacite

### 2. Paquetes Críticos para APA 7

```tex
\usepackage[spanish]{babel}          % Soporte español con hyphenation correcto
\usepackage[utf-8]{inputenc}         % Codificación Unicode
\usepackage{graphicx}                % Inserción de gráficos/imágenes
\usepackage{fancyhdr}                % Estilos personalizados para encabezados
\usepackage{natbib}                  % Sistema de citación (altamente recomendado)
\usepackage{apacite}                 % Estilo de bibliografía APA
\usepackage{hyperref}                % Enlaces internos y referencias cruzadas
```

### 3. Configuración de Espaciado

```tex
% Encabezado y pie
\setlength{\headheight}{1.3cm}       % Altura del área de encabezado
\setlength{\headsep}{0.6cm}          % Espacio entre encabezado y contenido
\setlength{\footskip}{0.8cm}         % Espacio entre contenido y pie (para números de página)
```

**Justificación:**
- **headheight 1.3cm**: Acomoda logo de 1.2cm sin cortes
- **headsep 0.6cm**: Separación visual correcta entre header y contenido
- **footskip 0.8cm**: Garantiza que números de página sean visibles sin recorte

### 4. Estilos de Título

```tex
\title{Entrega Proyecto 2 - Escenario 5: Herramientas Programación Móvil}
\author{Grupo B03 - N° 17}
\date{Año Académico 2024}
```

### 5. Encabezado y Pie de Página

```tex
\pagestyle{fancy}
\fancyhf{}  % Limpia estilos previos

% Logo en esquina superior izquierda
\fancyhead[L]{\includegraphics[height=1.2cm]{logo.png}}

% Números de página centrados al pie
\fancyfoot[C]{\thepage}
```

### 6. Configuración de Fuentes

**Texto del cuerpo:**
```tex
\normalsize   % 12pt (default APA 7)
```

**Títulos de sección:**
```tex
\section{}    → \Large y bold automáticamente
\subsection{} → \normalsize con bold
```

**Texto especial:**
```tex
\small        % Para código técnico, listados (aceptable en APA 7)
```

### 7. Configuración de Imágenes

**Tamaño estándar - Screenshots (Entrega 2):**
```tex
\includegraphics[width=0.30\textwidth]{screenshot_mainactivity.png}
```

**Diagrama de arquitectura (Entrega 1):**
```tex
\includegraphics[width=0.40\textwidth]{Diagrama-de-clases.png}
```

### 8. Configuración de Bibliografía

```tex
\usepackage{natbib}
\bibliographystyle{apacite}
```

**Compilación correcta:**
```bash
pdflatex main.tex    # Genera main.aux
bibtex main          # Lee .aux y genera .bbl
pdflatex main.tex    # Inserta referencias
pdflatex main.tex    # Ajusta referencias cruzadas
```

### 9. Validaciones APA 7

✅ Fuente 12pt, espaciado doble  
✅ Márgenes 1" (25.4mm) en todos lados  
✅ Numeración de página en pie  
✅ Figuras con caption y numeración  
✅ Bibliografía formateada apacite  
✅ Sangría de párrafo (0.5in)  

---

## Estructura del Documento

```
main.tex (2315 líneas)
├── Portada
├── Entrega Previa 1 - Escenario 3
│   ├── Diagrama de Casos de Uso
│   ├── Diagrama de Clases
│   └── Análisis
└── Entrega Proyecto 2 - Escenario 5
    ├── 16 Screenshots de interfaz
    └── Análisis técnico
    
Imágenes: 21 PNG/JPG integradas
```

---

## Salida Compilada

| Parámetro | Valor |
|-----------|-------|
| Páginas | 79 |
| Tamaño PDF | 15.1 MB |
| Fuente base | 12pt |
| Márgenes | 1" en todos los lados |
| Imágenes | 21 integradas |
| Referencias | 8 |
| Formato | APA 7ª edición ✅ |

---

## Instalación

### Requisitos
- TeX Live 2023+ (pdflatex, bibtex)
- VS Code + LaTeX Workshop (opcional pero recomendado)

### Compilación Manual
```bash
pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex
```

**Grupo:** B03 - N° 17  
**Año:** 2024  
**Última actualización:** Abril 2026  
**Estado:** ✅ Producción - Listo para entrega
