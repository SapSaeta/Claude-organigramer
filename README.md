# Claude Organigramer

Claude Organigramer no evalua ideas con una plantilla fija.
Construye un organigrama critico temporal para cada idea.
Cada agente existe solo si cubre una funcion critica para decidir si la idea merece avanzar.

---

## Que es

Claude Organigramer es un repositorio de Skills para Claude Code que contiene la Skill `idea-critical-organigramer`.

Esta Skill evalua ideas de negocio, producto, automatizacion, aplicaciones, servicios, proyectos SAP/enterprise, contenido, herramientas IA, inversiones y cualquier otro proyecto mediante un comite dinamico de agentes especialistas.

No es un generador de planes de negocio. No es una herramienta de motivacion. Es un sistema de evaluacion critica cuyo objetivo es detectar si una idea merece ser descartada, aparcada, validada o construida.

---

## Que problema resuelve

La mayoria de herramientas de evaluacion de ideas funcionan con plantillas fijas. Dan la misma estructura para un SaaS que para un bar, para una app medica que para una newsletter.

El resultado es un analisis superficial que no detecta las funciones criticas especificas de cada idea, no identifica los riesgos propios de ese tipo de negocio, no ajusta el nivel de escrutinio a la complejidad real y no distingue entre lo que se necesita saber y lo que es decorativo.

Claude Organigramer resuelve esto construyendo un comite diferente para cada idea a partir de sus funciones criticas concretas.

---

## Como funciona

Cuando el usuario presenta una idea, la Skill sigue este proceso:

1. **Entiende la idea.** Si hay ambiguedad, hace preguntas especificas antes de continuar.

2. **Infiere la organizacion necesaria.** Analiza que tipo de empresa, equipo u operacion tendria que existir para ejecutar la idea de forma realista. Identifica tipo de negocio, modelo operativo, cliente objetivo, canal de venta, complejidad tecnica, legal y financiera, y dependencias criticas.

3. **Identifica las funciones criticas.** Determina que funciones especificas decidiran el exito o el fracaso de esta idea concreta. No usa listas genericas.

4. **Disenha el comite dinamico.** Crea solo los agentes necesarios para cubrir esas funciones. Justifica por que cada agente esta en el comite. Elimina agentes redundantes.

5. **Ejecuta el analisis.** Cada agente emite su informe con senales positivas, senales negativas, complejidad oculta y una pregunta critica.

6. **El Abogado del Diablo destruye la idea.** Un agente dedicado exclusivamente a encontrar por que la idea va a fracasar.

7. **La Matriz de puntuacion.** Once dimensiones puntuadas de 0 a 10 con justificacion.

8. **El Evaluador Final emite el veredicto.** DESCARTAR, APARCAR, VALIDAR o CONSTRUIR.

9. **Prueba minima de validacion.** Si el veredicto es VALIDAR o CONSTRUIR, define una prueba ejecutable en menos de 7 dias.

---

## Por que es dinamico

La dinamica del sistema parte de una premisa: dos ideas del mismo sector pueden requerir comites completamente distintos porque sus funciones criticas son distintas.

Un cafe de especialidad en zona residencial y un bar de copas nocturno son ambos hosteleria. Pero las funciones que decidiran su exito o fracaso son diferentes. El comite se construye a partir de la idea, no a partir del sector.

La Skill no tiene listas cerradas de agentes por tipo de negocio. Tiene un metodo para inferir que agentes son necesarios para cada idea concreta.

Esto permite crear agentes muy especificos cuando la idea lo requiere:
- Especialista en licencias nocturnas para un bar
- Analista de dependencia de marketplaces para una dark kitchen
- Arquitecto SAP HR para una herramienta de RRHH enterprise
- Especialista en regulacion de productos sanitarios digitales para una app medica

---

## Estructura del repositorio

```
.
├── README.md
└── .claude/
    └── skills/
        └── idea-critical-organigramer/
            ├── SKILL.md
            └── resources/
                ├── dynamic-committee-method.md
                ├── evaluation-matrix.md
                └── validation-tests.md
```

**SKILL.md:** La Skill completa. Contiene el frontmatter YAML, los principios de operacion, el flujo obligatorio y el formato de salida.

**dynamic-committee-method.md:** Guia metodologica para disenar el comite dinamico. Incluye ejemplos comparativos que ilustran como el mismo sector produce comites distintos.

**evaluation-matrix.md:** Definicion de las once dimensiones de evaluacion con lo que significa puntuar 0, 5 o 10 en cada una.

**validation-tests.md:** Doce tipos de pruebas de validacion con instrucciones de ejecucion, coste, metricas de exito y cuando abandonar.

---

## Como usar la Skill

La Skill se activa desde Claude Code. Una vez disponible en el proyecto, el usuario puede invocarla con:

```
/idea-critical-organigramer
```

Y a continuacion describir la idea que quiere evaluar.

La Skill responde en espanol por defecto. Si el usuario escribe en otro idioma, responde en ese idioma.

---

## Ejemplo de uso

El usuario escribe:

> Quiero montar una dark kitchen especializada en bowls saludables para delivery. Solo en Madrid. Sin local a pie de calle.

La Skill analiza que esta idea es un negocio de restauracion sin local a pie de calle que opera exclusivamente a traves de plataformas de delivery.

Infiere que las funciones criticas son:
- Margen real despues de comisiones de plataforma
- Posicionamiento en apps de delivery frente a la competencia
- Coste de produccion y control de calidad en pedidos de alto volumen
- Diferenciacion en un mercado saturado de opciones saludables
- Licencia de actividad de cocina
- Logistica de entrega y dependencia del repartidor

Y construye un comite especifico para estas funciones.

---

## Ejemplo de comite generado dinamicamente

Para la idea de dark kitchen del ejemplo anterior, el comite podria ser:

**Analista de economicas de delivery y comisiones de plataforma**
Funcion: evaluar si el margen es viable despues de las comisiones de Glovo, Uber Eats y Just Eat.

**Especialista en posicionamiento en apps de delivery**
Funcion: analizar como se compite con los 40-80 locales que ya venden bowls en Madrid en las mismas plataformas.

**Responsable de produccion y control de tiempos**
Funcion: evaluar la velocidad de produccion necesaria para mantener la calidad en pedidos simultaneos.

**Analista de diferenciacion de marca en entorno sin local fisico**
Funcion: determinar si hay alguna razon para que un cliente elija este local y no los otros.

**Especialista en margenes por canal de venta**
Funcion: calcular el ticket medio necesario para ser rentable y si ese ticket es competitivo en el mercado.

**Consultor de licencias de actividad de cocina**
Funcion: evaluar los requisitos administrativos y sanitarios para operar una cocina sin servicio en sala.

**Abogado del Diablo**
Funcion: encontrar por que esta idea va a fracasar.

**Evaluador Final**
Funcion: emitir el veredicto con la informacion de todos los agentes.

---

## Ejemplo de veredicto

Para la idea de dark kitchen del ejemplo:

**VEREDICTO: VALIDAR**

Las plataformas de delivery tienen margenes que comprimen fuertemente la rentabilidad. El mercado de bowls saludables en Madrid esta saturado. Antes de invertir en equipamiento y licencias, es necesario confirmar que hay un nicho de diferenciacion real y que el margen unitario es positivo en el precio que el mercado acepta. La prueba minima es un unit economics test con precios reales de plataforma mas un outreach a potenciales clientes para verificar la propuesta de diferenciacion.

---

## Limitaciones

**La Skill no sustituye el juicio del usuario.** Es una herramienta de analisis critico, no una autoridad que toma decisiones.

**La calidad del analisis depende de la calidad de la informacion.** Si la idea es vaga o el usuario no proporciona contexto suficiente, el nivel de confianza del analisis sera bajo aunque la puntuacion sea alta.

**La Skill no tiene acceso a datos de mercado en tiempo real.** Trabaja con el conocimiento del modelo y la informacion que proporciona el usuario.

**El veredicto no es una garantia.** Una idea con veredicto VALIDAR puede fracasar. Una idea con veredicto DESCARTAR puede tener exito en manos de alguien con recursos o contexto que la Skill no conocia.

**Los agentes son simulaciones.** No hay expertos reales detras del comite. La Skill simula perspectivas especializadas con el conocimiento del modelo.

---

## Proxima evolucion posible

- Evaluacion comparativa de dos ideas en el mismo analisis
- Modo de seguimiento: reevaluar una idea tras completar la prueba de validacion
- Especializacion por sector con capas adicionales de conocimiento regulatorio
- Generacion de un plan de validacion con tareas ordenadas y asignadas
- Integracion con fuentes de datos externas para metricas de mercado
