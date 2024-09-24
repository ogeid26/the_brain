[]()# Teoría

## Clase 2
**Objetivo:** Principios

- Modularización
- Refactoring: modificar el código de manera que no afecta el comportamiento del sistema pero mejora la calidad

### **Idea 1:** Dividir la función en sus principales pasos
- *Flowchart* or functional decomposition
-  El código debe ser intencional: declarar sus intenciones (en su nombre por ejemplo)

#### Modularización
Dividir un programa en módulos individuales, creando barreras de abstracción bien definidas entre ellos

**Criterio según David Parnas, 1972**
- No simplemente dividir una función en sus pasos de ejecución
- Casa módulo oculta decisiones de diseño
	- Por ejemplo mediante el uso de *getters* y *setters*
- Cada módulo expone una interfaz sin revelar detalles de implementación (encapsulation)
- Separar el código no por orden de ejecución sino por decisiones de diseño difíciles

**Beneficios**
- Comprensión
- Coordinación
- Flexibilidad
- Cambios
	- En el tiempo: mismos usuarios, cambio de requerimientos
	- Distintos usuarios que al mismo tiempo requieren diferente funcionalidad

### **Idea 2:** Dividir la función por decisiones de diseño
*Cada sub-función oculta alguna decisión importante*
- Diseñar es tomar decisiones
- Cada s


#### Acoplamiento
El grado ene le cual los módulos se interconectan o se relacionan entre ellos
#### Cohesión
El grado en el cual los componentes de un módulo son necesarios y suficientes para llevar a cabo una  sola función bien definida

**Criterio bajo acoplamiento alta cohesión**

#### Ortogonalidad
Concepto tomado de la geometría. Si yo varío un parámetro, no debería variar el otro.


## Clase 3
### Abstracción
Para la comprensión de fenómenos complejos, una de las herramientas más poderosas que tenemos es la abstracción

**Ejemplo: el toro de Picasso**

> Una abstracción denota las características esenciales de un objeto que lo distingue de todos los demás tipos de objetos y, por lo tanto, proporcionar límites conceptuales claramente definidos, en relación con la perspectiva del espectador
> 	Grady Booch


**Recomendación: Structure And Interpretation of Computer Programs (SICP book)**

En el libro:

Abstracciones:
- **Abstracción procedural:**  Creamos abstracciones al crear, componer, y combinar funciones. Separamos el qué del cómo.
- **Abstracción de datos:** Creamos abstracciones al componer datos en datos más complejos. Separamos las operaciones de la construcción interna del dato.

#### Ejemplos de abstracción
- Nombrar una variable
- Crear y nombrar funciones
- Definir interfaces
- Clasificar conceptos (jerarquías)
- Crear módulos
- Definir nuevos tipos
- Crear "DSLs" (domain-specific languages)

### Niveles de abstracción
- En cada nivel ignoramos detalles de otros niveles
- Barreras de abstracción
- Cada nivel utiliza su propio "lenguaje"

La abstracción es parecida a la ciencia en el sentido en que engloba fenómenos parecidos bajo la misma área

Las capas de una aplicación no suelen ser capas de abstracción
*Stratified Design over Layered Design*

- Programming bottom-up (Paul Graham)

Dynamic programming

**Tarea**
Leer papers de programación
- *No Silver Bullet - Essence and Accident in Software Engineering*
- *Out of the Tar Pit*
Vale la pena, importante para el parcial / final

## Clase 4

### No Silver Bullet

Dificultades
**Esenciales ->**  de la naturaleza del software en general (material, conformidades, etc.)
**Accidentales ->** cómo nosotros hacemos el software

"Ninguna mejora en las  dificultades accidentales mejorará nuestra capacidad de mejorar la solución"

*Por qué el software es difícil*
**Complejidad** , crece en forma no lineal
**Conformidad**, debe adaptarse a realidades arbitrariamente complejas
**Cambios**, constantemente bajo presión a cambios
**Invisibilidad**, difícil de visualizar, sin correlación física

### Out of the Tar Pit

> La complejidad es la principal dificultad en los sistemas de software

Diferencia entre esencial y accidental

*A diferencia de Brooks:*

**Esencial** es lo inherente al problema **según lo ve el usuario**

No concuerdan con que la mayoría de la complejidad que queda sea esencial

Mayor causa de complejidad: *estado*
En menor medida: *volumen de código*** y *control explícito de flujo*

Control de flujo: entender el programa, las partes necesarias y las que no lo son

Complejidad accidental: lo que es culpa nuestra, no del problema

#### ¿Qué es lo opuesto a complejo?
*Complejo vs. simple*
Complejo: que está compuesto por muchos elementos
Simple: compuesto por pocos elementos

*Difícil vs. fácil*

Lo que es más simple es más fácil de
- Comprender
- Cambiar
- Debuggear

Charla: [Simple Made Easy de Rich Hickey](https://www.infoq.com/presentations/Simple-Made-Easy/)


### Inmutabillidad

**Transparencia referencial:** Una expresión es referencialmente transparente si se puede reemplazar por su valor correspondiente sin cambiar el comportamiento del programa

Ventajas
- Fácil razonar acerca de código
- Fácil de probar
- Fácil de experimentar
- Se puede guardar el resultado (memoize)

Una expresión debe ser pura
- El valor de la expresión debe ser el mismo para las mismas entradas

*Inmutabilidad: objeto cuyo estado no se puede modificar después de que se ha creado*

Effective Java -> "Inmutabilidad" aparece 145 veces :0

## Clase 6
Pilares de la Orientación a Objetos
- Abstracción 
- Encapsulamiento
- Herencia
- Polimorfismo

### Abstracción

### Encapsulamiento
**Beneficios**
- Desacoplar código
- Evitar que se muestre más de lo necesario



### SOLID

#### SRP: Single Responsibility Principle
- Un módulo debe tener una única responsabilidad
- Una sola responsabilidad
- Un solo motivo de cambio
- Un módulo debe responder a cambios o intereses de un solo actor

### Liskov Substitution Principle
Objetos de un subtipo de A deben poder sustituir a objetos de tipo A


## Clase 8

### Patrones de Diseño

#### 3. Singleton
Patrón de diseño que habilita únicamente la existencia de una instancia. 

**Ejemplos**
- Caches
- Connection pooling
- `java.lang.Runtime.getRuntime()`

#### 4. Strategy
- Strategy al extremo: Entity Component System