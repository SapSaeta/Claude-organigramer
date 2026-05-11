# Claude Organigramer

```
Claude Organigramer no evalua ideas con una plantilla fija.
Construye un organigrama critico temporal para cada idea.
Cada agente existe solo si cubre una funcion critica para decidir si la idea merece avanzar.
```

---

## El problema con las evaluaciones de ideas convencionales

```
IDEA
  |
  v
+---------------------------+
|  PLANTILLA GENERICA       |
|  - Mercado                |
|  - Competencia            |
|  - Finanzas               |  <-- Igual para un SaaS que para un bar.
|  - Operaciones            |      Igual para una app medica que para
|  - Legal                  |      una newsletter. Superficial siempre.
+---------------------------+
  |
  v
ANALISIS IDENTICO PARA CUALQUIER IDEA
```

Claude Organigramer hace lo contrario. Construye el comite desde cero para cada idea concreta.

---

## Como funciona

```
                   IDEA DEL USUARIO
                         |
                         v
          +--------------+--------------+
          |   INFERENCIA DE LA          |
          |   ORGANIZACION NECESARIA    |
          |   - Tipo de negocio         |
          |   - Modelo operativo        |
          |   - Cliente objetivo        |
          |   - Complejidad tecnica     |
          |   - Complejidad legal       |
          |   - Dependencias criticas   |
          +--------------+--------------+
                         |
                         v
          +--------------+--------------+
          |   IDENTIFICACION DE         |
          |   FUNCIONES CRITICAS        |
          |   Solo las que pueden       |
          |   matar o salvar la idea    |
          +--------------+--------------+
                         |
                         v
          +--------------+--------------+
          |   DISENO DEL COMITE         |
          |   DINAMICO                  |
          |   Un agente por funcion     |
          |   critica. Sin redundancia. |
          |   Sin agentes decorativos.  |
          +--------------+--------------+
                         |
              +----------+----------+
              |                     |
              v                     v
   +----------+------+   +----------+------+
   |  AGENTES        |   |  ABOGADO DEL    |
   |  ESPECIALISTAS  |   |  DIABLO         |
   |                 |   |                 |
   | - Senales +     |   | Unica funcion:  |
   | - Senales -     |   | encontrar por   |
   | - Complejidad   |   | que va a        |
   |   oculta        |   | fracasar.       |
   | - Propuestas    |   |                 |
   |   de mejora     |   |                 |
   | - Pregunta      |   |                 |
   |   critica       |   |                 |
   +----------+------+   +----------+------+
              |                     |
              +----------+----------+
                         |
                         v
          +--------------+--------------+
          |   MATRIZ DE PUNTUACION      |
          |   11 dimensiones / 0-10     |
          +--------------+--------------+
                         |
                         v
          +--------------+--------------+
          |   EVALUADOR FINAL           |
          |                             |
          |   DESCARTAR                 |
          |   APARCAR                   |
          |   VALIDAR        <-- usual  |
          |   CONSTRUIR                 |
          +--------------+--------------+
                         |
                         v
          +--------------+--------------+
          |   PRUEBA MINIMA             |
          |   DE VALIDACION             |
          |   Ejecutable en < 7 dias    |
          +--------------+--------------+
```

---

## Por que es dinamico

El sistema parte de una premisa: dos ideas del mismo sector pueden requerir comites completamente distintos.

```
MISMO SECTOR: HOSTELERIA
       |
       +--------------------------------+
       |                                |
       v                                v
  CAFE DE ESPECIALIDAD           BAR DE COPAS NOCTURNO
  en zona residencial
       |                                |
       v                                v
  FUNCIONES CRITICAS:           FUNCIONES CRITICAS:
  - Ubicacion/trafico peatonal  - Licencia nocturna
  - Recurrencia del cliente     - Insonorizacion
  - Diferenciacion de producto  - Seguridad en local
  - Margen unitario             - Margen en alcohol
  - Proveedores de grano        - Personal nocturno
  - Operaciones ligeras         - Afluencia fines de semana
       |                                |
       v                                v
  AGENTES DIFERENTES            AGENTES COMPLETAMENTE
  PARA ESTAS FUNCIONES          DISTINTOS PARA ESTAS
                                FUNCIONES
```

La Skill no tiene listas cerradas. Tiene un metodo para inferir que agentes son necesarios para cada idea especifica.

---

## Lo que aporta cada agente

```
+--------------------------------------------------+
|  AGENTE ESPECIALISTA                             |
+--------------------------------------------------+
|                                                  |
|  Senales positivas     Lo que juega a favor      |
|  Senales negativas     Lo que juega en contra    |
|  Complejidad oculta    Lo que no has visto aun   |
|  Pregunta critica      Lo que debes responder    |
|  Propuestas de mejora  Lo que puedes hacer       |
|  Recomendacion         Su posicion sobre la idea |
|                                                  |
+--------------------------------------------------+
```

Los agentes no son decorativos. Cada uno cubre una funcion critica distinta y aporta propuestas concretas para mejorar el plan en su area de responsabilidad.

---

## Los cuatro veredictos posibles

```
+------------+-----------------------------------------------+
| VEREDICTO  | CUANDO SE EMITE                               |
+------------+-----------------------------------------------+
| DESCARTAR  | Demanda debil, rentabilidad dudosa, legal      |
|            | bloqueante, o ejecucion sin retorno suficiente |
+------------+-----------------------------------------------+
| APARCAR    | Idea interesante pero prematura, no            |
|            | prioritaria o sin encaje con recursos actuales |
+------------+-----------------------------------------------+
| VALIDAR    | Default para ideas prometedoras sin evidencia  |
|            | de demanda. Hay que probar antes de construir. |
+------------+-----------------------------------------------+
| CONSTRUIR  | Solo si existe evidencia previa de demanda     |
|            | real. Prohibido sin datos de pago confirmados. |
+------------+-----------------------------------------------+
```

---

## Ejemplo: dark kitchen de bowls saludables en Madrid

**Idea presentada:**
> Quiero montar una dark kitchen especializada en bowls saludables para delivery. Solo en Madrid. Sin local a pie de calle.

**Funciones criticas inferidas:**
```
- Margen real despues de comisiones de plataforma
- Posicionamiento en apps de delivery (40-80 competidores directos)
- Velocidad de produccion y control de calidad
- Diferenciacion en mercado saturado
- Licencia de actividad de cocina
- Dependencia del repartidor externo
```

**Comite generado:**
```
+-------------------------------------------+
|  COMITE DARK KITCHEN BOWLS MADRID         |
+-------------------------------------------+
|                                           |
|  1. Analista de economicas de delivery    |
|     Comisiones Glovo / Uber / Just Eat    |
|                                           |
|  2. Especialista en posicionamiento       |
|     en apps de delivery                   |
|                                           |
|  3. Responsable de produccion             |
|     y control de tiempos                  |
|                                           |
|  4. Analista de diferenciacion            |
|     de marca sin local fisico             |
|                                           |
|  5. Especialista en margenes              |
|     por canal de venta                    |
|                                           |
|  6. Consultor de licencias                |
|     de actividad de cocina                |
|                                           |
|  7. Abogado del Diablo                    |
|                                           |
|  8. Evaluador Final                       |
|                                           |
+-------------------------------------------+
```

**Ejemplo de propuestas de mejora del Analista de economicas de delivery:**
```
1. Calcular el unit economics con las comisiones reales antes de abrir
   (30-35% en Glovo, similar en Uber Eats).

2. Negociar con una sola plataforma los primeros 90 dias para reducir
   la dependencia multiple y conseguir mejores condiciones iniciales.

3. Disenar el menu con ticket medio minimo de 14-16 euros para que
   el margen neto sea positivo despues de comisiones y produccion.

4. Incluir en el calculo el coste de los embalajes sostenibles si
   el posicionamiento es saludable/eco, que suele subestimarse.
```

**Veredicto:**
```
+--------------------------------------------------+
|  VEREDICTO: VALIDAR                             |
+--------------------------------------------------+
|                                                  |
|  Las comisiones de plataforma comprimen el       |
|  margen hasta hacerlo marginal o negativo en     |
|  tickets bajos. El mercado de bowls en Madrid    |
|  esta saturado. Antes de invertir en licencia    |
|  y equipamiento, hay que confirmar el margen     |
|  unitario real y que existe diferenciacion       |
|  percibida por el cliente.                       |
|                                                  |
|  Prueba: unit economics test + outreach a        |
|  20 clientes potenciales. Coste: ~100 euros.     |
|  Plazo: 5 dias.                                  |
|                                                  |
+--------------------------------------------------+
```

---

## La matriz de puntuacion

```
+-----------------------------+-------+-----------------------------+
| DIMENSION                   | 0-10  | QUE MIDE                    |
+-----------------------------+-------+-----------------------------+
| Demanda real                |       | Evidencia de pago           |
| Facilidad de validacion     |       | Prueba en menos de 7 dias   |
| Facilidad de venta          |       | Ciclo y friccion de compra  |
| Viabilidad tecnica          |       | Con recursos disponibles    |
| Velocidad de construccion   |       | Tiempo hasta MVP funcional  |
| Potencial de rentabilidad   |       | Margen neto sostenible      |
| Seguridad legal             |       | Obstaculos regulatorios     |
| Simplicidad operativa       |       | Carga diaria de gestion     |
| Ventaja competitiva         |       | Dificultad de replicacion   |
| Encaje con recursos         |       | Capital, tiempo, skills     |
| Potencial de automatizacion |       | Escala sin crecimiento      |
|                             |       | lineal de costes            |
+-----------------------------+-------+-----------------------------+
| TOTAL                       |  /110 |                             |
+-----------------------------+-------+-----------------------------+
```

La puntuacion no determina el veredicto. Una idea con 90/110 pero con 0 en demanda real no puede recibir veredicto CONSTRUIR.

---

## Estructura del repositorio

```
Claude-organigramer/
|
+-- README.md
|
+-- .claude/
    |
    +-- skills/
        |
        +-- idea-critical-organigramer/
            |
            +-- SKILL.md                       La Skill operativa
            |                                  Frontmatter YAML + flujo completo
            |
            +-- resources/
                |
                +-- dynamic-committee-method.md  Como disenar el comite
                |                                Ejemplos comparativos
                |                                Criterios de seleccion
                |
                +-- evaluation-matrix.md         11 dimensiones 0-10
                |                                Que significa cada puntuacion
                |
                +-- validation-tests.md          12 tipos de prueba
                                                 Coste, tiempo, metricas
```

---

## Como activar la Skill

```
/idea-critical-organigramer

[descripcion de la idea]
```

La Skill responde en espanol por defecto. Si la descripcion es ambigua, hace preguntas especificas antes de evaluar. Si la descripcion es suficiente, emite el analisis completo directamente.

---

## Limitaciones

```
+--------------------------------------------------+
|  La Skill simula perspectivas especializadas.   |
|  No hay expertos reales detras del comite.      |
+--------------------------------------------------+

+--------------------------------------------------+
|  La calidad del analisis depende de la          |
|  calidad de la informacion proporcionada.       |
|  Idea vaga = nivel de confianza bajo.           |
+--------------------------------------------------+

+--------------------------------------------------+
|  No tiene acceso a datos de mercado en          |
|  tiempo real. Trabaja con conocimiento          |
|  del modelo e informacion del usuario.          |
+--------------------------------------------------+

+--------------------------------------------------+
|  El veredicto no es una garantia. Es una        |
|  evaluacion critica con la informacion          |
|  disponible en el momento del analisis.         |
+--------------------------------------------------+
```

---

## Proxima evolucion posible

- Evaluacion comparativa de dos ideas en el mismo analisis
- Modo de seguimiento: reevaluar una idea tras completar la prueba de validacion
- Especializacion por sector con capas adicionales de conocimiento regulatorio
- Generacion de un plan de validacion con tareas ordenadas y asignadas
- Integracion con fuentes de datos externas para metricas de mercado
