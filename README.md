# 🖥️ Arquitecturas de Procesadores 2026

[![GitHub Pages](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-2ea44f?style=for-the-badge&logo=github)](https://c7dev-77.github.io/Recurso_Academico/)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/es/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/Vanilla%20CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/es/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript%20ES6+-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/es/docs/Web/JavaScript)
[![Three.js](https://img.shields.io/badge/Three.js-r128-000000?style=for-the-badge&logo=three.js&logoColor=white)](https://threejs.org/)
[![RISC-V](https://img.shields.io/badge/RISC--V-RV32%20Subset-D9230F?style=for-the-badge&logo=riscv&logoColor=white)](https://riscv.org/)

> **Portal interactivo educativo y simulador RISC paso a paso**, diseñado para la enseñanza visual, intuitiva y rigurosa de las arquitecturas de procesadores modernas: desde los fundamentos de diseño **CISC vs RISC** y **ARM vs x86**, hasta la computación multinúcleo, segmentación (pipeline), y aceleradores especializados en silicio para Inteligencia Artificial en 2026.

---

## 🌐 Demo en Vivo

Puedes acceder a la versión interactiva completa sin necesidad de instalación previa a través de **GitHub Pages**:

👉 **[https://c7dev-77.github.io/Recurso_Academico/](https://c7dev-77.github.io/Recurso_Academico/)**

---

## 👥 Autores · Grupo 6

Proyecto desarrollado para la cátedra de **Arquitectura de Computadores (2026)**:

| Integrante | Rol / Enfoque |
| :--- | :--- |
| **Juan David Arrieta Flórez** | Investigación de arquitecturas modernas y documentación técnica |
| **Brandon Andrés García Baldovino** | Diseño conceptual, visualización y análisis comparativo CISC/RISC |
| **Cristian de Jesús Morales Berrío** | Implementación del simulador, integración Three.js y despliegue web |
| **César Miguel Yepes Hernández** | Modelado de conceptos multinúcleo, pipeline y glosario técnico |

---

## 🚀 Características Principales

### 1. 🧊 Escenas y Modelos 3D Interactivos (Three.js WebGL)
- **Comparador de Longitud de Instrucciones:** Visualiza barras 3D proporcionales al tamaño en bytes de instrucciones x86 (longitud variable) frente a ARM/RISC (4 bytes fijos) con animación de descomposición en micro-operaciones (`load`, `add`, `store`).
- **Simulador 3D de Chip Multinúcleo:** Representación espacial de núcleos homogéneos/heterogéneos y memoria caché L3 compartida, con simulación de carga y pulso de actividad.
- **Flujo de Pipeline 3D:** Animación tridimensional de instrucciones en tránsito a través de las 5 etapas clásicas, demostrando visualmente la diferencia de rendimiento entre ejecución secuencial y segmentada.
- **Empaquetado Avanzado y Chiplets 2026:** Maqueta en capas con control deslizante de **"explosión vertical"** para inspeccionar la integración de CPU, GPU/TPU, NPU, sustrato, interposer y pilas de memoria HBM apilada verticalmente.

### 2. ⚡ Simulador RISC Paso a Paso
- **Ciclo de Instrucción Completo:** Iluminación en tiempo real de las 5 etapas del pipeline (*Fetch, Decode, Execute, Memory, Write-back*) correspondientes a la instrucción activa.
- **Inspección de Estado:**
  - Banco de **32 registros** (`zero`, `ra`, `sp`, `gp`, `tp`, `t0-t6`, `s0-s11`, `a0-a7`) con detección de cambios y resaltado animado.
  - **Memoria de datos** de 16 palabras alineadas a 32 bits (0x00 a 0x3C).
  - Contador de programa (`PC`) que avanza de 4 en 4 bytes.
  - Contador de ciclos e instrucciones ejecutadas.
- **Control de Ejecución Flexible:** Modos paso a paso (*Step*), retroceso temporal (*Undo/Back*), ejecución continua (*Play/Pause*) y selector de velocidad ajustable.
- **Editor y Ensamblador Integrado:** Pestaña *«Mi programa»* para redactar código en ensamblador RISC personalizado, compilarlo sintácticamente y simularlo al instante.

### 3. 📖 Glosario Técnico Interactivo
- Más de **35 términos clave** sobre arquitectura de procesadores y silicio avanzado.
- **Búsqueda en tiempo real** para filtrar conceptos al instante.
- **Tooltips dinámicos contextuales:** Pasa el cursor sobre cualquier término punteado dentro de los textos explicativos para consultar su definición inmediata sin perder la lectura.

### 4. 📄 Documentación Técnica Incluida
- Incluye el documento PDF oficial explicativo del portal: [`Explicacion-Portal-y-Simulador-RISC.pdf`](./Explicacion-Portal-y-Simulador-RISC.pdf).

---

## 📚 Estructura Temática del Portal

```
├── 1. CISC vs RISC ──────────── Comparativa ISA, micro-operaciones, tablas y visualizador 3D
├── 2. ARM vs x86 ────────────── Licencias IP vs integración vertical, contadores y métricas 2024-2026
├── 3. Arquitecturas Multinúcleo ─ Coherencia de caché, núcleos P/E y calculadora interactiva de Ley de Amdahl
├── 4. Pipeline RISC (5 etapas) ─ Segmentación, CPI ideal, riesgos de datos y comparativa de ciclos
├── 5. Chips Especializados 2026 ─ TPU v7 Ironwood, Blackwell B200, NPU Copilot+, HBM3e y Chiplets 3D
├── 6. Simulador RISC ────────── Ejecución paso a paso, programas demo y editor libre con ensamblador
├── 7. Uso de IA en el Proyecto ─ Metodología de prompts, validación cruzada y rigor académico
└── 8. Referencias y Glosario ── Fuentes formales indexadas y buscador de terminología
```

### Tabla Resumen: CISC vs. RISC

| Característica | CISC (Complex Instruction Set Computer) | RISC (Reduced Instruction Set Computer) |
| :--- | :--- | :--- |
| **Longitud de instrucción** | Variable (ej. x86: de 1 a 15 bytes) | Fija (estándar: 4 bytes / 32 bits) |
| **Acceso a Memoria** | Permitido en múltiples tipos de instrucciones | Exclusivo mediante modelo **Load/Store** (`lw`, `sw`) |
| **Registros Disponibles** | Menor cantidad general (x86-64: 16 de uso general) | Mayor cantidad (ej. RISC-V / ARM: 32 registros) |
| **Decodificación** | Compleja; requiere microcódigo y traductores | Sencilla, simétrica y directa por hardware |
| **Filosofía de Compilador** | Código binario más denso | Mayor trabajo para el optimizador del compilador |

### Calculadora Interactiva: Ley de Amdahl
El portal incluye un calculador visual con la fórmula:

$$\text{Aceleración} = \frac{1}{(1 - p) + \frac{p}{n}}$$

Donde:
- $p$: Fracción del programa paralelizable (ajustable de 50% a 99%).
- $n$: Número de núcleos físicos (ajustable de 1 a 8).

Demuestra cuantitativamente por qué un programa con solo el 90% paralelizable tiene un límite teórico estricto de **10×**, sin importar cuántos núcleos se agreguen.

---

## 🛠️ Especificación del Simulador RISC

El simulador implementa un subconjunto práctico de la arquitectura **RV32I**:

### Conjunto de Instrucciones Soportadas

| Instrucción | Sintaxis | Etapas Activas | Descripción |
| :--- | :--- | :--- | :--- |
| `add` | `add rd, rs1, rs2` | F, D, E, WB | Suma: `rd = rs1 + rs2` |
| `sub` | `sub rd, rs1, rs2` | F, D, E, WB | Resta: `rd = rs1 - rs2` |
| `mul` | `mul rd, rs1, rs2` | F, D, E, WB | Multiplicación entera de 32 bits |
| `and` | `and rd, rs1, rs2` | F, D, E, WB | Operación lógica AND a nivel de bits |
| `or` | `or rd, rs1, rs2` | F, D, E, WB | Operación lógica OR a nivel de bits |
| `slt` | `slt rd, rs1, rs2` | F, D, E, WB | Set Less Than: `rd = 1` si `rs1 < rs2`, sino `0` |
| `addi` | `addi rd, rs1, imm` | F, D, E, WB | Suma inmediata con constante con signo |
| `li` | `li rd, imm` | F, D, E, WB | Carga constante inmediata en registro |
| `mv` | `mv rd, rs` | F, D, E, WB | Copia de valor entre registros |
| `lw` | `lw rd, desp(rs1)` | F, D, E, MEM, WB | Carga palabra de memoria: `rd = MEM[rs1 + desp]` |
| `sw` | `sw rs2, desp(rs1)` | F, D, E, MEM | Guarda palabra en memoria: `MEM[rs1 + desp] = rs2` |
| `beq` | `beq rs1, rs2, label` | F, D, E | Salto condicional si `rs1 == rs2` |
| `bne` | `bne rs1, rs2, label` | F, D, E | Salto condicional si `rs1 != rs2` |
| `blt` | `blt rs1, rs2, label` | F, D, E | Salto condicional si `rs1 < rs2` |
| `j` | `j label` | F, D, E | Salto incondicional al destino |
| `halt` | `halt` | F, D | Detiene el ciclo de ejecución |

### Programas Demostrativos Incluidos

1. **1. Suma:** Demuestra el uso de constantes con `li`, suma de registros con `add` y almacenamiento en memoria RAM mediante `sw`.
2. **2. Resta:** Demuestra aritmética con `sub` y representación de valores negativos en complemento a dos ($12 - 7 = 5$ y $7 - 12 = -5$).
3. **3. Multiplicación:** Demuestra estructuras de control mediante bucles iterativos condicionales (`addi`, `bne`) y validación contra la instrucción nativa `mul`.
4. **4. Mi programa:** Editor libre con soporte para saltos, comparaciones (`slt`), lecturas de memoria (`lw`) y gestión completa de etiquetas.

---

## 🤖 Uso Ético y Asistido de Inteligencia Artificial

Siguiendo las mejores prácticas académicas y de transparencia, la creación de este recurso involucró herramientas de IA de forma supervisada y controlada:

```
[Definición de Requisitos y Contenidos]
                    │
                    ▼
       ┌────────────────────────┐
       │   Ingeniería de Prompts │
       └───────────┬────────────┘
                   │
         ┌─────────┴─────────┐
         ▼                   ▼
    ┌─────────┐         ┌─────────┐
    │ Claude  │         │ Gemini  │
    └────┬────┘         └────┬────┘
         │                   │
         │ Código y motor 3D │ Investigación y datos
         ▼                   ▼
       ┌────────────────────────┐
       │ Validación Humana      │
       │ Grupo 6                │
       └───────────┬────────────┘
                   │ Verificación contra fuentes oficiales (AWS, Apple, AMD, IEEE)
                   ▼
     [Despliegue y Proyecto Final]
```

- **Claude:** Generación, depuración y optimización del código fuente en un solo archivo autosuficiente (Three.js WebGL, motor de ensamblado, máquina de estados del simulador y diseño responsive con temas CSS adaptativos).
- **Gemini:** Exploración de literatura técnica contemporánea (2024-2026), especificaciones de microarquitecturas de servidores (AWS Graviton4, AMD Turin) y silicio de IA (Google TPU v7 Ironwood, NVIDIA Blackwell B200).
- **Verificación Humana:** El 100% de los datos numéricos, leyes físicas, algoritmos de pipeline y referencias fueron contrastados directamente con manuales oficiales y literatura indexada por los autores.

---

## 📂 Estructura del Repositorio

```bash
Recurso_Academico/
├── index.html                                 # Archivo principal para despliegue en GitHub Pages
├── portal-arquitecturas-procesadores.html     # Portal web interactivo completo (HTML + CSS + JS)
├── Explicacion-Portal-y-Simulador-RISC.pdf    # Guía técnica académica en PDF del simulador y portal
└── README.md                                  # Documentación profesional del proyecto
```

---

## 💻 Ejecución Local

No se requieren gestores de paquetes ni compilación (cero dependencias complejas). El portal está diseñado para ser completamente autocontenido:

### Opción 1: Abrir directamente en el navegador
Haz doble clic sobre [`index.html`](./index.html) o arrástralo a cualquier navegador web moderno (Google Chrome, Mozilla Firefox, Microsoft Edge o Safari).

> *Nota: Se requiere conexión a Internet únicamente para cargar la librería Three.js (vía CDN) y las fuentes tipográficas de Google Fonts.*

### Opción 2: Servidor local ligero (Opcional)
Si deseas ejecutarlo mediante un servidor web local:

**Con Python:**
```bash
# Python 3.x
python -m http.server 8080
```
Luego abre tu navegador en `http://localhost:8080`.

**Con Node.js (npx):**
```bash
npx serve .
```

---

## 📖 Referencias Bibliográficas

- Amazon Web Services. (2023). *AWS Graviton4 processors*. [https://aws.amazon.com/ec2/graviton/](https://aws.amazon.com/ec2/graviton/)
- Apple. (2024, 7 de mayo). *Apple introduces M4 chip*. Apple Newsroom.
- Blem, E., Menon, J., & Sankaralingam, K. (2013). Power struggles: Revisiting the RISC vs. CISC debate on contemporary ARM and x86 architectures. *IEEE HPCA*, 1–12.
- Google Cloud. (2025). *Ironwood: The first Google TPU for the age of inference*. Blog de Google Cloud.
- Hennessy, J., & Patterson, D. (2019). A new golden age for computer architecture. *Communications of the ACM*, 62(2), 48–60.
- Jouppi, N. P., et al. (2023). TPU v4: An optically reconfigurable supercomputer for machine learning with hardware support for embeddings. *ISCA '23*.
- Naffziger, S., et al. (2021). Pioneering chiplet technology and design for the AMD EPYC and Ryzen processor families. *ISCA 2021*.
- NVIDIA. (2024). *NVIDIA Blackwell architecture technical brief*.
- Patterson, D., & Hennessy, J. (2020). *Computer organization and design: RISC-V edition* (2.ª ed.). Morgan Kaufmann.
- Stallings, W. (2019). *Computer organization and architecture* (11.ª ed.). Pearson.
- Waterman, A., & Asanović, K. (Eds.). (2019). *The RISC-V instruction set manual, Volume I: Unprivileged ISA*. RISC-V International.

---

<p align="center">
  <b>Grupo 6 · Arquitectura de Computadores 2026</b><br>
  Hecho con pasión por el hardware, el aprendizaje interactivo y la ingeniería de software.
</p>
