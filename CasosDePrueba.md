# Casos de Prueba

## [Casos de prueba en Google Sheets](https://docs.google.com/spreadsheets/d/15xFU5RRDqvDir1Zi-TJ2CQpVB_ZR88Py/edit?usp=sharing&ouid=112670958619645052421&rtpof=true&sd=true)

## Índice
1. [Introducción](#introducción)
2. [Casos de Prueba para la Funcionalidad de Métodos de Pago](#casos-de-prueba-para-la-funcionalidad-de-métodos-de-pago)
3. [Casos de Prueba para la Lógica del Botón de Reserva](#casos-de-prueba-para-la-lógica-del-botón-de-reserva)
4. [Casos de Prueba para la Lógica del Campo "Desde" y "Hasta"]( #casos-de-prueba-para-la-lógica-del-campo-desde-y-hasta)
5. [Casos de Prueba para la Integración de Nuevos Modos de Transporte](#casos-de-prueba-para-la-integración-de-nuevos-modos-de-transporte)
6. [Criterios de Aceptación](#criterios-de-aceptación)
7. [Recursos Necesarios](#recursos-necesarios)
8. [Responsable de las Pruebas](#responsable-de-las-pruebas)


## Introducción
Este documento detalla los casos de prueba diseñados para validar las funcionalidades del sistema relacionado con los métodos de pago, la lógica del botón de reserva, la lógica de los campos "Desde" y "Hasta", y la integración de nuevos modos de transporte. Cada caso de prueba incluye una descripción, datos de prueba y resultados esperados para garantizar la calidad y funcionalidad del sistema.

## Casos de Prueba para la Funcionalidad de Métodos de Pago

1. **CT001**: **Abrir Ventana "Opción de Pago"**
    - **Descripción**: Verificar que al dar clic en el campo "Método de pago", se abre la ventana "Opción de pago".
    - **Datos de Prueba**: Hacer clic en el campo "Método de pago".
    - **Resultado Esperado**: La ventana "Opción de pago" se abre.

2. **CT002**: **Abrir Formulario "Agregar una Tarjeta"**
    - **Descripción**: Verificar que al dar clic en la etiqueta "Añadir tarjeta" en la ventana "Opción de pago", se abre el formulario "Agregar una tarjeta".
    - **Datos de Prueba**: Hacer clic en la etiqueta "Añadir tarjeta".
    - **Resultado Esperado**: El formulario "Agregar una tarjeta" se abre.

3. **CT003**: **Botón "Agregar" Activo con Datos Correctos**
    - **Descripción**: Verificar que al llenar correctamente los campos "Número de tarjeta" y "Código" y quitar el foco, el botón "Agregar" se pinta de color azul.
    - **Datos de Prueba**: Ingresar un número de tarjeta válido y un código válido.
    - **Resultado Esperado**: El botón "Agregar" se pinta de color azul.

4. **CT004**: **Botón "Agregar" Inactivo con Datos Incorrectos**
    - **Descripción**: Verificar que al llenar incorrectamente alguno de los campos del formulario "Agregar una tarjeta", el botón "Agregar" permanece bloqueado y en color gris.
    - **Datos de Prueba**: Ingresar datos incorrectos en alguno de los campos.
    - **Resultado Esperado**: El botón "Agregar" permanece bloqueado y en color gris.

5. **CT005**: **Cerrar Formulario sin Guardar**
    - **Descripción**: Verificar que al dar clic en el botón "Cancelar" dentro del formulario "Agregar tarjeta", el formulario se cierra sin guardarse.
    - **Datos de Prueba**: Hacer clic en el botón "Cancelar".
    - **Resultado Esperado**: El formulario se cierra sin guardar cambios.

6. **CT006**: **Cerrar Ventana sin Método Registrado**
    - **Descripción**: Verificar que al dar clic en el botón "X" de la ventana emergente "Opción de pago" sin tener algún método registrado, esta se cierra.
    - **Datos de Prueba**: Hacer clic en el botón "X" sin métodos registrados.
    - **Resultado Esperado**: La ventana emergente se cierra.

7. **CT007**: **Cerrar Ventana con Método Registrado**
    - **Descripción**: Verificar que al dar clic en el botón "X" de la ventana emergente "Opción de pago" con algún método registrado, esta se cierra guardando el método seleccionado.
    - **Datos de Prueba**: Hacer clic en el botón "X" con métodos registrados.
    - **Resultado Esperado**: La ventana emergente se cierra y el método seleccionado se guarda.

8. **CT008**: **Agregar Espacios en el Campo "Número de Tarjeta"**
    - **Descripción**: Verificar que al introducir 12 caracteres en el campo "Número de tarjeta" y quitar el foco, se agregan automáticamente los espacios.
    - **Datos de Prueba**: Introducir 12 números en el campo "Número de tarjeta".
    - **Resultado Esperado**: Los espacios se agregan automáticamente.

9. **CT009**: **Campo "Número de Tarjeta" con Menos de 12 Caracteres**
    - **Descripción**: Verificar que si se introducen menos de 12 caracteres en el campo "Número de tarjeta" y se llena el campo "Código" correctamente, el botón "Añadir tarjeta" permanece inactivo.
    - **Datos de Prueba**: Introducir menos de 12 números en el campo "Número de tarjeta" y un código válido.
    - **Resultado Esperado**: El botón "Añadir tarjeta" permanece inactivo.

10. **CT010**: **Campo "Número de Tarjeta" con Más de 12 Caracteres**
    - **Descripción**: Verificar que en el campo "Número de tarjeta" no se permite introducir más de 12 caracteres.
    - **Datos de Prueba**: Introducir 13 números en el campo "Número de tarjeta".
    - **Resultado Esperado**: No se permiten más de 12 caracteres.

11. **CT011**: **Campo "Número de Tarjeta" con Caracteres Especiales**
    - **Descripción**: Verificar que el campo "Número de tarjeta" no permite añadir caracteres especiales.
    - **Datos de Prueba**: Intentar ingresar caracteres especiales en el campo "Número de tarjeta".
    - **Resultado Esperado**: No se permiten caracteres especiales.

12. **CT012**: **Campo "Número de Tarjeta" con Letras**
    - **Descripción**: Verificar que el campo "Número de tarjeta" no permite introducir letras.
    - **Datos de Prueba**: Intentar ingresar letras en el campo "Número de tarjeta".
    - **Resultado Esperado**: No se permiten letras.

13. **CT013**: **Campo "Código" con Menos de 2 Números**
    - **Descripción**: Verificar que si se introducen menos de 2 números en el campo "Código", el botón "Añadir tarjeta" permanece inactivo.
    - **Datos de Prueba**: Introducir menos de 2 números en el campo "Código".
    - **Resultado Esperado**: El botón "Añadir tarjeta" permanece inactivo.

14. **CT014**: **Campo "Código" con Más de 2 Caracteres**
    - **Descripción**: Verificar que en el campo "Código" no se permite introducir más de 2 caracteres.
    - **Datos de Prueba**: Introducir 3 números en el campo "Código".
    - **Resultado Esperado**: No se permiten más de 2 caracteres.

15. **CT015**: **Campo "Código" con Letras**
    - **Descripción**: Verificar que el campo "Código" no permite letras.
    - **Datos de Prueba**: Intentar ingresar letras en el campo "Código".
    - **Resultado Esperado**: No se permiten letras.

16. **CT016**: **Campo "Código" con Caracteres Especiales**
    - **Descripción**: Verificar que el campo "Código" no permite caracteres especiales.
    - **Datos de Prueba**: Intentar ingresar caracteres especiales en el campo "Código".
    - **Resultado Esperado**: No se permiten caracteres especiales.

17. **CT017**: **Campo "Código" con Número "00"**
    - **Descripción**: Verificar que el número "00" no se permite en el campo "Código".
    - **Datos de Prueba**: Introducir "00" en el campo "Código".
    - **Resultado Esperado**: El número "00" no es permitido.

18. **CT018**: **Campo "Número de Tarjeta" con 10 Números**
    - **Descripción**: Verificar que al introducir 10 números en el campo "Número de tarjeta", el botón "Añadir" permanece bloqueado.
    - **Datos de Prueba**: Introducir 10 números en el campo "Número de tarjeta".
    - **Resultado Esperado**: El botón "Añadir" permanece bloqueado.

19. **CT019**: **Campo "Número de Tarjeta" con 11 Números**
    - **Descripción**: Verificar que al introducir 11 números en el campo "Número de tarjeta", el botón "Añadir" permanece bloqueado.
    - **Datos de Prueba**: Introducir 11 números en el campo "Número de tarjeta".
    - **Resultado Esperado**: El botón "Añadir" permanece bloqueado.

20. **CT020**: **Campo "Número de Tarjeta" con 13 Números**
    - **Descripción**: Verificar que al introducir 13 números en el campo "Número de tarjeta", estos no son permitidos y no se deja escribir más de 12.
    - **Datos de Prueba**: Introducir 13 números en el campo "Número de tarjeta".
    - **Resultado Esperado**: Solo se permiten 12 números y el campo no acepta más.

21. **CT021**: **Campo "Número de Tarjeta" con 14 Números**
    - **Descripción**: Verificar que al introducir 14 números en el campo "Número de tarjeta", estos no son permitidos y no se deja escribir más de 12.
    - **Datos de Prueba**: Introducir 14 números en el campo "Número de tarjeta".
    - **Resultado Esperado**: Solo se permiten 12 números y el campo no acepta más.

22. **CT022**: **Campo "Código" con 0 Números**
    - **Descripción**: Verificar que al introducir 0 números en el campo "Código", estos no son permitidos y el botón "Añadir" permanece bloqueado.
    - **Datos de Prueba**: Dejar vacío el campo "Código".
    - **Resultado Esperado**: El botón "Añadir" permanece bloqueado.

23. **CT023**: **Campo "Código" con 1 Número**
    - **Descripción**: Verificar que al introducir 1 número en el campo "Código", estos no son permitidos y el botón "Añadir" permanece bloqueado.
    - **Datos de Prueba**: Introducir 1 número en el campo "Código".
    - **Resultado Esperado**: El botón "Añadir" permanece bloqueado.

24. **CT024**: **Campo "Código" con 3 Números**
    - **Descripción**: Verificar que al introducir 3 números en el campo "Código", estos no son permitidos y no se deja escribir más de 2.
    - **Datos de Prueba**: Introducir 3 números en el campo "Código".
    - **Resultado Esperado**: Solo se permiten 2 números y el campo no acepta más.

25. **CT025**: **Campo "Código" con 4 Números**
    - **Descripción**: Verificar que al introducir 4 números en el campo "Código", estos no son permitidos y no se deja escribir más de 2.
    - **Datos de Prueba**: Introducir 4 números en el campo "Código".
    - **Resultado Esperado**: Solo se permiten 2 números y el campo no acepta más.

26. **CT026**: **Agregar Múltiples Tarjetas**
    - **Descripción**: Verificar que se puede agregar más de una tarjeta.
    - **Datos de Prueba**: Agregar múltiples tarjetas válidas.
    - **Resultado Esperado**: Se pueden agregar múltiples tarjetas.

27. **CT027**: **Campo "Número de Tarjeta" Vacío**
    - **Descripción**: Verificar que al llenar correctamente el campo "Número de tarjeta" pero dejar vacío el campo "Código", el botón "Agregar" permanece bloqueado.
    - **Datos de Prueba**: Llenar el campo "Número de tarjeta" y dejar el campo "Código" vacío.
    - **Resultado Esperado**: El botón "Agregar" permanece bloqueado.

28. **CT028**: **Campo "Código" Vacío**
    - **Descripción**: Verificar que al dejar vacío el campo "Número de tarjeta" pero llenar correctamente el campo "Código", el botón "Agregar" permanece bloqueado.
    - **Datos de Prueba**: Llenar el campo "Código" y dejar el campo "Número de tarjeta" vacío.
    - **Resultado Esperado**: El botón "Agregar" permanece bloqueado.

29. **CT029**: **Campos no Aceptan Letras Latinas**
    - **Descripción**: Verificar que los campos "Número de tarjeta" y "Código" no aceptan letras latinas.
    - **Datos de Prueba**: Intentar ingresar letras latinas en ambos campos.
    - **Resultado Esperado**: No se permiten letras latinas.

30. **CT030**: **Campos no Aceptan Letras No Latinas**
    - **Descripción**: Verificar que los campos "Número de tarjeta" y "Código" no aceptan letras no latinas.
    - **Datos de Prueba**: Intentar ingresar letras no latinas en ambos campos.
    - **Resultado Esperado**: No se permiten letras no latinas.

31. **CT031**: **Botón "Agregar" Activo Solo con Datos Correctos**
    - **Descripción**: Verificar que el botón "Agregar" solo se activa si los campos "Número de tarjeta" y "Código" están llenados correctamente.
    - **Datos de Prueba**: Ingresar datos correctos en ambos campos.
    - **Resultado Esperado**: El botón "Agregar" se activa.

## Casos de Prueba para la Lógica del Botón de Reserva

1. **CT032**: **Reserva con Todos los Campos Obligatorios Completos**
    - **Descripción**: Verificar la lógica del botón de reserva al completar todos los campos obligatorios del formulario de reserva.
    - **Datos de Prueba**: Completar todos los campos y direcciones requeridos, excepto el de la licencia de conducir.
    - **Resultado Esperado**: El botón de reserva se activa o muestra el comportamiento esperado.

2. **CT033**: **Reserva con Campos Obligatorios Completos y Sin Método de Pago**
    - **Descripción**: Verificar la lógica del botón de reserva al completar todos los campos y direcciones obligatorios, excepto el método de pago.
    - **Datos de Prueba**: Completar todos los campos y direcciones obligatorios, excepto el método de pago.
    - **Resultado Esperado**: El botón de reserva se activa o muestra el comportamiento esperado.

3. **CT034**: **Reserva con Campos Obligatorios Completos y Direcciones Borradas**
    - **Descripción**: Verificar la lógica del botón de reserva al completar todos los campos obligatorios y borrar las direcciones.
    - **Datos de Prueba**: Completar todos los campos obligatorios y borrar las direcciones.
    - **Resultado Esperado**: El botón de reserva se activa o muestra el comportamiento esperado.

4. **CT035**: **Reserva Sin Campos Obligatorios Completos y Direcciones Borradas**
    - **Descripción**: Verificar la lógica del botón de reserva al no completar ninguno de los campos obligatorios y borrar las direcciones.
    - **Datos de Prueba**: No completar ningún campo obligatorio y borrar las direcciones.
    - **Resultado Esperado**: El botón de reserva permanece inactivo o muestra el comportamiento esperado.

## Casos de Prueba para la Lógica del Campo "Desde" y "Hasta"

1. **CT036**: **Reserva con Solo el Campo "Desde" Relleno**
    - **Descripción**: Verificar la lógica de la reserva al rellenar solo el campo "Desde".
    - **Datos de Prueba**: Completar solo el campo "Desde".
    - **Resultado Esperado**: El sistema muestra el comportamiento esperado o el botón de reserva se activa/desactiva según sea apropiado.

2. **CT037**: **Reserva con Solo el Campo "Hasta" Relleno**
    - **Descripción**: Verificar la lógica de la reserva al rellenar solo el campo "Hasta".
    - **Datos de Prueba**: Completar solo el campo "Hasta".
    - **Resultado Esperado**: El sistema muestra el comportamiento esperado o el botón de reserva se activa/desactiva según sea apropiado.

3. **CT038**: **Cancelar Proceso de Reserva**
    - **Descripción**: Verificar la lógica de la reserva al cancelar el proceso.
    - **Datos de Prueba**: Cancelar el proceso de reserva.
    - **Resultado Esperado**: El sistema debe cancelar el proceso y regresar al estado anterior.

## Casos de Prueba para la Integración de Nuevos Modos de Transporte

1. **CT039**: **Nuevo Modo de Transporte en la Interfaz**
    - **Descripción**: Verificar que si se agrega un nuevo modo de transporte en la respuesta del servidor, este aparece en la interfaz.
    - **Datos de Prueba**: Agregar un nuevo modo de transporte en la respuesta del servidor.
    - **Resultado Esperado**: El nuevo modo de transporte aparece en la interfaz.

2. **CT040**: **Ícono del Nuevo Modo de Transporte en la Sección de Tipo de Transporte**
    - **Descripción**: Verificar que el ícono del nuevo modo de transporte se muestra en la sección de tipo de transporte y la interfaz no cambia.
    - **Datos de Prueba**: Confirmar la presencia del ícono del nuevo modo de transporte en la sección correspondiente.
    - **Resultado Esperado**: El ícono se muestra correctamente y la interfaz no cambia.

3. **CT041**: **Ícono Apagado al Cambiar de Modo**
    - **Descripción**: Verificar que el ícono del nuevo modo de transporte se apaga cuando se cambia el modo de "Personal" a cualquier otro.
    - **Datos de Prueba**: Cambiar el modo de "Personal" a otro modo.
    - **Resultado Esperado**: El ícono del nuevo modo de transporte se apaga.

4. **CT042**: **Ícono del Modo de Transporte Cambia al Estado Seleccionado**
    - **Descripción**: Verificar que el ícono del modo de transporte cambia al estado seleccionado al hacer clic en él en el modo "Personal".
    - **Datos de Prueba**: Hacer clic en el ícono del modo de transporte en el modo "Personal".
    - **Resultado Esperado**: El ícono cambia al estado seleccionado.

5. **CT043**: **Cálculo del Costo del Viaje con Nuevo Modo de Transporte**
    - **Descripción**: Verificar que el costo del viaje se calcula si todos los campos se rellenan correctamente y se selecciona un nuevo modo de transporte.
    - **Datos de Prueba**: Completar todos los campos y seleccionar un nuevo modo de transporte.
    - **Resultado Esperado**: El costo del viaje se calcula correctamente.

6. **CT044**: **Resultados del Cálculo Muestran el Nombre del Nuevo Modo de Transporte**
    - **Descripción**: Verificar que los resultados del cálculo muestran el nombre del nuevo modo de transporte que vino del servidor.
    - **Datos de Prueba**: Confirmar que el nombre del nuevo modo de transporte se muestra en los resultados del cálculo.
    - **Resultado Esperado**: El nombre del nuevo modo de transporte se muestra correctamente.

7. **CT045**: **Resultados del Cálculo Muestran el Costo y Tiempo de Viaje**
    - **Descripción**: Verificar que los resultados del cálculo muestran el costo y el tiempo de viaje en el modo de transporte recién seleccionado.
    - **Datos de Prueba**: Confirmar que el costo y el tiempo de viaje se muestran correctamente en los resultados del cálculo.
    - **Resultado Esperado**: El costo y el tiempo de viaje se muestran correctamente.

## Criterios de Aceptación
- Todos los casos de prueba deben pasar con los resultados esperados descritos.
- Cualquier fallo debe ser registrado y reportado para su resolución.

## Recursos Necesarios
- Acceso al entorno de prueba del sistema.
- Herramientas de prueba y documentación necesarias.
- Datos de prueba específicos para cada caso.

## Responsable de las Pruebas
- Nombre: David Elías Ledesma Rivera


---

**Nota**: Este documento debe actualizarse y ajustarse según los cambios en el sistema o requisitos de prueba. Los casos de prueba deben ser revisados periódicamente para asegurar su relevancia y exactitud.
