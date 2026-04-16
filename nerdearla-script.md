================================================================================
SCRIPT DETALLADO - "El 80% de AI es gratis. El 20% restante puede costarte todo."
================================================================================

TIMING TOTAL: 25 minutos
ESTRUCTURA: Nico abre (0:00 - 2:00), ambos (2:00 - 20:00), Sergio cierra (20:00 - 25:00)

TOTAL DE SLIDES: 31

NOTA IMPORTANTE: En cada slide habla SOLO UNA PERSONA, excepto SLIDE 2 donde se presentan juntos.

================================================================================
SLIDE 1: PORTADA (0:00 - 0:30)
================================================================================

[Pausa de 5 segundos para que el público se acomude]

NICO:
"El 80% de AI es gratis. El 20% restante puede costarte todo.

Dos perspectivas reales sobre AI en organizaciones de ingeniería.

Nerdearla Chile, 2026."

[Pausa de 5 segundos]

================================================================================
SLIDE 2: PRESENTACIÓN CONJUNTA (0:30 - 1:30) - AMBOS HABLAN
================================================================================

NICO:
"Hola. Yo soy Nico. Soy tech leader. Paso mis días construyendo cosas con AI: 
firmware, automatizaciones, prototipos. Vivo en el 80% constantemente."

SERGIO:
"Y yo soy Sergio. Escalé la adopción de AI a centenares de devs. 
Enfrenté el 20%: guardrails, coherencia, confianza. Pasé años lidiando con lo que pasa 
cuando el modelo se desvía."

NICO:
"Ahora, dato curioso: somos nerds del café. Hasta tostamos en conjunto."

SERGIO:
"Hicimos todas las montañas rusas de 4 parques de Disney en 1 día."

NICO:
"Hoy vamos a contar qué aprendimos sobre AI en producción. Sin demos de laboratorio. Sin slides de vendors. 
Solo lo que funciona, lo que no, y por qué esa brecha sigue siendo tan grande."

[Timer: 1:00]

================================================================================
SLIDE 3: HOOK / EL PROBLEMA (1:30 - 2:00) - NICO Y SERGIO
================================================================================

NICO:
"Vamos a empezar con esto. Hace poco armé un monitor de consumo de API con un 
microcontrolador ESP32, una pantalla OLED y Claude como copiloto.

En 2 horas estaba funcionando. Perfecto. Era el 80%."

SERGIO:
"En 4 meses implementamos un modelo de desarrollo basado en AI a centenares de devs. 
Con guardrails claros, estandarización, coherencia. El primer piloto funcionó en 2 semanas.

Lo difícil empezó después."

NICO:
"Ambas cosas son verdad al mismo tiempo."

[Cambiar a SLIDE 4]

================================================================================
SLIDE 4: SECCIÓN 1 - EL REGALO (2:00 - 2:30) - NICO
================================================================================

NICO:
"La IA generativa rompió una barrera histórica. Hoy cualquier engineer puede 
llegar al 80% de una solución en horas.

Vamos a explicar con casos reales qué significa ese 80%."

[Cambiar a SLIDE 5]

[Timer: 2:30]

================================================================================
SLIDE 5: CASO NICO #1 - LLEVANDO A CLAUDE AL MUNDO FÍSICO (2:30 - 4:00) - NICO
================================================================================

NICO:
"Empecemos conmigo. Hace poco necesitaba monitorear cuántos tokens estaba gastando 
en las APIs de Claude. Conectar un microcontrolador a una API.

Pero aquí está lo importante: lo hice funcionar en 2 horas. El ESP32 enviaba requests 
a Claude, obtenía datos, los mostraba en una pantallita OLED. Bonito, rápido.

Pero ahí vino el problema. Cloudflare bloquea requests que no vienen de un navegador 
autenticado. Mi ESP32 no es un navegador.

Así que tuve que armar un mini servidor en mi compu que actúa como proxy. 
El ESP32 le pega a ese servidor local, que a su vez habla con Claude. 
Funcionó. Pero requirió capas extra de indirección.

Ese es el patrón del 80%: rápido, funciona, pero no pensaste en todas las capas 
de la realidad. Y cuando las encontrás, necesitás arreglarlo."

[Timer: 4:00]

================================================================================
SLIDE 5.5: CLAUDE MONITOR EN ACCIÓN (4:00 - 4:30) - NICO
================================================================================

NICO:
"Así se ve en acción: la app que monitorea los tokens y el hardware ESP32 
con el display OLED mostrando los datos en tiempo real."

[Timer: 4:30]

================================================================================
SLIDE 6: CASO NICO #2 - MISSION CONTROL PERSONAL (4:30 - 5:30) - NICO
================================================================================

NICO:
"Tengo otro ejemplo más grande: armé algo que llamo 'Mission Control personal'.

La idea es simple: integrar TODO en un mismo lugar. Mis tareas, mis datos de salud 
que salen de un reloj Garmin, el tracking de los paquetes que me van a llegar, 
todos los gastos que hago con tarjeta tap and pay. Un hub central donde ves tu vida.

¿Cuánto tardé? Una tarde. ¿Funciona? Sí. ¿Me da visibility total? Sí.

Pero el 20%: backup de datos, seguridad, notificaciones push, 
exposición a internet, más integraciones.

Está en 80% porque es para mí. Si fuera para vender, eso sería work.

La lección es ésta: el 80% es increíblemente accesible ahora. 
Cualquiera puede construir algo que 'funciona' en horas. 
Lo que diferencia un prototipo de un producto es exactamente ese 20% que nadie ve."

[Timer: 5:30]

================================================================================
SLIDE 6.5: MISSION CONTROL EN ACCIÓN (5:30 - 6:00) - NICO
================================================================================

NICO:
"Aquí se ve el Mission Control: el dashboard con todo integrado, 
la sección de salud desde Garmin, y el menú lateral con todas las opciones."

[Timer: 6:00]

================================================================================
SLIDE 7: SECCIÓN 2 - LA TRAMPA (6:00 - 6:30) - SERGIO
================================================================================

SERGIO:
"Ahora viene mi parte. El 80% es democratizado. Eso está claro. 
Pero ese 20% no es lineal.

No es un 20% más tiempo, más esfuerzo. Es exponencialmente más difícil."

[Timer: 6:30]

================================================================================
SLIDE 8: CASO SERGIO #1 - GUARDRAILS QUE SE ROMPEN (6:30 - 9:00) - SERGIO
================================================================================

SERGIO:
"Implementamos un modelo de desarrollo basado en IA a centenares de devs. 
Con guardrails claros. Skills específicos. Estandarización.

La idea era que todos los devs usaran el modelo de la misma forma, 
que el código fuera coherente, predecible.

¿El 80%? Funcionó. Centenares de engineers lo adoptaron. Aceleró el development. 
Todo parecía estar bajo control.

Pero con el tiempo, el modelo comenzó a desviarse de la fuerza.

Los engineers encontraron formas creativas de saltar guardrails. 
Prompts que confundían el modelo. Contextos que no preveíamos. 
El modelo alucinaba en contextos no esperados.

Y la coherencia que ganamos en el 80%? Se quiebra.

El 20% fue: mantener que el modelo siga siendo confiable. 
Auditar constantemente dónde se desvía. Reentrenar skills. 
Human in the loop obligatorio. No es 'set and forget'. Es trabajo continuo.

Y eso tiene costo: en tiempo de dev, en overhead operativo, en governance, 
en que tenés que confiar en algo pero también validar que funciona."

[Timer: 9:00]

================================================================================
SLIDE 9: CASO SERGIO #2 - CLIENTES QUE LLEGARON AL 80% SOLOS (9:00 - 12:00) - SERGIO
================================================================================

SERGIO:
"Ahora voy a lo que está pasando en el mundo real con nuestros clientes.

Hace 4 meses, un cliente nos llama. 'Queremos escalar AI en nuestro desarrollo. 
Ayudennos a hacerlo.' Cero AI todavía.

Hoy, hace apenas 4 meses, voy a visitarlo. Me abre la puerta y me dice: 
'Mirá, ya tenemos una POC armada. Por nosotros.'

No me necesitaban para llegar al 80%. Lo hicieron solos.

¿Sabés qué significa eso?

Que el 80% se democratizó TANTO que ya no es un diferencial. 
Los clientes ya lo hacen. El acceso es libre. La barrera bajó a cero.

Pero aquí está lo interesante: la POC que armaron tiene exactamente 
los problemas que describimos. Desvíos en los guardrails. Coherencia cuestionable. 
Confianza baja.

Y AHÍ me necesitan. Para industrializar. Para que no se erosione. 
Para que ese 80% que les funciona no se convierte en un problema.

La lección es brutal: el 80% es gratis ahora. Lo que se vende es el 20%."

[Timer: 12:00]

================================================================================
SLIDE 10: CASO SERGIO #3 - CYBORG ENGINEERS (12:00 - 15:00) - SERGIO
================================================================================

SERGIO:
"Tengo un último caso que es sobre economía.

Hace 3 años: un equipo de desarrollo 'completo' costaba mucho. 
Talento senior era limitado, caro, difícil de contratar.
Solo las grandes empresas podían pagarlo.

Hoy: con 'cyborg engineers' — un human más AI, trabajando en conjunto — 
puedes tener capacidad similar por una fracción del costo.

El ticket baja. El acceso se democratiza. Una startup que antes no podía 
permitirse un equipo de 5 seniors ahora puede tener esa capacidad con 3 juniors 
más IA.

Eso es BUENO. Es democratización real.

PERO.

No puedes simplemente bajar el precio y esperar que todo funcione igual.

El 20% es: ¿cómo mantengo estándares? ¿Cómo audito? ¿Cómo valido? 
¿Cómo evito que código malo generado por AI entre a producción?

Porque acá está el punto: más acceso requiere MÁS governance, no menos.

Democratización ≠ Lawlessness."

[Timer: 15:00]

================================================================================
SLIDE 11: SECCIÓN 3 - EL PATRÓN (15:00 - 15:30) - SERGIO
================================================================================

SERGIO:
"Entonces, ¿quiénes lo logran? ¿Quiénes cruzan ese abismo?

Las organizaciones que logran pasar del 80% al 100% tienen esto en común."

[Cambiar a SLIDE 12]

[Timer: 15:30]

================================================================================
SLIDE 12: QUIÉNES LO LOGRAN (15:30 - 18:30) - SERGIO
================================================================================

SERGIO:
"Primero: empiezan aburrido. No persiguen el caso de uso más sexy. 
Buscan el más controlable, donde puedas medir el éxito sin sorpresas.

Segundo: tratan AI como infraestructura, no como un proyecto especial. 
Como un layer más de tu stack. Con SLAs. Con monitoreo. Con governance.

Tercero: miden outcomes reales. No 'cuántos usan Copilot'. 
'Cuánto bajó el cycle time'. No 'qué tan bonito es el modelo'. 
'Cuántas veces alucina'.

Y cuarto, el más importante: el liderazgo entiende que el 20% hay que pagarlo. 
Y tiene presupuesto para hacerlo. No es una sorpresa. Es parte del plan desde el día 1.

Si falta uno de estos cuatro, no lo logran.

Y el error más común?"

[Timer: 18:30]

================================================================================
SLIDE 13: EL ANTI-PATRÓN (18:30 - 20:00) - SERGIO
================================================================================

SERGIO:
"Llegan al 80%. Y dicen: 'Esto es transformación. Misión cumplida.'

No. Se quedaron en el 80% y lo llamaron éxito.

En una startup o un proyecto personal: está bien. El 80% ya da valor. 
Funciona. Genera beneficio.

Pero en una empresa que vende servicios o productos? 
Ese 80% es un prototipo. El 20% es lo que lo diferencia de un producto.

Y eso es lo que pasa ahora con la IA: muchas organizaciones están celebrando 
que llegaron al 80% y llamándolo 'transformación digital'. 
Pero el trabajo real — el que define qué tan robusta es tu arquitectura — 
está recién empezando."

[Timer: 20:00]

================================================================================
SLIDE 13.5: EL CONCEPTO CENTRAL (20:00 - 20:30) - SERGIO
================================================================================

SERGIO:
"Esta tabla resume todo. El 80% es democrático. El 20% depende de quién sos.

Con AI llegás al 80% en horas. El 20% restante puede costarte meses, o tu empresa."

[Timer: 20:30]

================================================================================
SLIDE 14: FRAMEWORK DE DECISIÓN (20:30 - 22:30) - SERGIO
================================================================================

SERGIO:
"Entonces ¿cómo sé si el 20% es para mí?

Hay un framework simple para hacerte la pregunta correcta.

¿Dónde estoy parado con AI?

Si es un experimento interno? El 80% alcanza. Experimenta. Aprende. Itera.

¿Toca datos sensibles o usuarios reales? El 20% no es opcional. 
Seguridad, auditoría, confianza son non-negotiable.

¿Escala a miles de usuarios o devs? El 20% se multiplica. 
Cada decisión del modelo impacta a centenares de personas. El costo del error es alto.

No hay respuesta universal. Hay contexto."

[Timer: 22:30]

================================================================================
SLIDE 15: CIERRE (22:30 - 24:00) - NICO Y SERGIO
================================================================================

NICO:
"La IA no es magia ni mentira. Es una herramienta que llegó al 80% 
más rápido de lo que cualquiera esperaba.

Pero lo que hacés con el 20% restante?"

SERGIO:
"Eso dice todo sobre el tipo de organización que sos."

NICO:
"Antes de irte de acá, identifica un caso donde estás en el 80%.

Pregúntate conscientemente: ¿es una decisión o un descuido?

Porque la diferencia es importante."

[Timer: 24:00]

================================================================================
SLIDE 16: GRACIAS (24:00 - 25:00) - AMBOS
================================================================================

NICO y SERGIO (juntos):
"Gracias."

[Pausa de 10 segundos]

SERGIO:
"Preguntas?"

[FIN - Timer: 25:00]

================================================================================
NOTAS PARA EL ENSAYO
================================================================================

1. PAUSAS: Son críticas. Cada [Pausa] es 2-3 segundos mínimo. 
   Sin pausas la charla suena apresurada.

2. ÉNFASIS: Las palabras en MAYÚSCULAS son puntos clave. Léelas con más lentitud.

3. TIMING: El script está diseñado para 25 minutos exactos. 
   Si practican y les sobra tiempo, usen las pausas para dejar que las ideas "respiren".

4. DISTRIBUCIÓN POR SPEAKER:
   - SLIDE 1: Nico
   - SLIDE 2: Ambos (presentación)
   - SLIDES 3-6.5: Nico (casos)
   - SLIDES 7-14: Sergio (casos y patrones)
   - SLIDE 15: Ambos (cierre)
   - SLIDE 16: Ambos (gracias + Q&A)

5. TRANSICIONES: Cada speaker habla su sección completa. 
   No hay interrupciones entre ellos (excepto en presentación y cierre).

6. ENSAYAN JUNTOS: Mínimo 3-4 veces. La primera pasada será de 30+ minutos. 
   Cada ensayo la va a afinar.

7. CASOS: Si quieren añadir una anécdota más específica (un número concreto, 
   una fecha, un error particular que cometieron), insertenla donde diga [Pausa]. 
   Eso no rompe el timing.

8. CIERRE: El último slide es deliberadamente corto. 15 segundos de Q&A is enough. 
   Si vuelca más preguntas, genial, pero no lo planeamos.

9. NUEVOS SLIDES VISUALES:
   - SLIDE 5.5: Claude Monitor (app + hardware)
   - SLIDE 6.5: Mission Control (dashboard, health, menu)
   - SLIDE 13.5: El concepto central (tabla comparativa)

================================================================================
