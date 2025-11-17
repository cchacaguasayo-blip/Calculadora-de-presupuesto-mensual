# Calculadora-de-presupuesto-mensual
La Calculadora de Presupuesto Mensual es una aplicación que permite al usuario registrar sus ingresos y gastos mensuales, clasificarlos y obtener un balance final que le indique si está dentro de su presupuesto o si presenta déficit.

 Objetivos del Proyecto

Facilitar al usuario el cálculo del presupuesto mensual.

Registrar ingresos y gastos en categorías.

Mostrar el balance final de manera clara.

Aplicar documentación técnica estructurada.

Utilizar control de versiones con Git y GitHub.

 Requerimientos Funcionales y No Funcionales (v1)
Funcionales

El sistema permite ingresar el monto total de ingresos.

El usuario puede registrar gastos manualmente.

El sistema calcula el balance final (ingresos – gastos).

No Funcionales

Interfaz simple y entendible.

Respuesta inmediata al cálculo.

Los datos deben ser mostrados de forma clara y ordenada.

 Requerimientos Funcionales y No Funcionales (v2)
Funcionales

Permitir registrar categorías de gastos (comida, transporte, servicios, etc.).

Generar un resumen de gastos por categoría.

Mostrar advertencia cuando los gastos superan los ingresos.

No Funcionales

Mejoras de usabilidad en botones y mensajes.

Diseño responsivo para dispositivos móviles.

Optimización del cálculo sin recargar la página.

 Plan de Pruebas Funcionales
Caso de Prueba	Descripción	Datos de Entrada	Resultado Esperado	Validación
CP01	Calcular presupuesto básico	Ingresos: 500, Gastos: 300	Balance: 200	✔ Cálculo correcto
CP02	Advertencia por gastos altos	Ingreso: 400, Gastos: 500	Mensaje: “Gastos superan ingresos”	✔ Advertencia mostrada
CP03	Categorías de gasto	Categoría: Comida, Monto: 50	Registro exitoso	✔ Aparece en listado
 Tipo de Mantenimiento Propuesto
Mantenimiento Perfectivo

Se elige mantenimiento perfectivo porque se agregan funciones nuevas en la versión 2 (categorías, advertencias, mejoras de interfaz) que perfeccionan el sistema sin corregir errores graves.

 Reflexión sobre el Control de Versiones
El uso de Git y GitHub permitió organizar cada entrega (v1 y v2), registrar cambios y mantener un historial claro del proyecto.
Los commits ayudaron a documentar la evolución del sistema y evitar pérdida de archivos, además de permitir comparar versiones antes y después de las mejoras.
El uso de Git y GitHub permitió organizar cada entrega (v1 y v2), registrar cambios y mantener un historial claro del proyecto.
Los commits ayudaron a documentar la evolución del sistema y evitar pérdida de archivos, además de permitir comparar versiones antes y después de las mejoras.
