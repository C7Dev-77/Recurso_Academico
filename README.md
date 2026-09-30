Arquitecturas de Procesadores 2026
Guia tecnica del portal interactivo y del simulador RISC paso a paso. Grupo 6: Juan David Arrieta Florez,
Brandon Andres Garcia Baldovino, Cristian de Jesus Morales Berrio y Cesar Miguel Yepes Hernandez.
1. Que contiene el portal
Seccion Contenido Elemento interactivo
CISC vs RISC Filosofias de ISA, ejemplo x86 vs RISC-V, tabla
comparativa
3D: comparador de longitud de instrucciones y
decodificacion en micro-operaciones
ARM vs x86 Licenciamiento, eficiencia, ejemplos reales
2023-2025
Contadores animados
Multinucleo Nucleos, cache L3, coherencia, nucleos P y E,
Ley de Amdahl
3D: chip multinucleo + deslizadores de nucleos y
fraccion paralela
Pipeline Cinco etapas, CPI, riesgos de datos 3D: instrucciones fluyendo con y sin pipeline
Chips 2026 GPU, TPU, NPU, chiplets, HBM, RISC-V 3D: empaquetado con capas explotables
Simulador Tres programas mas un editor propio Ejecucion paso a paso con retroceso
Glosario Mas de 35 terminos Tooltip al pasar el mouse sobre palabras
punteadas y buscador
2. Conceptos clave
CISC usa instrucciones potentes y de longitud variable (x86: de 1 a 15 bytes); una sola puede leer
memoria, operar y escribir. RISC usa instrucciones simples de 4 bytes y arquitectura load/store, lo que
facilita el pipeline. Los x86 modernos traducen cada instruccion a micro-operaciones, asi que la frontera
entre ambos es hoy borrosa (Blem et al., 2013).
Multinucleo: ante el limite termico de la frecuencia se integran varios nucleos. Segun la Ley de Amdahl,
aceleracion = 1 / ((1 - p) + p/n); con p = 90 % el maximo teorico es 10x. Chips especializados: GPU
(paralelismo masivo), TPU (ASIC para tensores), NPU (inferencia local), integrados como chiplets sobre
un interposer con memoria HBM.
3. El simulador RISC
Subconjunto inspirado en RISC-V: 32 registros, instrucciones de 4 bytes (el PC avanza de 4 en 4),
registro zero fijo en 0 y acceso a memoria solo con lw y sw. Cada paso ilumina las etapas Fetch, Decode,
Execute, Memory y Write-back que usa la instruccion, explica la operacion con los valores reales y
resalta en verde el registro o la palabra de memoria que cambio.
Instruccion Operacion Ejemplo
add, sub, mul, and, or, slt rd = rs1 op rs2 (slt: 1 si rs1 < rs2) add a0, t0, t1
addi rd = rs1 + constante addi t1, t1, -1
lw / sw Lee / escribe memoria en rs1 + desp sw a0, 0(zero)
beq, bne, blt Salto condicional a etiqueta bne t1, zero, bucle
li, mv, j, halt Constante, copia, salto, fin li t0, 12
Programas incluidos
Portal Arquitecturas de Procesadores 2026 - Grupo 6 - Guia tecnica Pagina 2
Programa Que demuestra Resultado esperado
1. Suma li, add y sw: 12 + 7 a0 = 19; memoria[0] = 19
2. Resta sub y numeros negativos (complemento a dos): 12 - 7 y 7 - 12 a0 = 5; a1 = -5
3. Multiplicacion Bucle con addi y bne que suma 6 cuatro veces; se verifica con
mul
a0 = 24; a1 = 24
4. Mi programa Editor libre para escribir y ensamblar codigo propio Depende del codigo
Uso: elegir programa, pulsar Paso (o Ejecutar con velocidad ajustable), usar Atras para deshacer y
Reiniciar para empezar de nuevo. Limitaciones: no hay codificacion binaria, pila ni subrutinas;
ampliaciones posibles: sll, div, jal y simulacion de pipeline con riesgos de datos.
4. Tecnologia y uso de IA
El portal es un unico archivo HTML con CSS y JavaScript propios; los graficos 3D usan Three.js (r128)
cargado desde cdnjs, por lo que se necesita conexion a internet para verlos. Se uso Claude para generar
y depurar el codigo (simulador, escenas 3D, glosario) y Gemini para investigar tendencias y contrastar
cifras. Todas las cifras se verificaron contra las fuentes oficiales citadas.
5. Referencias
Amazon Web Services. (2023). AWS Graviton4 processors. https://aws.amazon.com/ec2/graviton/
Apple. (2024, 7 de mayo). Apple introduces M4 chip. Apple Newsroom.
Blem, E., Menon, J., & Sankaralingam, K. (2013). Power struggles: Revisiting the RISC vs. CISC debate on contemporary
ARM and x86 architectures. IEEE HPCA, 1-12.
Google Cloud. (2025). Ironwood: The first Google TPU for the age of inference. Blog de Google Cloud.
Hennessy, J., & Patterson, D. (2019). A new golden age for computer architecture. Communications of the ACM, 62(2),
48-60.
Jouppi, N. P., et al. (2023). TPU v4: An optically reconfigurable supercomputer for machine learning with hardware support
for embeddings. ISCA 23.
Naffziger, S., et al. (2021). Pioneering chiplet technology and design for the AMD EPYC and Ryzen processor families. ISCA
2021.
NVIDIA. (2024). NVIDIA Blackwell architecture technical brief.
Patterson, D., & Hennessy, J. (2020). Computer organization and design: RISC-V edition (2.a ed.). Morgan Kaufmann.
Stallings, W. (2019). Computer organization and architecture (11.a ed.). Pearson.
Waterman, A., & Asanovic, K. (Eds.). (2019). The RISC-V instruction set manual, Volume I: Unprivileged ISA. RISC-V
International.
