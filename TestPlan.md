# Plan de Pruebas para la Funcionalidad de "Agregar Tarjeta" y Botón de Reserva

## 1. Objetivo del Plan de Pruebas
Validar que la funcionalidad de agregar una tarjeta, la lógica del botón de reserva en el formulario de reserva, la lógica relacionada con los campos "Desde" y "Hasta", y la integración de nuevos modos de transporte funcionan correctamente y cumplen con los requisitos especificados.

## 2. Alcance
Este plan de pruebas cubre las interacciones con los campos "Número de tarjeta" y "Código" en el formulario "Agregar una tarjeta", las acciones asociadas con los botones "Agregar", "Cancelar" y "X", la lógica del botón de reserva en el formulario de reserva, la lógica relacionada con los campos "Desde" y "Hasta", y la integración de nuevos modos de transporte en la interfaz.

## 3. Casos de Prueba

### 3.1. Navegación y Apertura de Formularios

1. **CT001**: **Abrir Ventana de Pago**
   - **Descripción**: Verificar que al hacer clic en el campo "Método de pago", se abre la ventana "Opción de pago".
   - **Datos de Prueba**: Clic en el campo "Método de pago".
   - **Resultado Esperado**: La ventana "Opción de pago" se abre.

2. **CT002**: **Abrir Formulario de Agregar Tarjeta**
   - **Descripción**: Verificar que al hacer clic en la etiqueta "Añadir tarjeta" dentro de la ventana "Opción de pago", se abre el formulario "Agregar una tarjeta".
   - **Datos de Prueba**: Clic en la etiqueta "Añadir tarjeta".
   - **Resultado Esperado**: El formulario "Agregar una tarjeta" se abre.

### 3.2. Validaciones del Campo "Número de Tarjeta"

1. **CT003**: **Botón Agregar Activado con Datos Correctos**
   - **Descripción**: Verificar que al ingresar un número de tarjeta válido (12 dígitos) y un código válido (2 dígitos) y quitar el foco, el botón "Agregar" se pinta de color azul.
   - **Datos de Prueba**: Ingresar un número de tarjeta válido (12 dígitos) y un código válido (2 dígitos), luego quitar el foco.
   - **Resultado Esperado**: El botón "Agregar" se pinta de color azul.

2. **CT004**: **Botón Agregar Desactivado con Datos Incorrectos**
   - **Descripción**: Verificar que al ingresar datos incorrectos en alguno de los campos del formulario "Agregar una tarjeta" (número de tarjeta o código), el botón "Agregar" permanece bloqueado y en color gris.
   - **Datos de Prueba**: Ingresar un número de tarjeta o código incorrecto.
   - **Resultado Esperado**: El botón "Agregar" permanece bloqueado y en color gris.

3. **CT005**: **Cancelar Formulario de Agregar Tarjeta**
   - **Descripción**: Verificar que al hacer clic en el botón "Cancelar" dentro del formulario "Agregar tarjeta", se cierra el formulario sin guardar los datos.
   - **Datos de Prueba**: Hacer clic en el botón "Cancelar".
   - **Resultado Esperado**: El formulario se cierra sin guardar los datos.

4. **CT006**: **Cerrar Ventana de Opción de Pago sin Métodos Registrados**
   - **Descripción**: Verificar que al hacer clic en el botón "X" de la ventana emergente "Opción de pago" sin tener ningún método registrado, la ventana se cierra.
   - **Datos de Prueba**: Hacer clic en el botón "X".
   - **Resultado Esperado**: La ventana se cierra.

5. **CT007**: **Cerrar Ventana de Opción de Pago con Métodos Registrados**
   - **Descripción**: Verificar que al hacer clic en el botón "X" de la ventana emergente "Opción de pago" teniendo algún método registrado, la ventana se cierra guardando el método seleccionado.
   - **Datos de Prueba**: Hacer clic en el botón "X" con un método registrado.
   - **Resultado Esperado**: La ventana se cierra y el método seleccionado se guarda.

### 3.3. Validaciones del Campo "Código"

1. **CT008**: **Campo "Número de Tarjeta" con Espacios Automáticos**
   - **Descripción**: Verificar que al introducir 12 caracteres en el campo "Número de tarjeta" y quitar el foco, se agregan automáticamente los espacios.
   - **Datos de Prueba**: Introducir 12 caracteres y quitar el foco.
   - **Resultado Esperado**: Los espacios se agregan automáticamente.

2. **CT009**: **Campo "Número de Tarjeta" con Menos de 12 Caracteres**
   - **Descripción**: Verificar que al introducir menos de 12 caracteres en el campo "Número de tarjeta" y llenar correctamente el campo "Código", el botón "Añadir tarjeta" permanece inactivo.
   - **Datos de Prueba**: Introducir menos de 12 caracteres en el campo "Número de tarjeta" y llenar correctamente el campo "Código".
   - **Resultado Esperado**: El botón "Añadir tarjeta" permanece inactivo.

3. **CT010**: **Campo "Número de Tarjeta" con Caracteres Especiales**
   - **Descripción**: Verificar que el campo "Número de tarjeta" no permite introducir caracteres especiales.
   - **Datos de Prueba**: Intentar introducir caracteres especiales en el campo "Número de tarjeta".
   - **Resultado Esperado**: Los caracteres especiales no son permitidos.

4. **CT011**: **Campo "Número de Tarjeta" con Letras**
   - **Descripción**: Verificar que el campo "Número de tarjeta" no permite introducir letras.
   - **Datos de Prueba**: Intentar introducir letras en el campo "Número de tarjeta".
   - **Resultado Esperado**: Las letras no son permitidas.

5. **CT012**: **Campo "Código" con Menos de 2 Números**
   - **Descripción**: Verificar que al introducir menos de 2 números en el campo "Código", el botón "Añadir tarjeta" permanece inactivo.
   - **Datos de Prueba**: Introducir menos de 2 números en el campo "Código".
   - **Resultado Esperado**: El botón "Añadir tarjeta" permanece inactivo.

6. **CT013**: **Campo "Código" con Más de 2 Números**
   - **Descripción**: Verificar que el campo "Código" no permite introducir más de 2 números.
   - **Datos de Prueba**: Intentar introducir más de 2 números en el campo "Código".
   - **Resultado Esperado**: No se permiten más de 2 números.

7. **CT014**: **Campo "Código" con Letras**
   - **Descripción**: Verificar que el campo "Código" no permite introducir letras.
   - **Datos de Prueba**: Intentar introducir letras en el campo "Código".
   - **Resultado Esperado**: Las letras no son permitidas.

8. **CT015**: **Campo "Código" con Caracteres Especiales**
   - **Descripción**: Verificar que el campo "Código" no permite introducir caracteres especiales.
   - **Datos de Prueba**: Intentar introducir caracteres especiales en el campo "Código".
   - **Resultado Esperado**: Los caracteres especiales no son permitidos.

9. **CT016**: **Campo "Código" con Número "00"**
   - **Descripción**: Verificar que el campo "Código" no permite el número "00".
   - **Datos de Prueba**: Introducir el número "00" en el campo "Código".
   - **Resultado Esperado**: El número "00" no es permitido.

10. **CT017**: **Campo "Número de Tarjeta" con 10 Números**
    - **Descripción**: Verificar que al introducir 10 números en el campo "Número de tarjeta", el botón "Añadir" permanece bloqueado.
    - **Datos de Prueba**: Introducir 10 números en el campo "Número de tarjeta".
    - **Resultado Esperado**: El botón "Añadir" permanece bloqueado.

11. **CT018**: **Campo "Número de Tarjeta" con 11 Números**
    - **Descripción**: Verificar que al introducir 11 números en el campo "Número de tarjeta", el botón "Añadir" permanece bloqueado.
    - **Datos de Prueba**: Introducir 11 números en el campo "Número de tarjeta".
    - **Resultado Esperado**: El botón "Añadir" permanece bloqueado.

12. **CT019**: **Campo "Número de Tarjeta" con 13 Números**
    - **Descripción**: Verificar que al introducir 13 números en el campo "Número de tarjeta", no se permite introducir más de 12 dígitos.
    - **Datos de Prueba**: Introducir 13 números en el campo "Número de tarjeta".
    - **Resultado Esperado**: No se permiten más de 12 dígitos.

13. **CT020**: **Campo "Número de Tarjeta" con 14 Números**
    - **Descripción**: Verificar que al introducir 14 números en el campo "Número de tarjeta", no se permite introducir más de 12 dígitos.
    - **Datos de Prueba**: Introducir 14 números en el campo "Número de tarjeta".
    - **Resultado Esperado**: No se permiten más de 12 dígitos.

14. **CT021**: **Campo "Código" con 0 Números**
    - **Descripción**: Verificar que al introducir 0 números en el campo "Código", el botón "Añadir" permanece bloqueado.
    - **Datos de Prueba**: Introducir 0 números en el campo "Código".
    - **Resultado Esperado**: El botón "Añadir" permanece bloqueado.

15. **CT022**: **Campo "Código" con 1 Número**
    - **Descripción**: Verificar que al introducir 1 número en el campo "Código", el botón "Añadir" permanece bloqueado.
    - **Datos de Prueba**: Introducir 1 número en el campo "Código".
    - **Resultado Esperado**: El botón "Añadir" permanece bloqueado.

16. **CT023**: **Campo "Código" con 3 Números**
    - **Descripción**: Verificar que al introducir 3 números en el campo "Código", no se permite introducir más de 2 dígitos.
    - **Datos de Prueba**: Introducir 3 números en el campo "Código".
    - **Resultado Esperado**: No se permiten más de 2 dígitos.

17. **CT024**: **Campo "Código" con 4 Números**
    - **Descripción**: Verificar que al introducir 4 números en el campo "Código", no se permite introducir más de 2 dígitos.
    - **Datos de Prueba**: Introducir 4 números en el campo "Código".
    - **Resultado Esperado**: No se permiten más de 2 dígitos.

18. **CT025**: **Agregar Más de una Tarjeta**
    - **Descripción**: Verificar que se puede agregar más de una tarjeta.
    - **Datos de Prueba**: Agregar más de una tarjeta.
    - **Resultado Esperado**: Se pueden agregar múltiples tarjetas.

19. **CT026**: **Campo "Número de Tarjeta" Vacío y Campo "Código" Lleno**
    - **Descripción**: Verificar que al llenar correctamente el campo "Número de tarjeta" pero dejar vacío el campo "Código", el botón "Agregar" permanece bloqueado.
    - **Datos de Prueba**: Llenar el campo "Número de tarjeta" y dejar vacío el campo "Código".
    - **Resultado Esperado**: El botón "Agregar" permanece bloqueado.

20. **CT027**: **Campo "Código" Lleno y Campo "Número de Tarjeta" Vacío**
    - **Descripción**: Verificar que al dejar vacío el campo "Número de tarjeta" pero llenar correctamente el campo "Código", el botón "Agregar" permanece bloqueado.
    - **Datos de Prueba**: Llenar el campo "Código" y dejar vacío el campo "Número de tarjeta".
    - **Resultado Esperado**: El botón "Agregar" permanece bloqueado.

21. **CT028**: **Campos no Aceptan Letras Latinas y No Latinas**
    - **Descripción**: Verificar que los campos "Número de tarjeta" y "Código" no aceptan letras latinas y no latinas.
    - **Datos de Prueba**: Intentar ingresar letras latinas y no latinas en los campos "Número de tarjeta" y "Código".
    - **Resultado Esperado**: No se permiten letras latinas ni no latinas.

22. **CT029**: **Activación del Botón "Agregar"**
    - **Descripción**: Verificar que el botón "Agregar" solo se activa si los campos "Número de tarjeta" y "Código" están llenos correctamente.
    - **Datos de Prueba**: Ingresar datos válidos en ambos campos.
    - **Resultado Esperado**: El botón "Agregar" se activa solo si ambos campos están correctos.

### 3.4. Lógica del Botón de Reserva

1. **CT030**: **Formulario de Reserva con Todos los Campos Obligatorios Llenos**
   - **Descripción**: Comprobar la lógica del botón de reserva al completar todos los campos obligatorios del formulario de reserva.
   - **Datos de Prueba**: Completar todos los campos obligatorios del formulario de reserva.
   - **Resultado Esperado**: El botón de reserva está habilitado.

2. **CT031**: **Formulario de Reserva con Todos los Campos y Direcciones Completos, Excepto Licencia de Conducir**
   - **Descripción**: Verificar la lógica del botón de reserva cuando se han completado todos los campos y direcciones requeridos, excepto el campo de licencia de conducir.
   - **Datos de Prueba**: Completar todos los campos y direcciones obligatorios excepto el campo de licencia de conducir.
   - **Resultado Esperado**: El botón de reserva está bloqueado.

3. **CT032**: **Formulario de Reserva con Todos los Campos y Direcciones Completos, Excepto Método de Pago**
   - **Descripción**: Verificar la lógica del botón de reserva cuando se han completado todos los campos y direcciones obligatorios, excepto el método de pago.
   - **Datos de Prueba**: Completar todos los campos y direcciones obligatorios excepto el método de pago.
   - **Resultado Esperado**: El botón de reserva está bloqueado.

4. **CT033**: **Formulario de Reserva con Todos los Campos Obligatorios y Direcciones Borradas**
   - **Descripción**: Verificar la lógica del botón de reserva al completar todos los campos obligatorios y borrar las direcciones.
   - **Datos de Prueba**: Completar todos los campos obligatorios y borrar las direcciones.
   - **Resultado Esperado**: El botón de reserva está bloqueado.

5. **CT034**: **Formulario de Reserva con Ningún Campo Obligatorio Completo y Direcciones Borradas**
   - **Descripción**: Verificar la lógica del botón de reserva cuando no se ha completado ninguno de los campos obligatorios y las direcciones se han borrado.
   - **Datos de Prueba**: No completar ningún campo obligatorio y borrar las direcciones.
   - **Resultado Esperado**: El botón de reserva está bloqueado.

### 3.5. Lógica del Campo "Desde" y "Hasta"

1. **CT035**: **Campo "Desde" Lleno**
   - **Descripción**: Verificar la lógica de la reserva al llenar solo el campo "Desde".
   - **Datos de Prueba**: Llenar solo el campo "Desde".
   - **Resultado Esperado**: La lógica de la reserva se comporta correctamente según el sistema.

2. **CT036**: **Campo "Hasta" Lleno**
   - **Descripción**: Verificar la lógica de la reserva al llenar solo el campo "Hasta".
   - **Datos de Prueba**: Llenar solo el campo "Hasta".
   - **Resultado Esperado**: La lógica de la reserva se comporta correctamente según el sistema.

3. **CT037**: **Cancelar el Proceso de Reserva**
   - **Descripción**: Verificar la lógica de la reserva al cancelar el proceso.
   - **Datos de Prueba**: Cancelar el proceso de reserva.
   - **Resultado Esperado**: La reserva se cancela y el sistema regresa al estado anterior.

### 3.6. Integración de Nuevos Modos de Transporte

1. **CT038**: **Nuevo Modo de Transporte en la Interfaz**
   - **Descripción**: Verificar que si se agrega un nuevo modo de transporte en la respuesta del servidor, este aparece en la interfaz.
   - **Datos de Prueba**: Agregar un nuevo modo de transporte en el servidor.
   - **Resultado Esperado**: El nuevo modo de transporte aparece en la interfaz.

2. **CT039**: **Ícono del Nuevo Modo de Transporte**
   - **Descripción**: Verificar que el ícono del nuevo modo de transporte se muestra en la sección de tipo de transporte y la interfaz no cambia.
   - **Datos de Prueba**: Verificar la presencia del ícono del nuevo modo de transporte en la sección correspondiente.
   - **Resultado Esperado**: El ícono se muestra y la interfaz permanece sin cambios.

3. **CT040**: **Ícono Apagado en Modo "Personal"**
   - **Descripción**: Verificar que el ícono del nuevo modo de transporte se apaga cuando cambias el modo de "Personal" a cualquier otro.
   - **Datos de Prueba**: Cambiar el modo de "Personal" a otro.
   - **Resultado Esperado**: El ícono del nuevo modo de transporte se apaga.

4. **CT041**: **Ícono Seleccionado en Modo "Personal"**
   - **Descripción**: Verificar que el ícono del modo de transporte cambia al estado seleccionado al hacer clic en él en el modo "Personal".
   - **Datos de Prueba**: Hacer clic en el ícono del modo de transporte en el modo "Personal".
   - **Resultado Esperado**: El ícono cambia al estado seleccionado.

5. **CT042**: **Cálculo del Costo del Viaje con Nuevo Modo de Transporte**
   - **Descripción**: Verificar que el costo del viaje se calcula si todos los campos se rellenan correctamente y se selecciona un nuevo modo de transporte.
   - **Datos de Prueba**: Completar todos los campos y seleccionar un nuevo modo de transporte.
   - **Resultado Esperado**: El costo del viaje se calcula correctamente.

6. **CT043**: **Resultados del Cálculo con Nuevo Modo de Transporte**
   - **Descripción**: Verificar que los resultados del cálculo muestran el nombre del nuevo modo de transporte que vino del servidor.
   - **Datos de Prueba**: Realizar el cálculo del viaje con un nuevo modo de transporte.
   - **Resultado Esperado**: Los resultados muestran el nombre del nuevo modo de transporte.

7. **CT044**: **Resultados del Cálculo con Costo y Tiempo de Viaje**
   - **Descripción**: Verificar que los resultados del cálculo muestran el costo y el tiempo de viaje en el modo de transporte recién seleccionado.
   - **Datos de Prueba**: Realizar el cálculo del viaje con el nuevo modo de transporte seleccionado.
   - **Resultado Esperado**: Los resultados muestran el costo y el tiempo de viaje en el nuevo modo de transporte.

## 4. Criterios de Aceptación
- Todos los casos de prueba deben pasar con éxito según los resultados esperados.
- El sistema debe comportarse según lo especificado en los resultados esperados para cada caso de prueba.

## 5. Recursos Necesarios
- Acceso al sistema de prueba.
- Datos de prueba válidos y válidos.
- Herramientas de prueba para la validación de resultados.

## 6. Responsable de las Pruebas
- David Elías Ledesma Rivera

## 7. Fecha de Ejecución
- [Fecha a definir]
