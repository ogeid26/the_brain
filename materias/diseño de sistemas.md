# Teoría

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

