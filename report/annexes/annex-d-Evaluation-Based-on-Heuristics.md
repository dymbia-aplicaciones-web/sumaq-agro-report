## Evaluación de User Experience según Heurísticas

### SITE o APP A EVALUAR

**SumaqAgro – Web Application**

### TAREAS A EVALUAR

El alcance de esta evaluación incluye la revisión de la usabilidad, el diseño inclusivo y la arquitectura de información de las siguientes tareas:

1. Registrar una cuenta de usuario e iniciar sesión.
2. Registrar una nueva parcela y definir su ubicación geográfica.
3. Registrar un gasto asociado a una campaña agrícola.
4. Consultar el estado de salud de los cultivos y sus alertas.
5. Consultar los certificados de calidad de los lotes de cosecha.
6. Seleccionar un plan de suscripción y completar el pago simulado.

No están incluidas en esta etapa:

1. La validación de credenciales contra el backend.
2. La entrega de correos de recuperación.
3. El proceso completo de registro.
4. La navegación posterior al inicio de sesión.


### ESCALA DE SEVERIDAD

| Nivel | Descripción |
|---|---|
| 1 | Problema superficial. No impide completar la tarea y puede corregirse cuando exista disponibilidad de tiempo. |
| 2 | Problema menor. Genera confusión o esfuerzo adicional, pero permite continuar. Su corrección tiene prioridad baja. |
| 3 | Problema mayor. Dificulta considerablemente una tarea y debe corregirse con prioridad alta. |
| 4 | Problema muy grave. Impide completar una tarea esencial y debe corregirse antes del lanzamiento. |

### TABLA RESUMEN

| # | Problema | Severidad | Heurística/Principio vulnerado |
|---|---|---|---|
| 1 | Se muestra un aviso técnico de licencia inválida en la pantalla de acceso. | 2 | Usabilidad: Diseño estético y minimalista. |
| 2 | Los campos utilizan el texto interior como única identificación visual. | 2 | Usabilidad: Reconocimiento antes que recuerdo. |
| 3 | Las opciones de idioma se presentan únicamente mediante abreviaturas. | 1 | Usabilidad: Correspondencia entre el sistema y el mundo real. |

### DESCRIPCIÓN DE PROBLEMAS

### PROBLEMA #1: No se informan los requisitos de la contraseña antes de crear la cuenta

**Severidad:** 2 — Problema menor.

**Heurística violada:** Usabilidad — Prevención de errores.

**Problema:**

En el formulario “Crea tu cuenta”, el campo “Contraseña” no presenta instrucciones visibles sobre los requisitos que debe cumplir. La aplicación exige un mínimo de ocho caracteres, pero esta condición no se comunica antes de enviar el formulario.

Esto puede provocar que el usuario ingrese una contraseña demasiado corta y descubra la restricción después de intentar crear la cuenta, obligándolo a corregir los datos y repetir la acción.

**Imagen:**

![Register](../assets/img/heuristics/register-hs.png)

**Recomendación:**

Agregar debajo del campo una indicación permanente: “La contraseña debe tener al menos 8 caracteres”. Complementar esta ayuda con una validación durante la escritura o al salir del campo, e informar junto a “Confirmar contraseña” cuando ambos valores no coincidan.