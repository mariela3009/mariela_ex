# CASOS Y PROCEDIMIENTOS DE PRUEBA

## MÓDULO PUNTO DE VENTA COMERCIAL

**Versión 1.0**

**Fecha: 09/05/2026**

---

## Información del Documento

| Título del Documento: | Casos y procedimientos de prueba — Sistema Punto de Venta Comercial |
| --- | --- |
| Nombre del Archivo del Documento: | CASOSYPROCEDIMIENTOPRUEBA_POS_V1_0.md |
| Número de Versión | 1.0 |
| Autor: | Mariela Estefany Ramos Loza |
| Fecha de Creación: | 09/05/2026 |
| Estado: | En proceso |

---

## Aprobaciones

| Mariela Estefany Ramos Loza | | | |
| --- | --- | --- | --- |
| **Autor** | | Firma | |
| Percy Taquila Carazas | | | |
| **PM** | | Firma | |
| Alexander Huallpa Huaychani | | | |
| **LT** | | Firma | |

---

## Historia de Cambios

| **Fecha** | **Versión** | **Descripción** | **Autor** |
| --- | --- | --- | --- |
| 09/05/2026 | 1.0 | Versión Inicial | Mariela Estefany Ramos Loza |
| | | | |
| | | | |

---

## Tabla de Contenido

1. NORMA DE SEGURIDAD ISO 27001
2. UC-01 – INICIAR SESIÓN
   - 2.1. CASOS DE PRUEBA
     - a) CP01 – Autenticar usuario en el sistema POS
     - b) CP02 – Cerrar sesión del sistema POS
   - 2.2. PROCEDIMIENTO DE PRUEBA
     - a) PP01 – Inicio de sesión exitoso con credenciales válidas
     - b) PP02 – Inicio de sesión fallido con contraseña y/o usuario incorrecto
     - c) PP03 – Inicio de sesión fallido con campos vacíos
     - d) PP04 – Inicio de sesión fallido con usuario inactivo
     - e) PP05 – Cierre de sesión exitoso
3. UC-02 – GESTIONAR DASHBOARD
   - 3.1. CASOS DE PRUEBA
     - a) CP01 – Visualizar indicadores KPI y gráficos del Dashboard
     - b) CP02 – Configurar widgets del Dashboard por rol
   - 3.2. PROCEDIMIENTO DE PRUEBA
     - a) PP01 – Visualización exitosa del Dashboard con datos del día
     - b) PP02 – Filtrado del gráfico de ventas por período (Hoy, Semana, Mes)
     - c) PP03 – Cambio de vista del widget Distribución de Ventas
     - d) PP04 – Configuración de parámetros del widget Distribución de Ventas
     - e) PP05 – Acceso a módulo completo de Pedidos desde la tabla Últimos Pedidos
     - f) PP06 – Navegación mediante accesos rápidos del Dashboard
     - g) PP07 – Dashboard sin datos en el período actual
     - h) PP08 – Dashboard vacío por falta de configuración de widgets para el rol
     - i) PP09 – Configuración exitosa de widgets por rol
     - j) PP10 – Dashboard con widgets deshabilitados para el rol
4. UC-03 – GESTIONAR PUNTO DE VENTA
   - 4.1. CASOS DE PRUEBA
     - a) CP01 – Registrar venta rápida en el POS
     - b) CP02 – Cancelar venta en proceso en el POS
   - 4.2. PROCEDIMIENTO DE PRUEBA
     - a) PP01 – Registro exitoso de venta con búsqueda por código de barras
     - b) PP02 – Registro exitoso de venta con búsqueda por descripción de artículo
     - c) PP03 – Ajuste de cantidades de ítems en el carrito
     - d) PP04 – Eliminación de ítem del carrito
     - e) PP05 – Intento de cobro sin artículos en el carrito
     - f) PP06 – Registro de cobro con monto recibido menor al total
     - g) PP07 – Registro de cobro sin seleccionar tipo de comprobante
     - h) PP08 – Registro de cobro sin seleccionar forma de pago
     - i) PP09 – Registro exitoso de venta completa (cobro)
     - j) PP10 – Cancelación de venta en proceso
5. UC-04 – GESTIONAR VENTAS
   - 5.1. CASOS DE PRUEBA
     - a) CP01 – Listar y filtrar comprobantes de ventas
     - b) CP02 – Ver detalle de comprobante
     - c) CP03 – Imprimir comprobante
     - d) CP04 – Descargar XML/CDR
     - e) CP05 – Editar documento de venta
     - f) CP06 – Enviar comprobante a SUNAT
     - g) CP07 – Anular documento de venta
   - 5.2. PROCEDIMIENTO DE PRUEBA
     - a) PP01 – Listado de comprobantes con filtros aplicados
     - b) PP02 – Listado sin resultados al aplicar filtros sin coincidencias
     - c) PP03 – Visualización del detalle completo de un comprobante
     - d) PP04 – Impresión de comprobante en vista previa PDF
     - e) PP05 – Descarga de archivo XML/CDR de un comprobante aceptado
     - f) PP06 – Edición exitosa de documento no enviado a SUNAT
     - g) PP07 – Intento de edición de documento ya enviado a SUNAT
     - h) PP08 – Envío exitoso de comprobante a SUNAT (estado Aceptado)
     - i) PP09 – Envío de comprobante a SUNAT con resultado Rechazado
     - j) PP10 – Anulación exitosa de documento en estado Activa
     - k) PP11 – Intento de anulación de documento ya Anulado
6. UC-05 – GESTIONAR PEDIDOS
   - 6.1. CASOS DE PRUEBA
     - a) CP01 – Registrar pedido
     - b) CP02 – Editar pedido
     - c) CP03 – Convertir pedido en venta
     - d) CP04 – Imprimir pedido
     - e) CP05 – Anular pedido
   - 6.2. PROCEDIMIENTO DE PRUEBA
     - a) PP01 – Registro exitoso de nuevo pedido
     - b) PP02 – Registro fallido de pedido con campos obligatorios vacíos
     - c) PP03 – Registro fallido con precio o cantidad no numérica
     - d) PP04 – Edición exitosa de pedido en estado Activo
     - e) PP05 – Intento de edición de pedido en estado Atendido o Anulado
     - f) PP06 – Conversión exitosa de pedido a venta
     - g) PP07 – Impresión de pedido
     - h) PP08 – Anulación exitosa de pedido en estado Activo
     - i) PP09 – Intento de anulación de pedido en estado Atendido o Anulado
     - j) PP10 – Filtrado de pedidos por rango de fechas, cliente y estado
7. UC-06 – GESTIONAR CLIENTES
   - 7.1. CASOS DE PRUEBA
     - a) CP01 – Registrar cliente
     - b) CP02 – Editar cliente
     - c) CP03 – Buscar cliente
   - 7.2. PROCEDIMIENTO DE PRUEBA
     - a) PP01 – Registro exitoso de nuevo cliente con datos válidos
     - b) PP02 – Registro fallido por campos obligatorios vacíos
     - c) PP03 – Registro fallido por número de documento duplicado
     - d) PP04 – Registro fallido por formato inválido de número de documento
     - e) PP05 – Edición exitosa de datos de cliente existente
     - f) PP06 – Edición fallida con campos obligatorios vacíos
     - g) PP07 – Búsqueda exitosa de cliente por nombre, razón social o número de documento
     - h) PP08 – Búsqueda sin resultados
8. UC-07 – GESTIONAR USUARIOS
   - 8.1. CASOS DE PRUEBA
     - a) CP01 – Registrar usuario en el sistema POS
     - b) CP02 – Editar usuario en el sistema POS
     - c) CP03 – Listar usuarios del sistema POS
   - 8.2. PROCEDIMIENTO DE PRUEBA
     - a) PP01 – Registro exitoso de nuevo usuario con datos válidos
     - b) PP02 – Registro fallido por nombre de usuario duplicado
     - c) PP03 – Registro fallido por campos obligatorios vacíos
     - d) PP04 – Edición exitosa de usuario existente
     - e) PP05 – Edición fallida con campos obligatorios vacíos
     - f) PP06 – Verificación de inmutabilidad del nombre de usuario en edición
     - g) PP07 – Listado completo de usuarios registrados
9. UC-08 – GESTIONAR ROLES
   - 9.1. CASOS DE PRUEBA
     - a) CP01 – Registrar rol
     - b) CP02 – Editar rol y permisos
     - c) CP03 – Listar roles
   - 9.2. PROCEDIMIENTO DE PRUEBA
     - a) PP01 – Registro exitoso de nuevo rol con permisos asignados
     - b) PP02 – Registro fallido por nombre de rol duplicado
     - c) PP03 – Registro fallido por campos obligatorios vacíos
     - d) PP04 – Edición exitosa de rol existente y sus permisos
     - e) PP05 – Edición fallida por nombre de rol duplicado
     - f) PP06 – Edición fallida por campos obligatorios vacíos
     - g) PP07 – Listado completo de roles registrados
10. UC-09 – GESTIONAR FORMULARIOS
    - 10.1. CASOS DE PRUEBA
      - a) CP01 – Configurar campos de formularios por módulo y rol
    - 10.2. PROCEDIMIENTO DE PRUEBA
      - a) PP01 – Configuración exitosa de visibilidad de campo de formulario
      - b) PP02 – Configuración exitosa de obligatoriedad de campo de formulario
      - c) PP03 – Configuración exitosa de editabilidad de campo de formulario
      - d) PP04 – Verificación de aplicación inmediata de configuración de formularios
11. UC-10 – GESTIONAR FORMAS DE PAGO
    - 11.1. CASOS DE PRUEBA
      - a) CP01 – Habilitar o deshabilitar formas de pago en el POS
      - b) CP02 – Establecer orden de formas de pago
    - 11.2. PROCEDIMIENTO DE PRUEBA
      - a) PP01 – Habilitación exitosa de una forma de pago en el POS
      - b) PP02 – Deshabilitación exitosa de una forma de pago en el POS
      - c) PP03 – Intento de deshabilitar todas las formas de pago
      - d) PP04 – Establecer orden de presentación de formas de pago
      - e) PP05 – Verificación de que formas de pago deshabilitadas no aparecen en el POS

---

## CASOS DE PRUEBA

A continuación, se procede a describir los casos de prueba asignados al proyecto "Sistema Punto de Venta Comercial — SCOP ERP", junto a sus respectivos procedimientos de prueba. Para todos los casos y procedimientos se considera:

- Los casos de prueba están orientados a la interacción del usuario con las funcionalidades implementadas del Sistema Punto de Venta Comercial, en una plataforma web.

---

### 1. NORMA DE SEGURIDAD ISO 27001

El presente documento trabajará con la norma de Seguridad ISO 27001. Se indicará por cada prueba el control de seguridad que le corresponde. Según el documento ERS redactado, los controles a evaluar son los siguientes:

- Validación de Datos de Entrada
- Validación de Datos de Salida

---

### 2. UC-01 – INICIAR SESIÓN

#### 2.1. CASOS DE PRUEBA

##### a) CP01 – Autenticar usuario en el sistema POS

| **IDENTIFICADOR:** *CP01* | **NOMBRE:** *Autenticar usuario en el sistema POS* |
| --- | --- |
| **Requerimiento vinculado:** *RF-AUTH-001* | **Prioridad de prueba:** *Alta* |
| **Documentos de visualización asociados:** *Documento de Especificación de Requerimientos de Software — Sistema Punto de Venta Comercial.* |
| **Precondición:** *El usuario debe estar registrado y activo en el sistema POS. Debe encontrarse en la pantalla de inicio de sesión del sistema SCOP ERP.* |
| **Descripción:** *El sistema debe permitir que cualquier usuario registrado ingrese sus credenciales (nombre de usuario y contraseña) a través de la pantalla de inicio de sesión del sistema Punto de Venta Comercial. Si las credenciales son válidas, el sistema autentica al usuario y lo redirige automáticamente al Dashboard configurado según su rol y empresa (tenant). Si las credenciales son incorrectas, el sistema muestra un mensaje de error genérico sin revelar cuál de los campos es incorrecto, en cumplimiento de los controles de seguridad ISO 27001. La validación de los campos se realiza en tiempo real con retroalimentación visual inmediata.* |
| **DATOS DE ENTRADA** |
| **CAMPO/DATO** | **TIPO DE DATO** |
| *Usuario (nombre de usuario)* | *Cadena* |
| *Contraseña* | *Cadena* |
| **ESCENARIO DE PRUEBAS** *EP01: Inicio de sesión exitoso con credenciales válidas* *EP02: Inicio de sesión fallido con contraseña y/o usuario incorrecto* *EP03: Inicio de sesión fallido con campos vacíos* *EP04: Inicio de sesión fallido con usuario inactivo* |
| **CRITERIOS DE ACEPTACIÓN** El usuario puede autenticarse exitosamente con su nombre de usuario y contraseña correctos. Al autenticarse, el sistema lo redirige automáticamente al Dashboard configurado según su rol y empresa (tenant). Si el usuario no está registrado o las credenciales son incorrectas, el sistema muestra el mensaje genérico: "Credenciales inválidas. Verifique su usuario y contraseña.", sin especificar cuál de los dos campos es incorrecto. El sistema no permite el envío del formulario si el nombre de usuario o la contraseña están vacíos; el botón "Iniciar sesión" permanece deshabilitado hasta que ambos campos contienen información. El sistema valida en tiempo real el formato del campo Usuario con retroalimentación visual inmediata. El usuario puede hacer clic en el ícono del ojo para mostrar u ocultar la contraseña. Si la sesión expira por inactividad, el sistema cierra la sesión automáticamente y redirige al usuario a la pantalla de inicio de sesión con un mensaje informativo. Si el usuario se encuentra deshabilitado en el sistema, el servidor rechaza la autenticación y el sistema muestra el mensaje de error genérico correspondiente. |

##### b) CP02 – Cerrar sesión del sistema POS

| **IDENTIFICADOR:** *CP02* | **NOMBRE:** *Cerrar sesión del sistema POS* |
| --- | --- |
| **Requerimiento vinculado:** *RF-AUTH-001* | **Prioridad de prueba:** *Media* |
| **Documentos de visualización asociados:** *Documento de Especificación de Requerimientos de Software — Sistema Punto de Venta Comercial.* |
| **Precondición:** *El usuario debe estar autenticado y con una sesión activa en el sistema POS.* |
| **Descripción:** *El sistema debe permitir al usuario cerrar su sesión activa de forma explícita haciendo clic en el ícono de salida ubicado en la parte inferior del menú lateral, junto a su nombre de usuario. Al cerrar sesión, el sistema invalida la sesión activa, destruye el token de sesión y redirige al usuario a la pantalla de inicio de sesión. El sistema también gestiona el cierre automático de sesión por inactividad, con un contador de tiempo restante visible junto al nombre del usuario.* |
| **DATOS DE ENTRADA** |
| **CAMPO/DATO** | **TIPO DE DATO** |
| *Ícono de salida (flecha →)* | *Acción de usuario* |
| **ESCENARIO DE PRUEBAS** *EP01: Cierre de sesión exitoso mediante el ícono de salida* |
| **CRITERIOS DE ACEPTACIÓN** El usuario puede cerrar sesión exitosamente haciendo clic en el ícono de salida (flecha →) ubicado junto a su nombre en la parte inferior del menú lateral. El sistema cierra la sesión activa y redirige al usuario a la pantalla de inicio de sesión. La sesión es destruida correctamente, evitando el acceso por el navegador a páginas protegidas. El sistema muestra en todo momento el contador "Sesión expira en" con el tiempo restante de inactividad. |

---

#### 2.2. PROCEDIMIENTO DE PRUEBA

##### a) PP01 – Inicio de sesión exitoso con credenciales válidas

| **IDENTIFICADOR:** | *PP01* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP01 – Autenticar usuario en el sistema POS* | **NOMBRE:** *Inicio de sesión exitoso con credenciales válidas* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el sistema permita a un usuario autenticarse correctamente utilizando credenciales válidas (nombre de usuario y contraseña). El flujo incluye la verificación en tiempo real del formato de los campos, la habilitación del botón "Iniciar sesión" y la posterior redirección del usuario al Dashboard principal configurado según su rol y empresa (tenant).* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario abre un navegador web moderno (Chrome, Firefox o Edge) e ingresa la URL del sistema proporcionada por el administrador.* | *El sistema presenta la pantalla de bienvenida del sistema SCOP ERP con el formulario de inicio de sesión, compuesto por los campos: Usuario y Contraseña.* |
| *El usuario ingresa su nombre de usuario en el campo "Usuario" (ej: Administrador@dcp.pe).* | *El sistema valida en tiempo real el formato del campo, mostrando retroalimentación visual inmediata.* |
| *El usuario ingresa su contraseña en el campo "Contraseña" (ej: admin123). Puede hacer clic en el ícono del ojo para mostrar u ocultar la contraseña.* | *El sistema valida que el campo no esté vacío y habilita el botón "Iniciar sesión" una vez que ambos campos contienen información.* |
| *El usuario hace clic en el botón "Iniciar sesión".* | *El sistema envía las credenciales al servidor para su validación. Si las credenciales son válidas, el sistema redirige automáticamente al usuario al Dashboard principal configurado según su rol y empresa (tenant). La interfaz se adapta mostrando únicamente los módulos y opciones para los que el usuario tiene permisos asignados.* |

##### b) PP02 – Inicio de sesión fallido con contraseña y/o usuario incorrecto

| **IDENTIFICADOR:** | *PP02* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP01 – Autenticar usuario en el sistema POS* | **NOMBRE:** *Inicio de sesión fallido con contraseña y/o usuario incorrecto* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el sistema gestione correctamente los casos en los que un usuario intenta iniciar sesión con credenciales incorrectas, ya sea un nombre de usuario no registrado o una contraseña errónea. En cumplimiento con los controles de seguridad ISO 27001, el sistema debe mostrar un mensaje de error genérico sin revelar cuál de los dos campos es incorrecto, y mantener al usuario en la pantalla de inicio de sesión.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario ingresa la URL del sistema en el navegador.* | *Le cargará la pantalla de inicio de sesión con los campos de texto Usuario y Contraseña.* |
| *El usuario ingresa un nombre de usuario no registrado o incorrecto en el campo "Usuario".* | *El sistema valida el formato del campo en tiempo real.* |
| *El usuario ingresa una contraseña incorrecta en el campo "Contraseña".* | |
| *El usuario hace clic en el botón "Iniciar sesión".* | *El sistema no redirigirá a ninguna otra vista. La pantalla se mantendrá en el formulario de inicio de sesión y deberá mostrar el mensaje genérico: "Credenciales inválidas. Verifique su usuario y contraseña.", sin especificar cuál de los dos campos es incorrecto.* |

##### c) PP03 – Inicio de sesión fallido con campos vacíos

| **IDENTIFICADOR:** | *PP03* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP01 – Autenticar usuario en el sistema POS* | **NOMBRE:** *Inicio de sesión fallido con campos vacíos* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida el comportamiento del sistema cuando el usuario intenta iniciar sesión dejando los campos de Usuario y/o Contraseña vacíos. El sistema debe mostrar validación visual en tiempo real e impedir la habilitación del botón "Iniciar sesión" hasta que ambos campos contengan información.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario ingresa la URL del sistema en el navegador.* | *Le cargará la pantalla de inicio de sesión con los campos de texto Usuario y Contraseña.* |
| *El usuario no ingresa ningún valor en el campo "Usuario".* | |
| *El usuario tampoco ingresa ningún valor en el campo "Contraseña".* | |
| *El usuario intenta hacer clic en el botón "Iniciar sesión".* | *El sistema mostrará validación visual en tiempo real indicando que los campos son obligatorios. El botón "Iniciar sesión" permanece deshabilitado y el sistema no envía ninguna solicitud al servidor.* |

##### d) PP04 – Inicio de sesión fallido con usuario inactivo

| **IDENTIFICADOR:** | *PP04* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP01 – Autenticar usuario en el sistema POS* | **NOMBRE:** *Inicio de sesión fallido con usuario inactivo* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el sistema maneje correctamente el intento de inicio de sesión cuando un usuario deshabilitado ingresa sus credenciales. El sistema debe rechazar la autenticación y mostrar el mensaje de error genérico correspondiente, sin revelar el motivo específico del rechazo.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario deshabilitado ingresa la URL del sistema en el navegador.* | *Le cargará la pantalla de inicio de sesión con los campos de texto Usuario y Contraseña.* |
| *El usuario ingresa su nombre de usuario en el campo "Usuario".* | *El sistema valida el formato del campo en tiempo real.* |
| *El usuario ingresa su contraseña en el campo "Contraseña".* | *El sistema valida que el campo no esté vacío y habilita el botón "Iniciar sesión".* |
| *El usuario hace clic en el botón "Iniciar sesión".* | *El servidor rechaza la autenticación debido a que el usuario se encuentra deshabilitado en el sistema. El sistema mostrará el mensaje de error genérico: "Credenciales inválidas. Verifique su usuario y contraseña.", sin indicar explícitamente que el usuario está deshabilitado.* |

##### e) PP05 – Cierre de sesión exitoso

| **IDENTIFICADOR:** | *PP05* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP02 – Cerrar sesión del sistema POS* | **NOMBRE:** *Cierre de sesión exitoso* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el sistema permita al usuario cerrar su sesión activa de forma correcta mediante el ícono de salida ubicado en la parte inferior del menú lateral. El flujo incluye la identificación del elemento de cierre de sesión, la ejecución de la acción y la verificación de que la sesión queda destruida correctamente, redirigiendo al usuario a la pantalla de inicio de sesión.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario se encuentra autenticado en el sistema con una sesión activa. Localiza su nombre de usuario en la parte inferior del menú lateral izquierdo.* | *El sistema muestra el indicador de sesión activa con el contador "Sesión expira en" y el tiempo restante visible junto al nombre del usuario.* |
| *El usuario hace clic en el ícono de salida (flecha →) ubicado junto a su nombre.* | *El sistema cierra la sesión activa, destruye el token de sesión y redirige al usuario a la pantalla de inicio de sesión. Si el usuario intenta navegar a una página protegida mediante el historial del navegador, el sistema no permitirá el acceso y lo redirigirá a la pantalla de inicio de sesión.* |

---

### 3. UC-02 – GESTIONAR DASHBOARD

#### 3.1. CASOS DE PRUEBA

##### a) CP01 – Visualizar indicadores KPI y gráficos del Dashboard

| **IDENTIFICADOR:** *CP01* | **NOMBRE:** *Visualizar indicadores KPI y gráficos del Dashboard* |
| --- | --- |
| **Requerimiento vinculado:** *RF-DASH-002* | **Prioridad de prueba:** *Alta* |
| **Documentos de visualización asociados:** *Documento de Especificación de Requerimientos de Software — Sistema Punto de Venta Comercial. UC-DASH-02 — Gestionar Dashboard.* |
| **Precondición:** *El usuario debe estar autenticado con credenciales válidas en el sistema. El usuario debe tener permisos asignados para visualizar el Dashboard, conforme a la configuración RBAC de su rol. El Administrador debe haber configurado los widgets visibles para el rol del usuario en Administración > Dashboard > Widgets.* |
| **Descripción:** *El sistema debe presentar al usuario autenticado el Dashboard como panel central de control, mostrando automáticamente al ingresar los componentes configurados para su rol y tenant. El Dashboard debe presentar: cuatro tarjetas de indicadores KPI actualizadas automáticamente (Ventas Hoy, Pedidos Hoy, Clientes Atendidos y Prod. Vendidos), un gráfico de barras de evolución de ventas y pedidos filtrable por período (Hoy, Semana o Mes), un widget de distribución de ventas por tipo de comprobante con vistas intercambiables (Barras, Dona y Líneas) y opción de configuración, una tabla de últimos pedidos con enlace al módulo completo de Pedidos, y cuatro botones de acceso rápido a las operaciones más frecuentes del sistema.* |
| **DATOS DE ENTRADA** |
| **CAMPO/DATO** | **TIPO DE DATO** |
| *Credenciales de usuario autenticado* | *Cadena* |
| *Filtro de período del gráfico (Hoy, Semana, Mes)* | *Cadena (selección)* |
| *Vista del widget Distribución de Ventas (Barras, Dona, Líneas)* | *Cadena (selección)* |
| *Rango de fechas del modal "Configurar widget"* | *Cadena (selección)* |
| *Opción "Mostrar Comparativa" (Sí / No)* | *Booleano* |
| **ESCENARIO DE PRUEBAS** *EP01: Visualización exitosa del Dashboard con datos del día* *EP02: Filtrado del gráfico de ventas por período (Hoy, Semana, Mes)* *EP03: Cambio de vista del widget Distribución de Ventas* *EP04: Configuración de parámetros del widget Distribución de Ventas* *EP05: Acceso a módulo completo de Pedidos desde la tabla Últimos Pedidos* *EP06: Navegación mediante accesos rápidos del Dashboard* *EP07: Dashboard sin datos en el período actual* *EP08: Dashboard vacío por falta de configuración de widgets para el rol* |
| **CRITERIOS DE ACEPTACIÓN** El sistema redirige automáticamente al usuario al Dashboard al iniciar sesión y también permite acceder a él desde el menú lateral. El Dashboard presenta las cuatro tarjetas KPI (Ventas Hoy en S/, Pedidos Hoy, Clientes Atendidos y Prod. Vendidos) actualizadas con la información del día en curso. Si no existen datos para el período actual, los indicadores KPI muestran S/0.00 o cero según corresponda, y los gráficos se presentan vacíos sin información. El gráfico central muestra barras azules para Ventas y barras oscuras para Pedidos. Al pasar el cursor sobre cualquier barra, se muestra el valor exacto en soles. Al seleccionar Hoy, el sistema agrupa las ventas por hora del día actual; al seleccionar Semana, muestra el total por día de la semana en curso; al seleccionar Mes, muestra el total por día del mes en curso. El widget "Distribución de Ventas" muestra el desglose por tipo de comprobante (Facturas, Boletas, Notas de Crédito y Notas de Débito) con montos y porcentajes de participación. Al cambiar entre Barras, Dona y Líneas, el sistema modifica la representación visual manteniendo los datos inalterados. El modal "Configurar widget" permite seleccionar rango de fechas (Hoy, Semana, Mes o Personalizado) y activar o desactivar "Mostrar Comparativa". Al hacer clic en "Guardar", el sistema aplica los cambios y actualiza el gráfico. La tabla de últimos pedidos muestra los campos: NRO DOC, CLIENTE, ESTADO, TOTAL y FECHA. El enlace "Ver todos los pedidos →" redirige al módulo de Pedidos. Los cuatro accesos rápidos (Nuevo Pedido, Ver Ventas, Ver Clientes y Artículos) redirigen correctamente al módulo o funcionalidad correspondiente. Si el Administrador no ha configurado widgets visibles para el rol del usuario, el Dashboard se presenta vacío o con los widgets disponibles por defecto. Los widgets no habilitados para el rol del usuario no se renderizan en la interfaz, sin mostrar mensajes de error al respecto. |

##### b) CP02 – Configurar widgets del Dashboard por rol

| **IDENTIFICADOR:** *CP02* | **NOMBRE:** *Configurar widgets del Dashboard por rol* |
| --- | --- |
| **Requerimiento vinculado:** *RF-SADM-011* | **Prioridad de prueba:** *Alta* |
| **Documentos de visualización asociados:** *Documento de Especificación de Requerimientos de Software — Sistema Punto de Venta Comercial. UC-DASH-02 — Gestionar Dashboard.* |
| **Precondición:** *El Administrador debe estar autenticado con credenciales válidas. El Administrador debe contar con el rol de Administrador para acceder a la sección de configuración de widgets en Administración > Dashboard > Widgets.* |
| **Descripción:** *El sistema debe permitir al Administrador configurar, desde el módulo de Administración, qué widgets del Dashboard son visibles para cada rol de usuario. La configuración es granular por widget y por rol, e incluye: KPI (Ventas Hoy, Pedidos Hoy, Clientes Atendidos, Productos Vendidos), Gráfico de Ventas y Pedidos, Distribución de Ventas por tipo de comprobante, Tabla de Últimos Pedidos y Accesos Rápidos. Los cambios se aplican de forma inmediata a todos los usuarios del rol configurado, sin necesidad de que cierren y vuelvan a iniciar sesión.* |
| **DATOS DE ENTRADA** |
| **CAMPO/DATO** | **TIPO DE DATO** |
| *Rol de usuario a configurar* | *Cadena (selección)* |
| *Estado de visibilidad por widget (activado / desactivado)* | *Booleano* |
| **ESCENARIO DE PRUEBAS** *EP01: Configuración exitosa de widgets por rol* *EP02: Dashboard con widgets deshabilitados para el rol* |
| **CRITERIOS DE ACEPTACIÓN** El Administrador puede acceder a Administración > Dashboard > Widgets y seleccionar el rol a configurar. El sistema carga la lista de widgets disponibles con su estado de visibilidad actual para el rol seleccionado. El Administrador puede activar o desactivar la visibilidad de cada widget de forma individual. Al hacer clic en "Guardar", los cambios se aplican de forma inmediata sin necesidad de que los usuarios afectados cierren y vuelvan a iniciar sesión. Los usuarios del rol configurado visualizarán en el Dashboard únicamente los widgets habilitados para su rol. Si no se habilita ningún widget para un rol, el Dashboard de los usuarios con ese rol se presentará vacío, sin mostrar mensajes de error. |

---

#### 3.2. PROCEDIMIENTO DE PRUEBA

##### a) PP01 – Visualización exitosa del Dashboard con datos del día

| **IDENTIFICADOR:** | *PP01* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP01 – Visualizar indicadores KPI y gráficos del Dashboard* | **NOMBRE:** *Visualización exitosa del Dashboard con datos del día* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el sistema presente correctamente el Dashboard al usuario autenticado, mostrando los cuatro indicadores KPI con datos reales del día en curso, el gráfico de evolución de ventas y pedidos, el widget de distribución de ventas, la tabla de últimos pedidos y los accesos rápidos, todos configurados para el rol y tenant del usuario.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario ingresa al sistema con credenciales válidas o hace clic en la opción "Dashboard" del menú lateral izquierdo.* | *El sistema carga automáticamente el panel del Dashboard mostrando los componentes configurados para el rol y tenant del usuario autenticado.* |
| *El usuario visualiza el panel superior del Dashboard.* | *El sistema presenta las cuatro tarjetas KPI con la información del día en curso: (1) Ventas Hoy (S/) — monto total en soles; (2) Pedidos Hoy — cantidad de pedidos del día; (3) Clientes Atendidos — clientes únicos con transacciones; (4) Prod. Vendidos — unidades vendidas. Estos indicadores se actualizan automáticamente.* |
| *El usuario visualiza el gráfico central de evolución de ventas y pedidos.* | *El sistema presenta el gráfico con barras azules para Ventas y barras oscuras para Pedidos. El usuario pasa el cursor sobre una barra y el sistema muestra el valor exacto en soles.* |
| *El usuario visualiza el widget "Distribución de Ventas".* | *El sistema muestra el desglose del total de ventas por tipo de comprobante (Facturas, Boletas, Notas de Crédito y Notas de Débito) con sus montos y porcentajes de participación.* |
| *El usuario visualiza la tabla de "Últimos Pedidos".* | *El sistema presenta los pedidos más recientes con los campos: NRO DOC, CLIENTE, ESTADO, TOTAL y FECHA.* |
| *El usuario visualiza los accesos rápidos en la parte inferior derecha.* | *El sistema presenta los cuatro botones de acceso directo: Nuevo Pedido, Ver Ventas, Ver Clientes y Artículos.* |

##### b) PP02 – Filtrado del gráfico de ventas por período (Hoy, Semana, Mes)

| **IDENTIFICADOR:** | *PP02* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP01 – Visualizar indicadores KPI y gráficos del Dashboard* | **NOMBRE:** *Filtrado del gráfico de ventas por período (Hoy, Semana, Mes)* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el sistema actualice correctamente el gráfico de evolución de ventas y pedidos al seleccionar cada uno de los filtros de período disponibles: Hoy, Semana y Mes. Cada selección debe cambiar la agrupación de los datos manteniendo la estructura visual del gráfico.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario se encuentra en el Dashboard con el gráfico de evolución de ventas visible.* | *El sistema presenta el gráfico con la vista por defecto.* |
| *El usuario hace clic en el botón "Hoy" del filtro de período del gráfico.* | *El sistema actualiza el gráfico agrupando las ventas por hora del día actual.* |
| *El usuario hace clic en el botón "Semana" del filtro de período del gráfico.* | *El sistema actualiza el gráfico mostrando el total de ventas por día de la semana en curso.* |
| *El usuario hace clic en el botón "Mes" del filtro de período del gráfico.* | *El sistema actualiza el gráfico mostrando el total de ventas por día del mes en curso.* |

##### c) PP03 – Cambio de vista del widget Distribución de Ventas

| **IDENTIFICADOR:** | *PP03* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP01 – Visualizar indicadores KPI y gráficos del Dashboard* | **NOMBRE:** *Cambio de vista del widget Distribución de Ventas* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el sistema cambie correctamente la representación visual del widget "Distribución de Ventas" al seleccionar cada uno de los modos de vista disponibles: Barras, Dona y Líneas, manteniendo los datos inalterados en cada cambio de vista.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario se encuentra en el Dashboard con el widget "Distribución de Ventas" visible.* | *El sistema presenta el widget con la vista por defecto (Barras).* |
| *El usuario hace clic en el botón "Barras" del widget.* | *El sistema muestra la distribución de ventas en formato de gráfico de barras, manteniendo los datos (Facturas, Boletas, Notas de Crédito y Notas de Débito con sus montos y porcentajes) inalterados.* |
| *El usuario hace clic en el botón "Dona" del widget.* | *El sistema cambia la representación visual al formato de gráfico de dona, manteniendo los mismos datos inalterados.* |
| *El usuario hace clic en el botón "Líneas" del widget.* | *El sistema cambia la representación visual al formato de gráfico de líneas, manteniendo los mismos datos inalterados.* |

##### d) PP04 – Configuración de parámetros del widget Distribución de Ventas

| **IDENTIFICADOR:** | *PP04* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP01 – Visualizar indicadores KPI y gráficos del Dashboard* | **NOMBRE:** *Configuración de parámetros del widget Distribución de Ventas* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el sistema permita al usuario configurar los parámetros del widget "Distribución de Ventas" mediante el modal "Configurar widget", donde puede seleccionar el rango de fechas y activar o desactivar la opción "Mostrar Comparativa". Al guardar, el sistema debe aplicar los cambios y actualizar el gráfico del widget según los nuevos parámetros.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario se encuentra en el Dashboard con el widget "Distribución de Ventas" visible.* | *El sistema presenta el widget con la configuración actual.* |
| *El usuario hace clic en el botón "Config" ubicado en la esquina superior derecha del widget de distribución.* | *El sistema muestra el modal "Configurar widget" con las opciones de: Rango de Fechas (Hoy, Semana, Mes o Personalizado) y la opción "Mostrar Comparativa" (Sí / No).* |
| *El usuario selecciona el rango de fechas "Mes" en el modal.* | *El sistema registra la selección del rango de fechas.* |
| *El usuario activa la opción "Mostrar Comparativa".* | *El sistema registra la selección de la comparativa.* |
| *El usuario hace clic en "Guardar".* | *El sistema aplica los cambios y actualiza el gráfico del widget según los nuevos parámetros configurados.* |

##### e) PP05 – Acceso a módulo completo de Pedidos desde la tabla Últimos Pedidos

| **IDENTIFICADOR:** | *PP05* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP01 – Visualizar indicadores KPI y gráficos del Dashboard* | **NOMBRE:** *Acceso a módulo completo de Pedidos desde la tabla Últimos Pedidos* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el enlace "Ver todos los pedidos →" presente en la tabla de Últimos Pedidos del Dashboard redirija correctamente al usuario al módulo de Pedidos completo del sistema.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario se encuentra en el Dashboard visualizando la tabla de "Últimos Pedidos" en la parte inferior izquierda.* | *El sistema presenta la tabla con los pedidos más recientes con los campos: NRO DOC, CLIENTE, ESTADO, TOTAL y FECHA.* |
| *El usuario hace clic en el enlace "Ver todos los pedidos →".* | *El sistema redirige al usuario al módulo de Pedidos completo con el listado de todos los pedidos registrados en el sistema.* |

##### f) PP06 – Navegación mediante accesos rápidos del Dashboard

| **IDENTIFICADOR:** | *PP06* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP01 – Visualizar indicadores KPI y gráficos del Dashboard* | **NOMBRE:** *Navegación mediante accesos rápidos del Dashboard* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que cada uno de los cuatro botones de acceso rápido disponibles en el Dashboard redirija correctamente al módulo o funcionalidad correspondiente del sistema.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario se encuentra en el Dashboard visualizando los accesos rápidos en la parte inferior derecha.* | *El sistema presenta cuatro botones de acceso directo: Nuevo Pedido, Ver Ventas, Ver Clientes y Artículos.* |
| *El usuario hace clic en el botón "Nuevo Pedido".* | *El sistema abre el formulario de creación de un nuevo pedido.* |
| *El usuario regresa al Dashboard y hace clic en el botón "Ver Ventas".* | *El sistema navega directamente al listado de ventas registradas.* |
| *El usuario regresa al Dashboard y hace clic en el botón "Ver Clientes".* | *El sistema accede al maestro de clientes del sistema.* |
| *El usuario regresa al Dashboard y hace clic en el botón "Artículos".* | *El sistema navega al catálogo de artículos disponibles.* |

##### g) PP07 – Dashboard sin datos en el período actual

| **IDENTIFICADOR:** | *PP07* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP01 – Visualizar indicadores KPI y gráficos del Dashboard* | **NOMBRE:** *Dashboard sin datos en el período actual* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida el comportamiento del Dashboard cuando no existen datos registrados para el período actual. El sistema debe presentar los indicadores KPI en S/0.00 o cero según corresponda, y los gráficos deben presentarse vacíos sin información, sin generar mensajes de error.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario autenticado accede al Dashboard en un día en el que no se han registrado ventas ni pedidos.* | *El sistema carga el Dashboard sin generar errores. Las cuatro tarjetas KPI muestran: Ventas Hoy con S/0.00, Pedidos Hoy con 0, Clientes Atendidos con 0 y Prod. Vendidos con 0. El gráfico de evolución de ventas y pedidos se presenta vacío sin información. El widget "Distribución de Ventas" se presenta vacío sin datos. La tabla de "Últimos Pedidos" se presenta sin registros.* |

##### h) PP08 – Dashboard vacío por falta de configuración de widgets para el rol

| **IDENTIFICADOR:** | *PP08* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP01 – Visualizar indicadores KPI y gráficos del Dashboard* | **NOMBRE:** *Dashboard vacío por falta de configuración de widgets para el rol* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida el comportamiento del sistema cuando el Administrador no ha configurado ningún widget visible para el rol del usuario autenticado. El Dashboard debe presentarse vacío sin mostrar mensajes de error.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El Administrador previamente ha deshabilitado todos los widgets para el rol del usuario de prueba en Administración > Dashboard > Widgets.* | |
| *El usuario con el rol configurado sin widgets habilitados accede al Dashboard.* | *El sistema carga el Dashboard sin generar errores. Ningún widget se renderiza en la interfaz. El Dashboard se presenta vacío sin mostrar mensajes de error al respecto.* |

##### i) PP09 – Configuración exitosa de widgets por rol

| **IDENTIFICADOR:** | *PP09* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP02 – Configurar widgets del Dashboard por rol* | **NOMBRE:** *Configuración exitosa de widgets por rol* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el Administrador pueda configurar correctamente la visibilidad de los widgets del Dashboard para un rol específico, y que dichos cambios se apliquen de forma inmediata a los usuarios de ese rol sin necesidad de que cierren y vuelvan a iniciar sesión.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El Administrador accede a la sección Administración > Dashboard > Widgets.* | *El sistema presenta la interfaz de configuración de widgets del Dashboard, permitiendo seleccionar el rol de usuario a configurar.* |
| *El Administrador selecciona el rol a configurar.* | *El sistema carga la lista de widgets disponibles en el Dashboard con su estado de visibilidad actual para el rol seleccionado: KPI (Ventas Hoy, Pedidos Hoy, Clientes Atendidos, Productos Vendidos), Gráfico de Ventas y Pedidos, Distribución de Ventas por tipo de comprobante, Tabla de Últimos Pedidos y Accesos Rápidos.* |
| *El Administrador activa o desactiva la visibilidad de cada widget para el rol seleccionado.* | *El sistema registra las configuraciones seleccionadas.* |
| *El Administrador hace clic en "Guardar".* | *El sistema aplica la configuración de visibilidad de widgets de forma inmediata. Desde ese momento, los usuarios con el rol configurado visualizarán en el Dashboard únicamente los widgets habilitados para su rol, sin necesidad de que cierren y vuelvan a iniciar sesión.* |

##### j) PP10 – Dashboard con widgets deshabilitados para el rol

| **IDENTIFICADOR:** | *PP10* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP02 – Configurar widgets del Dashboard por rol* | **NOMBRE:** *Dashboard con widgets deshabilitados para el rol* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que los widgets deshabilitados para un rol específico no se rendericen en el Dashboard de los usuarios con ese rol, sin mostrar mensajes de error al respecto.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El Administrador ha deshabilitado el widget "Tabla de Últimos Pedidos" para el rol de Cajero en Administración > Dashboard > Widgets, y ha hecho clic en "Guardar".* | *El sistema aplica la configuración de forma inmediata.* |
| *Un usuario con rol de Cajero accede al Dashboard.* | *El sistema carga el Dashboard sin mostrar el widget "Tabla de Últimos Pedidos". Los demás widgets habilitados para el rol de Cajero se muestran correctamente. No se muestra ningún mensaje de error al respecto.* |

---

### 4. UC-03 – GESTIONAR PUNTO DE VENTA

#### 4.1. CASOS DE PRUEBA

##### a) CP01 – Registrar venta rápida en el POS

| **IDENTIFICADOR:** *CP01* | **NOMBRE:** *Registrar venta rápida en el POS* |
| --- | --- |
| **Requerimiento vinculado:** *RF-POS-003* | **Prioridad de prueba:** *Alta* |
| **Documentos de visualización asociados:** *Documento de Especificación de Requerimientos de Software — Sistema Punto de Venta Comercial.* |
| **Precondición:** *El usuario debe estar autenticado con credenciales válidas y tener el rol de Cajero o Administrador. El usuario debe contar con permisos de acceso al módulo Punto de Venta, conforme a la configuración RBAC de su rol. Deben existir artículos registrados y disponibles en el catálogo del sistema. Las formas de pago habilitadas deben haber sido configuradas previamente por el Administrador en RF-SADM-010.* |
| **Descripción:** *El sistema debe permitir al Cajero o Administrador registrar ventas de forma rápida desde el módulo Punto de Venta (POS). El flujo incluye la búsqueda de artículos por código de barras o descripción, la gestión del carrito (agregar, ajustar cantidades y eliminar ítems), el cálculo automático en tiempo real de base afecta, IGV (18%) y total a pagar, y el registro del cobro mediante la selección del tipo de comprobante, la forma de pago habilitada y el ingreso del monto recibido. El sistema registra la venta, emite el comprobante electrónico con series y correlativos automáticos, actualiza el estado SUNAT a "No enviado" y limpia el carrito para la siguiente transacción.* |
| **DATOS DE ENTRADA** |
| **CAMPO/DATO** | **TIPO DE DATO** |
| *Código de barras del artículo* | *Cadena / Numérico* |
| *Descripción del artículo (búsqueda parcial o completa)* | *Cadena* |
| *Cantidad de ítems (botones + y −)* | *Numérico* |
| *Tipo de Comprobante (Boleta de Venta Electrónica, Factura Electrónica, Nota de Crédito, Nota de Débito)* | *Cadena (selección)* |
| *Forma de Pago (según las habilitadas por el Administrador)* | *Cadena (selección)* |
| *Monto recibido* | *Numérico* |
| **ESCENARIO DE PRUEBAS** *EP01: Registro exitoso de venta con búsqueda por código de barras* *EP02: Registro exitoso de venta con búsqueda por descripción de artículo* *EP03: Ajuste de cantidades de ítems en el carrito* *EP04: Eliminación de ítem del carrito* *EP05: Intento de cobro sin artículos en el carrito* *EP06: Registro de cobro con monto recibido menor al total* *EP07: Registro de cobro sin seleccionar tipo de comprobante* *EP08: Registro de cobro sin seleccionar forma de pago* *EP09: Registro exitoso de venta completa (cobro)* |
| **CRITERIOS DE ACEPTACIÓN** El sistema presenta la interfaz del POS dividida en dos paneles: el panel izquierdo con el catálogo de artículos (campo de código de barras, campo de descripción, cuadrícula de artículos y paginación) y el panel derecho con el carrito de compras. Al ingresar un código de barras por escaneo o digitación, el sistema localiza el artículo y lo agrega automáticamente al carrito con cantidad 1. Al ingresar una descripción parcial o completa, el sistema filtra y muestra en la cuadrícula los artículos coincidentes con imagen, nombre, código y precio unitario, y permite navegar entre páginas. Al hacer clic sobre la tarjeta de un artículo en la cuadrícula, el sistema lo agrega al carrito con cantidad 1. Si ya existe, incrementa su cantidad en uno. Los botones + y − permiten ajustar las cantidades; el sistema recalcula automáticamente el subtotal, la base afecta, el IGV (18%) y el total a pagar. El botón ✕ elimina el ítem del carrito y el sistema recalcula automáticamente el resumen. Cada ítem muestra su tipo de afectación (IGV, Exon. o Inaf.). Todos los cálculos se ejecutan en el Front-End. Si el carrito está vacío, el botón "Cobrar" no está habilitado. Al hacer clic en "Cobrar", el sistema abre el formulario "Cobrar venta" con el resumen de importes (Base afecta, IGV 18% y Total a Pagar). El sistema asigna automáticamente la Serie (B001 para Boletas, F001 para Facturas) y el Correlativo secuencial. Solo se muestran las formas de pago habilitadas por el Administrador. Si el monto recibido es menor al Total a Pagar, el sistema muestra una advertencia y no permite continuar. Si no se selecciona Tipo de Comprobante o Forma de Pago, los campos obligatorios se marcan visualmente y el sistema no permite guardar la venta. Al guardar exitosamente, el sistema muestra la notificación "Venta registrada correctamente", limpia el carrito, registra el documento en Ventas con estado "Activa" y SUNAT "No enviado", y actualiza el stock de artículos vendidos. |

##### b) CP02 – Cancelar venta en proceso en el POS

| **IDENTIFICADOR:** *CP02* | **NOMBRE:** *Cancelar venta en proceso en el POS* |
| --- | --- |
| **Requerimiento vinculado:** *RF-POS-003* | **Prioridad de prueba:** *Media* |
| **Documentos de visualización asociados:** *Documento de Especificación de Requerimientos de Software — Sistema Punto de Venta Comercial.* |
| **Precondición:** *El usuario debe estar autenticado en el módulo Punto de Venta y debe tener al menos un ítem en el carrito.* |
| **Descripción:** *El sistema debe permitir al usuario cancelar la venta en proceso haciendo clic en el botón "Cancelar" del panel del carrito. Al cancelar, el sistema limpia todo el carrito sin generar ningún registro ni comprobante, dejando el módulo POS disponible para iniciar una nueva transacción.* |
| **DATOS DE ENTRADA** |
| **CAMPO/DATO** | **TIPO DE DATO** |
| *Botón "Cancelar"* | *Acción de usuario* |
| **ESCENARIO DE PRUEBAS** *EP01: Cancelación de venta en proceso* |
| **CRITERIOS DE ACEPTACIÓN** Al hacer clic en "Cancelar", el sistema limpia todo el carrito sin generar ningún registro ni comprobante. El módulo POS queda disponible para iniciar una nueva transacción inmediatamente después de la cancelación. |

---

#### 4.2. PROCEDIMIENTO DE PRUEBA

##### a) PP01 – Registro exitoso de venta con búsqueda por código de barras

| **IDENTIFICADOR:** | *PP01* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP01 – Registrar venta rápida en el POS* | **NOMBRE:** *Registro exitoso de venta con búsqueda por código de barras* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el sistema permita agregar artículos al carrito del POS mediante la búsqueda por código de barras, ya sea por escaneo o por digitación manual del código.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario hace clic en "Punto de Venta" en el menú lateral izquierdo.* | *El sistema presenta la interfaz del POS con el panel izquierdo (catálogo) y el panel derecho (carrito).* |
| *El usuario ingresa el código de barras del artículo en el campo correspondiente (mediante escaneo o digitación).* | *El sistema localiza el artículo correspondiente y lo agrega automáticamente al carrito con cantidad 1. El sistema actualiza en tiempo real la base afecta, el IGV (18%) y el total a pagar.* |

##### b) PP02 – Registro exitoso de venta con búsqueda por descripción de artículo

| **IDENTIFICADOR:** | *PP02* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP01 – Registrar venta rápida en el POS* | **NOMBRE:** *Registro exitoso de venta con búsqueda por descripción de artículo* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el sistema filtre y muestre los artículos coincidentes en la cuadrícula del POS al ingresar una descripción parcial o completa en el campo de búsqueda por descripción, y que al hacer clic sobre la tarjeta de un artículo este sea agregado correctamente al carrito.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario hace clic en "Punto de Venta" en el menú lateral izquierdo.* | *El sistema presenta la interfaz del POS con el panel izquierdo (catálogo) y el panel derecho (carrito).* |
| *El usuario ingresa una descripción parcial o completa en el campo de descripción del panel izquierdo.* | *El sistema filtra y muestra en la cuadrícula los artículos que coinciden con la búsqueda, presentando imagen, nombre, código y precio unitario. El usuario puede navegar entre páginas mediante el control de paginación (ej: 1/49).* |
| *El usuario hace clic sobre la tarjeta de un artículo en la cuadrícula.* | *El sistema agrega el artículo al carrito con cantidad 1. Si ya existe en el carrito, incrementa su cantidad en uno. El sistema actualiza en tiempo real la base afecta, el IGV (18%) y el total a pagar.* |

##### c) PP03 – Ajuste de cantidades de ítems en el carrito

| **IDENTIFICADOR:** | *PP03* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP01 – Registrar venta rápida en el POS* | **NOMBRE:** *Ajuste de cantidades de ítems en el carrito* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que los botones + y − de cada ítem del carrito del POS permitan ajustar correctamente las cantidades, y que el sistema recalcule automáticamente el subtotal del ítem, la base afecta, el IGV (18%) y el total a pagar con cada cambio.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario tiene al menos un artículo en el carrito del POS.* | *El sistema muestra el ítem con cantidad 1, su tipo de afectación (IGV, Exon. o Inaf.), precio unitario y subtotal.* |
| *El usuario hace clic en el botón "+" del ítem en el carrito.* | *El sistema incrementa la cantidad del ítem en uno y recalcula automáticamente el subtotal del ítem, la base afecta, el IGV (18%) y el total a pagar.* |
| *El usuario hace clic en el botón "−" del ítem en el carrito.* | *El sistema reduce la cantidad del ítem en uno y recalcula automáticamente el subtotal del ítem, la base afecta, el IGV (18%) y el total a pagar.* |

##### d) PP04 – Eliminación de ítem del carrito

| **IDENTIFICADOR:** | *PP04* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP01 – Registrar venta rápida en el POS* | **NOMBRE:** *Eliminación de ítem del carrito* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el botón ✕ de cada ítem del carrito del POS permita eliminar correctamente el artículo seleccionado, y que el sistema recalcule automáticamente el resumen de importes tras la eliminación.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario tiene al menos dos artículos en el carrito del POS.* | *El sistema muestra los ítems con sus cantidades, tipos de afectación, precios unitarios y subtotales.* |
| *El usuario hace clic en el botón "✕" de uno de los ítems del carrito.* | *El sistema elimina el ítem del carrito y recalcula automáticamente la base afecta, el IGV (18%) y el total a pagar.* |

##### e) PP05 – Intento de cobro sin artículos en el carrito

| **IDENTIFICADOR:** | *PP05* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP01 – Registrar venta rápida en el POS* | **NOMBRE:** *Intento de cobro sin artículos en el carrito* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el sistema no habilite el botón "Cobrar" cuando el carrito del POS está vacío, impidiendo así el registro de una venta sin artículos.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario accede al módulo Punto de Venta con el carrito vacío (sin artículos agregados).* | *El sistema no habilita el botón "Cobrar". El usuario no puede proceder al registro del cobro mientras el carrito esté vacío.* |

##### f) PP06 – Registro de cobro con monto recibido menor al total

| **IDENTIFICADOR:** | *PP06* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP01 – Registrar venta rápida en el POS* | **NOMBRE:** *Registro de cobro con monto recibido menor al total* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el sistema muestre una advertencia y no permita continuar con el registro de la venta cuando el monto ingresado en el campo "Recibido" es menor al Total a Pagar del comprobante.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario tiene artículos en el carrito del POS y hace clic en el botón "Cobrar".* | *El sistema abre el formulario "Cobrar venta" mostrando el resumen de importes: Base afecta, IGV (18%) y Total a Pagar.* |
| *El usuario selecciona el Tipo de Comprobante y la Forma de Pago.* | |
| *El usuario ingresa en el campo "Recibido" un monto menor al Total a Pagar.* | *El sistema valida que el monto ingresado sea igual o mayor al Total a Pagar. Al detectar que el monto es insuficiente, muestra el mensaje "El monto recibido es insuficiente" y no permite continuar con el registro de la venta.* |

##### g) PP07 – Registro de cobro sin seleccionar tipo de comprobante

| **IDENTIFICADOR:** | *PP07* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP01 – Registrar venta rápida en el POS* | **NOMBRE:** *Registro de cobro sin seleccionar tipo de comprobante* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el sistema marque visualmente el campo "Tipo de Comprobante" como obligatorio y no permita guardar la venta si el usuario no ha seleccionado ningún tipo de comprobante en el formulario "Cobrar venta".* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario tiene artículos en el carrito del POS y hace clic en el botón "Cobrar".* | *El sistema abre el formulario "Cobrar venta" mostrando el resumen de importes.* |
| *El usuario selecciona la Forma de Pago e ingresa el monto recibido, pero no selecciona el Tipo de Comprobante.* | |
| *El usuario intenta hacer clic en "Guardar venta".* | *El sistema marca visualmente el campo "Tipo de Comprobante" como obligatorio y no permite guardar la venta hasta que se complete la selección.* |

##### h) PP08 – Registro de cobro sin seleccionar forma de pago

| **IDENTIFICADOR:** | *PP08* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP01 – Registrar venta rápida en el POS* | **NOMBRE:** *Registro de cobro sin seleccionar forma de pago* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el sistema marque visualmente el campo "Forma de Pago" como obligatorio y no permita guardar la venta si el usuario no ha seleccionado ninguna forma de pago en el formulario "Cobrar venta".* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario tiene artículos en el carrito del POS y hace clic en el botón "Cobrar".* | *El sistema abre el formulario "Cobrar venta" mostrando el resumen de importes.* |
| *El usuario selecciona el Tipo de Comprobante e ingresa el monto recibido, pero no selecciona la Forma de Pago.* | |
| *El usuario intenta hacer clic en "Guardar venta".* | *El sistema marca visualmente el campo "Forma de Pago" como obligatorio y no permite guardar la venta hasta que se complete la selección.* |

##### i) PP09 – Registro exitoso de venta completa (cobro)

| **IDENTIFICADOR:** | *PP09* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP01 – Registrar venta rápida en el POS* | **NOMBRE:** *Registro exitoso de venta completa (cobro)* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida el flujo completo de registro de una venta en el POS, desde la adición de artículos al carrito hasta la confirmación del cobro. El sistema debe registrar la venta, emitir el comprobante electrónico con serie y correlativo automáticos, mostrar la notificación de confirmación, limpiar el carrito y registrar el documento en el módulo Ventas.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario tiene artículos en el carrito del POS y verifica el resumen: Base afecta, IGV (18%) y Total a Pagar.* | *El sistema muestra en tiempo real los importes calculados automáticamente.* |
| *El usuario hace clic en el botón "Cobrar".* | *El sistema abre el formulario "Cobrar venta" con el resumen de importes.* |
| *El usuario selecciona el Tipo de Comprobante (ej: Boleta de Venta Electrónica).* | *El sistema asigna automáticamente la Serie (B001 para Boletas, F001 para Facturas) y el Correlativo secuencial. No deben modificarse manualmente.* |
| *El usuario selecciona la Forma de Pago entre las opciones habilitadas por el Administrador (ej: Efectivo).* | |
| *El usuario ingresa el monto recibido, igual o mayor al Total a Pagar.* | |
| *El usuario hace clic en "Guardar venta".* | *El sistema registra la venta, emite el comprobante electrónico, muestra la notificación "Venta registrada correctamente", limpia el carrito para la siguiente transacción, registra el documento en el módulo Ventas con estado "Activa" y SUNAT "No enviado", y actualiza el stock de artículos vendidos.* |

##### j) PP10 – Cancelación de venta en proceso

| **IDENTIFICADOR:** | *PP10* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP02 – Cancelar venta en proceso en el POS* | **NOMBRE:** *Cancelación de venta en proceso* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el botón "Cancelar" del panel del carrito limpie correctamente todos los ítems del carrito sin generar ningún registro ni comprobante, dejando el módulo POS disponible para iniciar una nueva transacción.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario tiene artículos en el carrito del POS.* | *El sistema muestra el carrito con los ítems y el resumen de importes calculados.* |
| *El usuario hace clic en el botón "Cancelar" en el panel del carrito.* | *El sistema limpia todo el carrito sin generar ningún registro ni comprobante. El módulo POS queda disponible para iniciar una nueva transacción inmediatamente.* |

---

### 5. UC-04 – GESTIONAR VENTAS

#### 5.1. CASOS DE PRUEBA

##### a) CP01 – Listar y filtrar comprobantes de ventas

| **IDENTIFICADOR:** *CP01* | **NOMBRE:** *Listar y filtrar comprobantes de ventas* |
| --- | --- |
| **Requerimiento vinculado:** *RF-VEN-004* | **Prioridad de prueba:** *Alta* |
| **Documentos de visualización asociados:** *Documento de Especificación de Requerimientos de Software — Sistema Punto de Venta Comercial.* |
| **Precondición:** *El usuario debe estar autenticado con credenciales válidas y contar con permisos de acceso al módulo Ventas, conforme a la configuración RBAC de su rol.* |
| **Descripción:** *El sistema debe presentar el módulo Ventas con el panel de filtros en la parte superior y el listado de comprobantes. El usuario puede aplicar filtros por: Desde / Hasta (rango de fechas), Cliente, Serie, Nro. Doc., Tipo Doc. (Todos, Factura, Boleta, N. Crédito, N. Débito), Estado (Todos, Activa, Anulada) y Estado SUNAT (Todos, No enviado, Aceptado, Rechazado). Los contadores muestran el Total de registros, Total en página, Activas y Anuladas. El estado SUNAT se muestra con colores: gris "No enviado", verde "Aceptado", rojo "Rechazado".* |
| **DATOS DE ENTRADA** |
| **CAMPO/DATO** | **TIPO DE DATO** |
| *Desde (fecha inicio)* | *Fecha* |
| *Hasta (fecha fin)* | *Fecha* |
| *Cliente* | *Cadena* |
| *Serie* | *Cadena* |
| *Nro. Doc.* | *Numérico* |
| *Tipo Doc.* | *Cadena (selección)* |
| *Estado* | *Cadena (selección)* |
| *Estado SUNAT* | *Cadena (selección)* |
| **ESCENARIO DE PRUEBAS** *EP01: Listado de comprobantes con filtros aplicados* *EP02: Listado sin resultados al aplicar filtros sin coincidencias* |
| **CRITERIOS DE ACEPTACIÓN** El sistema muestra el listado de comprobantes con los contadores: Total de registros, Total en página, Activas y Anuladas. Al aplicar filtros y hacer clic en "Buscar", el sistema actualiza el listado mostrando únicamente los comprobantes que cumplen los criterios seleccionados. El botón "Limpiar" restablece todos los filtros y recarga el listado completo. Cada fila del listado muestra: CLIENTE, FECHA, SERIE/N°, TIPO, ESTADO y SUNAT. El estado SUNAT se muestra con colores: gris para "No enviado", verde para "Aceptado" y rojo para "Rechazado". |

##### b) CP02 – Ver detalle de comprobante

| **IDENTIFICADOR:** *CP02* | **NOMBRE:** *Ver detalle de comprobante* |
| --- | --- |
| **Requerimiento vinculado:** *RF-VEN-004* | **Prioridad de prueba:** *Alta* |
| **Documentos de visualización asociados:** *Documento de Especificación de Requerimientos de Software — Sistema Punto de Venta Comercial.* |
| **Precondición:** *El usuario debe estar autenticado, con permisos de acceso al módulo Ventas y con comprobantes registrados en el listado.* |
| **Descripción:** *El sistema debe permitir al usuario visualizar el detalle completo de un comprobante haciendo clic en el ícono "Ver" (👁) de la columna ACCIONES. El panel de detalle debe mostrar: encabezado (tipo de documento, número de serie, fecha y cliente), resumen financiero (BASE AFECTA, IGV 18%, TOTAL), detalle de ítems (código, descripción, cantidad, precio unitario y subtotal), forma de pago y botón "Enviar SUNAT".* |
| **DATOS DE ENTRADA** |
| **CAMPO/DATO** | **TIPO DE DATO** |
| *Ícono "Ver" (👁) en la columna ACCIONES* | *Acción de usuario* |
| **ESCENARIO DE PRUEBAS** *EP01: Visualización del detalle completo de un comprobante* |
| **CRITERIOS DE ACEPTACIÓN** Al hacer clic en el ícono "Ver" (👁), el sistema abre el panel de detalle con: encabezado (tipo, serie, fecha, cliente), resumen financiero (BASE AFECTA, IGV 18%, TOTAL), detalle de ítems (código, descripción, cantidad, precio, subtotal), forma de pago y botón "Enviar SUNAT". |

##### c) CP03 – Imprimir comprobante

| **IDENTIFICADOR:** *CP03* | **NOMBRE:** *Imprimir comprobante* |
| --- | --- |
| **Requerimiento vinculado:** *RF-VEN-004* | **Prioridad de prueba:** *Media* |
| **Documentos de visualización asociados:** *Documento de Especificación de Requerimientos de Software — Sistema Punto de Venta Comercial.* |
| **Precondición:** *El usuario debe estar autenticado, con permisos de acceso al módulo Ventas y con comprobantes registrados en el listado.* |
| **Descripción:** *El sistema debe permitir al usuario abrir la vista previa en PDF del comprobante haciendo clic en el ícono "Imprimir" (🖨) de la columna ACCIONES. La vista previa debe mostrar el comprobante oficial con membrete de la empresa, tipo y número de serie, información del cliente, detalle de ítems, resumen de importes y código QR para verificación en línea.* |
| **DATOS DE ENTRADA** |
| **CAMPO/DATO** | **TIPO DE DATO** |
| *Ícono "Imprimir" (🖨) en la columna ACCIONES* | *Acción de usuario* |
| **ESCENARIO DE PRUEBAS** *EP01: Impresión de comprobante en vista previa PDF* |
| **CRITERIOS DE ACEPTACIÓN** Al hacer clic en el ícono "Imprimir" (🖨), el sistema abre la vista previa en PDF con: membrete de la empresa (razón social, dirección y RUC), tipo de documento y número de serie, información del cliente (nombre, tipo de documento, número y RUC), detalle de ítems con cantidades y precios, resumen de importes (base afecta, IGV, otros tributos e importe total) y código QR para verificación en línea. El usuario puede hacer clic en "Imprimir" para enviar a la impresora o en "Abrir en navegador" para ver en pantalla completa. |

##### d) CP04 – Descargar XML/CDR

| **IDENTIFICADOR:** *CP04* | **NOMBRE:** *Descargar XML/CDR* |
| --- | --- |
| **Requerimiento vinculado:** *RF-VEN-004* | **Prioridad de prueba:** *Media* |
| **Documentos de visualización asociados:** *Documento de Especificación de Requerimientos de Software — Sistema Punto de Venta Comercial.* |
| **Precondición:** *El usuario debe estar autenticado, con permisos de acceso al módulo Ventas. El comprobante debe haber sido aceptado por SUNAT para que el CDR esté disponible.* |
| **Descripción:** *El sistema debe permitir al usuario descargar el archivo XML del comprobante y el CDR (Constancia de Recepción) de SUNAT haciendo clic en el ícono "Descargar" (⬇) de la columna ACCIONES. Los archivos están almacenados en Azure Blob Storage.* |
| **DATOS DE ENTRADA** |
| **CAMPO/DATO** | **TIPO DE DATO** |
| *Ícono "Descargar" (⬇) en la columna ACCIONES* | *Acción de usuario* |
| **ESCENARIO DE PRUEBAS** *EP01: Descarga de archivo XML/CDR de un comprobante aceptado* |
| **CRITERIOS DE ACEPTACIÓN** Al hacer clic en el ícono "Descargar" (⬇), el sistema descarga el archivo XML del comprobante y el CDR (Constancia de Recepción) de SUNAT almacenados en Azure Blob Storage. |

##### e) CP05 – Editar documento de venta

| **IDENTIFICADOR:** *CP05* | **NOMBRE:** *Editar documento de venta* |
| --- | --- |
| **Requerimiento vinculado:** *RF-VEN-004* | **Prioridad de prueba:** *Alta* |
| **Documentos de visualización asociados:** *Documento de Especificación de Requerimientos de Software — Sistema Punto de Venta Comercial.* |
| **Precondición:** *El usuario debe estar autenticado, con permisos de acceso al módulo Ventas. El documento debe encontrarse en estado "No enviado" a SUNAT para que la opción de edición esté disponible.* |
| **Descripción:** *El sistema debe permitir al usuario editar los campos modificables de un documento no enviado a SUNAT: Tipo Documento, Serie, Subdiario contable, Fecha Emisión, Tipo Moneda y Tipo Cambio. Para documentos ya enviados a SUNAT, el ícono de edición no estará disponible. Al guardar los cambios, el sistema valida los datos, actualiza el registro y regresa al listado con la información actualizada.* |
| **DATOS DE ENTRADA** |
| **CAMPO/DATO** | **TIPO DE DATO** |
| *Tipo Documento* | *Cadena (selección)* |
| *Serie* | *Cadena* |
| *Subdiario contable* | *Cadena (selección)* |
| *Fecha Emisión* | *Fecha* |
| *Tipo Moneda* | *Cadena (selección)* |
| *Tipo Cambio* | *Numérico* |
| **ESCENARIO DE PRUEBAS** *EP01: Edición exitosa de documento no enviado a SUNAT* *EP02: Intento de edición de documento ya enviado a SUNAT* |
| **CRITERIOS DE ACEPTACIÓN** El ícono "Editar" (✏) solo está disponible para documentos no enviados a SUNAT. Al hacer clic en el ícono "Editar" (✏), el sistema abre el formulario "Editar Venta" con los campos modificables: Tipo Documento, Serie, Subdiario contable, Fecha Emisión, Tipo Moneda y Tipo Cambio. Al hacer clic en "Guardar Cambios", el sistema valida los datos, actualiza el registro y regresa al listado con la información actualizada. Al hacer clic en "Cancelar", el sistema descarta los cambios sin modificar el registro. Para documentos ya enviados a SUNAT, el ícono de edición no está disponible para ese registro. |

##### f) CP06 – Enviar comprobante a SUNAT

| **IDENTIFICADOR:** *CP06* | **NOMBRE:** *Enviar comprobante a SUNAT* |
| --- | --- |
| **Requerimiento vinculado:** *RF-VEN-004* | **Prioridad de prueba:** *Alta* |
| **Documentos de visualización asociados:** *Documento de Especificación de Requerimientos de Software — Sistema Punto de Venta Comercial.* |
| **Precondición:** *El usuario debe estar autenticado con permisos de "Envío a SUNAT" asignados en su rol. El comprobante debe encontrarse en estado SUNAT "No enviado".* |
| **Descripción:** *El sistema debe permitir enviar el comprobante a SUNAT de forma asíncrona haciendo clic en el ícono "Enviar a SUNAT" (☁) de la columna ACCIONES o en el botón "Enviar SUNAT" del panel de detalle. La integración con SUNAT opera de forma asíncrona, de modo que las demás operaciones del sistema no se bloqueen durante el proceso de envío. El estado cambia a "Aceptado" si fue validado o a "Rechazado" si fue rechazado por datos inconsistentes.* |
| **DATOS DE ENTRADA** |
| **CAMPO/DATO** | **TIPO DE DATO** |
| *Ícono "Enviar a SUNAT" (☁) en la columna ACCIONES o botón "Enviar SUNAT" en el panel de detalle* | *Acción de usuario* |
| **ESCENARIO DE PRUEBAS** *EP01: Envío exitoso de comprobante a SUNAT (estado Aceptado)* *EP02: Envío de comprobante a SUNAT con resultado Rechazado* |
| **CRITERIOS DE ACEPTACIÓN** Al hacer clic en el ícono "Enviar a SUNAT" (☁) o en el botón "Enviar SUNAT" del panel de detalle, el sistema envía el comprobante de forma asíncrona a SUNAT sin bloquear las demás operaciones del sistema. Si SUNAT valida y acepta el comprobante, el estado cambia a "Aceptado" (verde). Si SUNAT rechaza el comprobante, el estado cambia a "Rechazado" (rojo) y el sistema detalla el motivo del rechazo. Si la conexión con SUNAT falla, el estado del comprobante se mantiene como "Pendiente" sin interrumpir las demás operaciones del sistema. |

##### g) CP07 – Anular documento de venta

| **IDENTIFICADOR:** *CP07* | **NOMBRE:** *Anular documento de venta* |
| --- | --- |
| **Requerimiento vinculado:** *RF-VEN-004* | **Prioridad de prueba:** *Alta* |
| **Documentos de visualización asociados:** *Documento de Especificación de Requerimientos de Software — Sistema Punto de Venta Comercial.* |
| **Precondición:** *El usuario debe estar autenticado con permisos de acceso al módulo Ventas. El documento debe encontrarse en estado "Activa" para que la opción de anulación esté disponible.* |
| **Descripción:** *El sistema debe permitir al usuario anular un documento en estado "Activa" haciendo clic en el ícono "Anular" (⊘) de la columna ACCIONES. El sistema muestra un cuadro de diálogo solicitando confirmación. Al confirmar, el documento cambia a estado "Anulado" y se conserva en el historial para auditoría; el documento no es eliminado del sistema. Para documentos ya anulados, la opción de anulación no estará disponible. Las facturas y boletas electrónicas aceptadas por SUNAT no pueden anularse directamente; debe emitirse una Nota de Crédito Electrónica vinculada al comprobante original.* |
| **DATOS DE ENTRADA** |
| **CAMPO/DATO** | **TIPO DE DATO** |
| *Ícono "Anular" (⊘) en la columna ACCIONES* | *Acción de usuario* |
| *Confirmación de anulación en cuadro de diálogo* | *Acción de usuario* |
| **ESCENARIO DE PRUEBAS** *EP01: Anulación exitosa de documento en estado Activa* *EP02: Intento de anulación de documento ya Anulado* |
| **CRITERIOS DE ACEPTACIÓN** El ícono "Anular" (⊘) solo está disponible para documentos en estado "Activa". Al hacer clic en el ícono "Anular" (⊘), el sistema muestra un cuadro de diálogo solicitando confirmación de la operación. Al confirmar, el sistema cambia el estado del documento a "Anulado" y lo conserva en el historial para auditoría. El documento no es eliminado del sistema. Para documentos con estado "Anulado", la opción de anulación no está disponible. |

---

#### 5.2. PROCEDIMIENTO DE PRUEBA

##### a) PP01 – Listado de comprobantes con filtros aplicados

| **IDENTIFICADOR:** | *PP01* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP01 – Listar y filtrar comprobantes de ventas* | **NOMBRE:** *Listado de comprobantes con filtros aplicados* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el sistema filtre correctamente el listado de comprobantes al aplicar criterios de búsqueda como rango de fechas, cliente, serie, número de documento, tipo de documento, estado y estado SUNAT.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario hace clic en "Ventas" en el menú lateral izquierdo.* | *El sistema presenta el módulo Ventas con el panel de filtros en la parte superior y el listado de comprobantes. Los contadores muestran: Total de registros, Total en página, Activas y Anuladas.* |
| *El usuario completa los campos del panel de filtros: Desde (fecha inicio), Hasta (fecha fin), Tipo Doc. (ej: Boleta) y Estado SUNAT (ej: Aceptado).* | |
| *El usuario hace clic en "Buscar".* | *El sistema actualiza el listado mostrando únicamente los comprobantes que cumplen los criterios seleccionados. Cada fila muestra: CLIENTE, FECHA, SERIE/N°, TIPO, ESTADO y SUNAT con sus colores correspondientes (gris: No enviado, verde: Aceptado, rojo: Rechazado).* |
| *El usuario hace clic en "Limpiar".* | *El sistema restablece todos los filtros y recarga el listado completo de comprobantes.* |

##### b) PP02 – Listado sin resultados al aplicar filtros sin coincidencias

| **IDENTIFICADOR:** | *PP02* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP01 – Listar y filtrar comprobantes de ventas* | **NOMBRE:** *Listado sin resultados al aplicar filtros sin coincidencias* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida el comportamiento del sistema cuando los filtros aplicados no arrojan ningún comprobante coincidente. El sistema debe presentar el listado vacío sin generar errores.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario se encuentra en el módulo Ventas con el panel de filtros visible.* | |
| *El usuario ingresa en el campo "Nro. Doc." un número de documento que no existe en el sistema.* | |
| *El usuario hace clic en "Buscar".* | *El sistema actualiza el listado sin mostrar registros, presentando el resultado vacío sin generar mensajes de error.* |

##### c) PP03 – Visualización del detalle completo de un comprobante

| **IDENTIFICADOR:** | *PP03* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP02 – Ver detalle de comprobante* | **NOMBRE:** *Visualización del detalle completo de un comprobante* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que al hacer clic en el ícono "Ver" (👁) de un comprobante del listado, el sistema abra el panel de detalle completo con toda la información del documento.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario se encuentra en el módulo Ventas con el listado de comprobantes visible.* | |
| *El usuario hace clic en el ícono "Ver" (👁) en la columna ACCIONES de un comprobante.* | *El sistema abre el panel de detalle completo mostrando: encabezado (tipo de documento, número de serie, fecha y cliente), resumen financiero (BASE AFECTA, IGV 18%, TOTAL), detalle de ítems (código, descripción, cantidad, precio unitario y subtotal), forma de pago y monto abonado, y botón "Enviar SUNAT".* |

##### d) PP04 – Impresión de comprobante en vista previa PDF

| **IDENTIFICADOR:** | *PP04* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP03 – Imprimir comprobante* | **NOMBRE:** *Impresión de comprobante en vista previa PDF* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que al hacer clic en el ícono "Imprimir" (🖨) de un comprobante del listado, el sistema genere y muestre la vista previa del comprobante en formato PDF con todos los elementos requeridos para su impresión oficial.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario se encuentra en el módulo Ventas con el listado de comprobantes visible.* | |
| *El usuario hace clic en el ícono "Imprimir" (🖨) en la columna ACCIONES de un comprobante.* | *El sistema abre la vista previa en PDF con: membrete de la empresa (razón social, dirección y RUC), tipo de documento y número de serie, información del cliente, detalle de ítems con cantidades y precios, resumen de importes (base afecta, IGV, otros tributos e importe total) y código QR para verificación en línea.* |
| *El usuario hace clic en "Imprimir".* | *El sistema envía el documento a la impresora.* |
| *El usuario hace clic en "Abrir en navegador".* | *El sistema abre el documento en pantalla completa.* |

##### e) PP05 – Descarga de archivo XML/CDR de un comprobante aceptado

| **IDENTIFICADOR:** | *PP05* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP04 – Descargar XML/CDR* | **NOMBRE:** *Descarga de archivo XML/CDR de un comprobante aceptado* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que al hacer clic en el ícono "Descargar" (⬇) de un comprobante aceptado por SUNAT, el sistema descargue correctamente el archivo XML del comprobante y el CDR de SUNAT.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario se encuentra en el módulo Ventas con el listado de comprobantes visible.* | |
| *El usuario localiza un comprobante con estado SUNAT "Aceptado" (verde) y hace clic en el ícono "Descargar" (⬇) en la columna ACCIONES.* | *El sistema descarga el archivo XML del comprobante y el CDR (Constancia de Recepción) de SUNAT almacenados en Azure Blob Storage.* |

##### f) PP06 – Edición exitosa de documento no enviado a SUNAT

| **IDENTIFICADOR:** | *PP06* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP05 – Editar documento de venta* | **NOMBRE:** *Edición exitosa de documento no enviado a SUNAT* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el sistema permita editar correctamente los campos modificables de un documento de venta no enviado a SUNAT, y que los cambios queden guardados correctamente al confirmar la edición.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario se encuentra en el módulo Ventas con el listado de comprobantes visible.* | |
| *El usuario localiza un documento con estado SUNAT "No enviado" y hace clic en el ícono "Editar" (✏) en la columna ACCIONES.* | *El sistema abre el formulario "Editar Venta" con los campos modificables: Tipo Documento, Serie, Subdiario contable, Fecha Emisión, Tipo Moneda y Tipo Cambio.* |
| *El usuario modifica el campo "Fecha Emisión" y/o el "Tipo Moneda".* | |
| *El usuario hace clic en "Guardar Cambios".* | *El sistema valida los datos ingresados, actualiza el registro y regresa al listado con la información actualizada.* |

##### g) PP07 – Intento de edición de documento ya enviado a SUNAT

| **IDENTIFICADOR:** | *PP07* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP05 – Editar documento de venta* | **NOMBRE:** *Intento de edición de documento ya enviado a SUNAT* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el sistema no permita la edición de documentos que ya han sido enviados a SUNAT, verificando que el ícono de edición no esté disponible para dichos registros en el listado de ventas.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario se encuentra en el módulo Ventas con el listado de comprobantes visible.* | |
| *El usuario localiza un documento con estado SUNAT "Aceptado" o "Rechazado".* | *El sistema no muestra disponible el ícono "Editar" (✏) para ese documento, impidiendo cualquier intento de edición de un comprobante ya enviado a SUNAT.* |

##### h) PP08 – Envío exitoso de comprobante a SUNAT (estado Aceptado)

| **IDENTIFICADOR:** | *PP08* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP06 – Enviar comprobante a SUNAT* | **NOMBRE:** *Envío exitoso de comprobante a SUNAT (estado Aceptado)* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el sistema envíe correctamente el comprobante a SUNAT de forma asíncrona al hacer clic en el ícono "Enviar a SUNAT" (☁), y que el estado del comprobante se actualice a "Aceptado" (verde) cuando SUNAT lo valida satisfactoriamente.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario se encuentra en el módulo Ventas con el listado de comprobantes visible.* | |
| *El usuario localiza un documento con estado SUNAT "No enviado" (gris) y hace clic en el ícono "Enviar a SUNAT" (☁) en la columna ACCIONES.* | *El sistema envía el comprobante de forma asíncrona a SUNAT sin bloquear las demás operaciones del sistema. El estado SUNAT cambia a "Aceptado" (verde) una vez que SUNAT valida y acepta el comprobante correctamente.* |

##### i) PP09 – Envío de comprobante a SUNAT con resultado Rechazado

| **IDENTIFICADOR:** | *PP09* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP06 – Enviar comprobante a SUNAT* | **NOMBRE:** *Envío de comprobante a SUNAT con resultado Rechazado* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el sistema refleje correctamente el estado "Rechazado" cuando SUNAT rechaza el comprobante enviado por datos inconsistentes, y que el sistema detalle el motivo del rechazo.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario localiza un documento con estado SUNAT "No enviado" que contiene datos inconsistentes y hace clic en el ícono "Enviar a SUNAT" (☁) en la columna ACCIONES.* | *El sistema envía el comprobante de forma asíncrona a SUNAT. SUNAT rechaza el comprobante por datos inconsistentes. El estado SUNAT cambia a "Rechazado" (rojo) y el sistema muestra el motivo del rechazo para que el usuario pueda corregir los datos y reenviar.* |

##### j) PP10 – Anulación exitosa de documento en estado Activa

| **IDENTIFICADOR:** | *PP10* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP07 – Anular documento de venta* | **NOMBRE:** *Anulación exitosa de documento en estado Activa* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el sistema permita anular correctamente un documento de venta en estado "Activa", conservándolo en el historial con estado "Anulado" para fines de auditoría.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario se encuentra en el módulo Ventas con el listado de comprobantes visible.* | |
| *El usuario localiza un documento con estado "Activa" y hace clic en el ícono "Anular" (⊘) en la columna ACCIONES.* | *El sistema muestra un cuadro de diálogo solicitando confirmación de la operación de anulación.* |
| *El usuario confirma la operación en el cuadro de diálogo.* | *El sistema cambia el estado del documento a "Anulado" y lo conserva en el historial para auditoría. El documento no es eliminado del sistema.* |

##### k) PP11 – Intento de anulación de documento ya Anulado

| **IDENTIFICADOR:** | *PP11* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP07 – Anular documento de venta* | **NOMBRE:** *Intento de anulación de documento ya Anulado* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el sistema no permita la anulación de documentos que ya tienen estado "Anulado", verificando que el ícono de anulación no esté disponible para dichos registros en el listado de ventas.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario se encuentra en el módulo Ventas con el listado de comprobantes visible.* | |
| *El usuario localiza un documento con estado "Anulado".* | *El sistema no muestra disponible el ícono "Anular" (⊘) para ese documento, impidiendo cualquier intento de anulación de un comprobante ya anulado.* |

---

### 6. UC-05 – GESTIONAR PEDIDOS

#### 6.1. CASOS DE PRUEBA

##### a) CP01 – Registrar pedido

| **IDENTIFICADOR:** *CP01* | **NOMBRE:** *Registrar pedido* |
| --- | --- |
| **Requerimiento vinculado:** *RF-PED-005* | **Prioridad de prueba:** *Alta* |
| **Documentos de visualización asociados:** *Documento de Especificación de Requerimientos de Software — Sistema Punto de Venta Comercial.* |
| **Precondición:** *El usuario debe estar autenticado con credenciales válidas y contar con permisos de acceso al módulo Pedidos, conforme a la configuración RBAC de su rol.* |
| **Descripción:** *El sistema debe permitir registrar nuevas órdenes de pedido previas a la facturación final. El formulario de registro debe incluir datos del cliente (búsqueda por nombre, razón social o número de documento), ítems (código, descripción, cantidad y precio unitario), y fecha de entrega. El sistema calcula automáticamente en tiempo real el subtotal de cada ítem, la base imponible, el IGV (18%) y el total del pedido. Al guardar, el pedido queda registrado con estado "Activo" y es visible en el listado de pedidos y en la tabla de últimos pedidos del Dashboard.* |
| **DATOS DE ENTRADA** |
| **CAMPO/DATO** | **TIPO DE DATO** |
| *Datos del cliente (nombre, razón social o número de documento)* | *Cadena* |
| *Código del ítem* | *Cadena* |
| *Descripción del ítem* | *Cadena* |
| *Cantidad del ítem* | *Numérico* |
| *Precio unitario del ítem* | *Numérico* |
| *Fecha de entrega* | *Fecha* |
| **ESCENARIO DE PRUEBAS** *EP01: Registro exitoso de nuevo pedido* *EP02: Registro fallido de pedido con campos obligatorios vacíos* *EP03: Registro fallido con precio o cantidad no numérica* |
| **CRITERIOS DE ACEPTACIÓN** El sistema permite registrar un nuevo pedido con datos completos y válidos. El sistema calcula automáticamente en tiempo real el subtotal de cada ítem, la base imponible, el IGV (18%) y el total del pedido. Si no se completan los campos obligatorios (datos del cliente o al menos un ítem con cantidad y precio), el sistema muestra mensajes de validación y no permite guardar. Si el precio unitario o la cantidad de un ítem son valores no numéricos o negativos, el sistema muestra advertencias en tiempo real e impide el guardado. Al guardar exitosamente, el pedido queda registrado con estado "Activo", se genera el número correlativo y es visible en el listado y en la tabla de últimos pedidos del Dashboard. |

##### b) CP02 – Editar pedido

| **IDENTIFICADOR:** *CP02* | **NOMBRE:** *Editar pedido* |
| --- | --- |
| **Requerimiento vinculado:** *RF-PED-005* | **Prioridad de prueba:** *Alta* |
| **Documentos de visualización asociados:** *Documento de Especificación de Requerimientos de Software — Sistema Punto de Venta Comercial.* |
| **Precondición:** *El usuario debe estar autenticado, con permisos de acceso al módulo Pedidos. El pedido debe encontrarse en estado "Activo" para que la opción de edición esté disponible.* |
| **Descripción:** *El sistema debe permitir al usuario editar un pedido en estado "Activo". El formulario de edición carga los datos actuales del pedido y permite modificar ítems, cantidades, precios, fecha de entrega y datos del cliente. El sistema recalcula dinámicamente la base imponible, el IGV y el total con cada modificación. Para pedidos en estado "Atendido" o "Anulado", la opción de edición no está disponible.* |
| **DATOS DE ENTRADA** |
| **CAMPO/DATO** | **TIPO DE DATO** |
| *Ítems (código, descripción, cantidad, precio unitario)* | *Cadena / Numérico* |
| *Fecha de entrega* | *Fecha* |
| *Datos del cliente* | *Cadena* |
| **ESCENARIO DE PRUEBAS** *EP01: Edición exitosa de pedido en estado Activo* *EP02: Intento de edición de pedido en estado Atendido o Anulado* |
| **CRITERIOS DE ACEPTACIÓN** El ícono de edición solo está disponible para pedidos en estado "Activo". Al editar, el sistema carga el formulario con los datos actuales del pedido. El sistema recalcula dinámicamente la base imponible, IGV y total con cada modificación de ítems, cantidades o precios. Al hacer clic en "Guardar Cambios", el sistema valida, actualiza el registro y regresa al listado con la información actualizada. Para pedidos en estado "Atendido" o "Anulado", la opción de edición no está disponible. |

##### c) CP03 – Convertir pedido en venta

| **IDENTIFICADOR:** *CP03* | **NOMBRE:** *Convertir pedido en venta* |
| --- | --- |
| **Requerimiento vinculado:** *RF-PED-005* | **Prioridad de prueba:** *Alta* |
| **Documentos de visualización asociados:** *Documento de Especificación de Requerimientos de Software — Sistema Punto de Venta Comercial.* |
| **Precondición:** *El usuario debe estar autenticado, con permisos de acceso al módulo Pedidos. El pedido debe encontrarse en estado "Activo".* |
| **Descripción:** *El sistema debe permitir convertir un pedido "Activo" en una venta generando el comprobante correspondiente. Al confirmar la conversión, el sistema solicita el tipo de comprobante (Boleta o Factura) y la forma de pago, genera el comprobante electrónico con serie y correlativo automáticos, registra la venta en el módulo Ventas con estado "Activa" y SUNAT "No enviado", y actualiza el pedido a estado "Atendido".* |
| **DATOS DE ENTRADA** |
| **CAMPO/DATO** | **TIPO DE DATO** |
| *Tipo de comprobante (Boleta o Factura)* | *Cadena (selección)* |
| *Forma de pago* | *Cadena (selección)* |
| **ESCENARIO DE PRUEBAS** *EP01: Conversión exitosa de pedido a venta* |
| **CRITERIOS DE ACEPTACIÓN** Solo es posible convertir pedidos en estado "Activo". Al confirmar la conversión con el tipo de comprobante y forma de pago, el sistema genera el comprobante electrónico con serie y correlativo automáticos, registra la venta en el módulo Ventas con estado "Activa" y SUNAT "No enviado", y actualiza el pedido a estado "Atendido". |

##### d) CP04 – Imprimir pedido

| **IDENTIFICADOR:** *CP04* | **NOMBRE:** *Imprimir pedido* |
| --- | --- |
| **Requerimiento vinculado:** *RF-PED-005* | **Prioridad de prueba:** *Media* |
| **Documentos de visualización asociados:** *Documento de Especificación de Requerimientos de Software — Sistema Punto de Venta Comercial.* |
| **Precondición:** *El usuario debe estar autenticado con permisos de acceso al módulo Pedidos.* |
| **Descripción:** *El sistema debe permitir al usuario generar la vista previa del pedido en formato imprimible haciendo clic en el ícono de impresión del listado. La vista previa debe mostrar datos del cliente, ítems, importes y fecha de entrega.* |
| **DATOS DE ENTRADA** |
| **CAMPO/DATO** | **TIPO DE DATO** |
| *Ícono de impresión del pedido en el listado* | *Acción de usuario* |
| **ESCENARIO DE PRUEBAS** *EP01: Impresión de pedido* |
| **CRITERIOS DE ACEPTACIÓN** Al hacer clic en el ícono de impresión, el sistema genera la vista previa del pedido en formato imprimible con datos del cliente, ítems, importes y fecha de entrega. Al hacer clic en "Imprimir", el sistema envía el documento a la impresora o lo abre en pantalla completa. |

##### e) CP05 – Anular pedido

| **IDENTIFICADOR:** *CP05* | **NOMBRE:** *Anular pedido* |
| --- | --- |
| **Requerimiento vinculado:** *RF-PED-005* | **Prioridad de prueba:** *Alta* |
| **Documentos de visualización asociados:** *Documento de Especificación de Requerimientos de Software — Sistema Punto de Venta Comercial.* |
| **Precondición:** *El usuario debe estar autenticado con permisos de acceso al módulo Pedidos. El pedido debe encontrarse en estado "Activo".* |
| **Descripción:** *El sistema debe permitir al usuario anular un pedido en estado "Activo". Al hacer clic en el ícono de anulación, el sistema muestra un cuadro de diálogo solicitando confirmación. Al confirmar, el pedido cambia a estado "Anulado" y se conserva en el historial para trazabilidad y auditoría. Para pedidos en estado "Atendido" o "Anulado", la opción de anulación no está disponible.* |
| **DATOS DE ENTRADA** |
| **CAMPO/DATO** | **TIPO DE DATO** |
| *Ícono de anulación del pedido en el listado* | *Acción de usuario* |
| *Confirmación de anulación en cuadro de diálogo* | *Acción de usuario* |
| **ESCENARIO DE PRUEBAS** *EP01: Anulación exitosa de pedido en estado Activo* *EP02: Intento de anulación de pedido en estado Atendido o Anulado* |
| **CRITERIOS DE ACEPTACIÓN** El ícono de anulación solo está disponible para pedidos en estado "Activo". Al confirmar la anulación, el sistema cambia el estado a "Anulado" y lo conserva en el historial para trazabilidad y auditoría. Para pedidos en estado "Atendido" o "Anulado", la opción de anulación no está disponible. |

---

#### 6.2. PROCEDIMIENTO DE PRUEBA

##### a) PP01 – Registro exitoso de nuevo pedido

| **IDENTIFICADOR:** | *PP01* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP01 – Registrar pedido* | **NOMBRE:** *Registro exitoso de nuevo pedido* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el sistema permita registrar correctamente un nuevo pedido con datos del cliente, ítems, cantidades, precios y fecha de entrega, verificando el cálculo automático en tiempo real de base imponible, IGV y total, y la correcta persistencia del registro en el listado y en la tabla de últimos pedidos del Dashboard.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario hace clic en el módulo Pedidos en el menú lateral o accede desde el acceso rápido "Nuevo Pedido" del Dashboard.* | *El sistema presenta el módulo con los indicadores: Total, Activos, Atendidos y Anulados.* |
| *El usuario hace clic en el botón de creación de nuevo pedido.* | *El sistema carga el formulario de registro con los campos: datos del cliente, ítems (código, descripción, cantidad, precio unitario), fecha de entrega y resumen de importes con cálculo dinámico.* |
| *El usuario ingresa o selecciona los datos del cliente (búsqueda por nombre, razón social o número de documento).* | *El sistema valida los datos del cliente.* |
| *El usuario agrega ítems al pedido con código, descripción, cantidad y precio unitario.* | *El sistema calcula automáticamente en tiempo real el subtotal de cada ítem, la base imponible, el IGV (18%) y el total del pedido.* |
| *El usuario ingresa la fecha de entrega.* | *El sistema registra la fecha de entrega indicada.* |
| *El usuario hace clic en "Guardar".* | *El sistema registra el pedido con estado "Activo", genera el número correlativo y lo presenta en el listado y en la tabla de últimos pedidos del Dashboard.* |

##### b) PP02 – Registro fallido de pedido con campos obligatorios vacíos

| **IDENTIFICADOR:** | *PP02* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP01 – Registrar pedido* | **NOMBRE:** *Registro fallido de pedido con campos obligatorios vacíos* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el sistema no permita guardar un pedido cuando los campos obligatorios (datos del cliente o al menos un ítem con cantidad y precio) no han sido completados, mostrando mensajes de validación correspondientes.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario se encuentra en el formulario de registro de nuevo pedido.* | |
| *El usuario no completa los datos del cliente ni agrega ningún ítem al pedido.* | |
| *El usuario intenta hacer clic en "Guardar".* | *El sistema muestra mensajes de validación indicando que los campos obligatorios deben ser completados y no permite guardar el pedido.* |

##### c) PP03 – Registro fallido con precio o cantidad no numérica

| **IDENTIFICADOR:** | *PP03* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP01 – Registrar pedido* | **NOMBRE:** *Registro fallido con precio o cantidad no numérica* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el sistema muestre advertencias en tiempo real e impida el guardado del pedido cuando el precio unitario o la cantidad de un ítem contienen valores no numéricos o negativos.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario se encuentra en el formulario de registro de nuevo pedido con datos del cliente completados.* | |
| *El usuario agrega un ítem al pedido e ingresa en el campo de cantidad el valor "-5" o una cadena de texto (ej: "abc").* | *El sistema muestra una advertencia en tiempo real indicando que el valor no es válido e impide el guardado del pedido.* |
| *El usuario ingresa en el campo de precio unitario el valor "0" o un valor negativo.* | *El sistema muestra una advertencia en tiempo real indicando que el valor no es válido e impide el guardado del pedido.* |

##### d) PP04 – Edición exitosa de pedido en estado Activo

| **IDENTIFICADOR:** | *PP04* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP02 – Editar pedido* | **NOMBRE:** *Edición exitosa de pedido en estado Activo* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el sistema permita editar correctamente un pedido en estado "Activo", que el sistema recalcule dinámicamente los importes con cada modificación y que los cambios queden guardados correctamente.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario se encuentra en el módulo Pedidos con el listado de pedidos visible.* | |
| *El usuario selecciona el ícono de edición en un pedido con estado "Activo".* | *El sistema carga el formulario de edición con los datos actuales del pedido.* |
| *El usuario modifica la cantidad de un ítem.* | *El sistema recalcula dinámicamente la base imponible, el IGV (18%) y el total del pedido.* |
| *El usuario hace clic en "Guardar Cambios".* | *El sistema valida los datos, actualiza el registro y regresa al listado con la información actualizada.* |

##### e) PP05 – Intento de edición de pedido en estado Atendido o Anulado

| **IDENTIFICADOR:** | *PP05* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP02 – Editar pedido* | **NOMBRE:** *Intento de edición de pedido en estado Atendido o Anulado* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el sistema no permita la edición de pedidos en estado "Atendido" o "Anulado", verificando que el ícono de edición no esté disponible para dichos registros.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario se encuentra en el módulo Pedidos con el listado de pedidos visible.* | |
| *El usuario localiza un pedido con estado "Atendido" o "Anulado".* | *El sistema no muestra disponible la opción de edición para ese pedido, impidiendo cualquier intento de modificación de un pedido en estado "Atendido" o "Anulado".* |

##### f) PP06 – Conversión exitosa de pedido a venta

| **IDENTIFICADOR:** | *PP06* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP03 – Convertir pedido en venta* | **NOMBRE:** *Conversión exitosa de pedido a venta* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el sistema permita convertir correctamente un pedido "Activo" en una venta, generando el comprobante electrónico correspondiente y actualizando el estado del pedido a "Atendido".* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario se encuentra en el módulo Pedidos con el listado de pedidos visible.* | |
| *El usuario selecciona la opción de conversión a venta en un pedido con estado "Activo".* | *El sistema solicita la confirmación del tipo de comprobante (Boleta o Factura) y la forma de pago.* |
| *El usuario selecciona el tipo de comprobante (ej: Boleta de Venta Electrónica) y la forma de pago.* | |
| *El usuario hace clic en el botón de confirmación.* | *El sistema genera el comprobante electrónico con serie y correlativo automáticos, registra la venta en el módulo Ventas con estado "Activa" y SUNAT "No enviado", y actualiza el pedido a estado "Atendido".* |

##### g) PP07 – Impresión de pedido

| **IDENTIFICADOR:** | *PP07* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP04 – Imprimir pedido* | **NOMBRE:** *Impresión de pedido* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que al hacer clic en el ícono de impresión de un pedido del listado, el sistema genere correctamente la vista previa del pedido en formato imprimible con todos los datos requeridos.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario se encuentra en el módulo Pedidos con el listado de pedidos visible.* | |
| *El usuario hace clic en el ícono de impresión de un pedido del listado.* | *El sistema genera la vista previa del pedido en formato imprimible con datos del cliente, ítems, importes y fecha de entrega.* |
| *El usuario hace clic en "Imprimir".* | *El sistema envía el documento a la impresora o lo abre en pantalla completa.* |

##### h) PP08 – Anulación exitosa de pedido en estado Activo

| **IDENTIFICADOR:** | *PP08* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP05 – Anular pedido* | **NOMBRE:** *Anulación exitosa de pedido en estado Activo* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el sistema permita anular correctamente un pedido en estado "Activo", conservándolo en el historial con estado "Anulado" para trazabilidad y auditoría.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario se encuentra en el módulo Pedidos con el listado de pedidos visible.* | |
| *El usuario hace clic en el ícono de anulación de un pedido con estado "Activo".* | *El sistema muestra un cuadro de diálogo solicitando confirmación de la anulación.* |
| *El usuario confirma la operación.* | *El sistema cambia el estado del pedido a "Anulado" y lo conserva en el historial para trazabilidad y auditoría.* |

##### i) PP09 – Intento de anulación de pedido en estado Atendido o Anulado

| **IDENTIFICADOR:** | *PP09* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP05 – Anular pedido* | **NOMBRE:** *Intento de anulación de pedido en estado Atendido o Anulado* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el sistema no permita la anulación de pedidos en estado "Atendido" o "Anulado", verificando que la opción de anulación no esté disponible para dichos registros.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario se encuentra en el módulo Pedidos con el listado de pedidos visible.* | |
| *El usuario localiza un pedido con estado "Atendido" o "Anulado".* | *El sistema no muestra disponible la opción de anulación para ese pedido, impidiendo cualquier intento de anulación de un pedido en estado "Atendido" o "Anulado".* |

##### j) PP10 – Filtrado de pedidos por rango de fechas, cliente y estado

| **IDENTIFICADOR:** | *PP10* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP01 – Registrar pedido* | **NOMBRE:** *Filtrado de pedidos por rango de fechas, cliente y estado* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el sistema permita filtrar correctamente el listado de pedidos al aplicar criterios de búsqueda como rango de fechas, cliente y estado del pedido.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario se encuentra en el módulo Pedidos con el listado de pedidos visible.* | |
| *El usuario aplica filtros por rango de fechas, cliente y estado (ej: Activo).* | *El sistema filtra el listado y muestra únicamente los registros que cumplen los criterios seleccionados.* |

---

### 7. UC-06 – GESTIONAR CLIENTES

#### 7.1. CASOS DE PRUEBA

##### a) CP01 – Registrar cliente

| **IDENTIFICADOR:** *CP01* | **NOMBRE:** *Registrar cliente* |
| --- | --- |
| **Requerimiento vinculado:** *RF-CLI-006* | **Prioridad de prueba:** *Alta* |
| **Documentos de visualización asociados:** *Documento de Especificación de Requerimientos de Software — Sistema Punto de Venta Comercial.* |
| **Precondición:** *El usuario debe estar autenticado con credenciales válidas y contar con permisos de creación en el módulo Clientes, conforme a la configuración RBAC de su rol.* |
| **Descripción:** *El sistema debe permitir registrar nuevos clientes en el directorio. El formulario de registro incluye: Tipo de Documento (DNI, RUC u otros), Número de Documento, Razón Social, Dirección y Teléfono de Contacto. El sistema ajusta la validación del Número de Documento según el tipo seleccionado (8 dígitos para DNI, 11 dígitos para RUC) con retroalimentación visual en tiempo real. No se permite registrar clientes con el mismo número de documento que uno ya existente.* |
| **DATOS DE ENTRADA** |
| **CAMPO/DATO** | **TIPO DE DATO** |
| *Tipo de Documento (DNI, RUC u otros)* | *Cadena (selección)* |
| *Número de Documento* | *Numérico* |
| *Razón Social* | *Cadena* |
| *Dirección* | *Cadena* |
| *Teléfono de Contacto* | *Cadena* |
| **ESCENARIO DE PRUEBAS** *EP01: Registro exitoso de nuevo cliente con datos válidos* *EP02: Registro fallido por campos obligatorios vacíos* *EP03: Registro fallido por número de documento duplicado* *EP04: Registro fallido por formato inválido de número de documento* |
| **CRITERIOS DE ACEPTACIÓN** El sistema permite registrar un nuevo cliente con datos completos y válidos. El sistema ajusta la validación del Número de Documento según el Tipo de Documento (8 dígitos para DNI, 11 dígitos para RUC). Si ya existe un cliente con el mismo número de documento, el sistema muestra: "Ya existe un cliente registrado con este número de documento." e impide el registro duplicado. Si no se completan los campos obligatorios (Tipo de Documento, Número de Documento y Razón Social), el sistema muestra mensajes de validación y no permite guardar. Si el Número de Documento no cumple el formato válido, el sistema muestra una advertencia y no permite continuar. El nuevo cliente queda registrado y disponible para su uso en los módulos de Ventas, POS y Pedidos del tenant. |

##### b) CP02 – Editar cliente

| **IDENTIFICADOR:** *CP02* | **NOMBRE:** *Editar cliente* |
| --- | --- |
| **Requerimiento vinculado:** *RF-CLI-006* | **Prioridad de prueba:** *Alta* |
| **Documentos de visualización asociados:** *Documento de Especificación de Requerimientos de Software — Sistema Punto de Venta Comercial.* |
| **Precondición:** *El usuario debe estar autenticado con permisos de edición en el módulo Clientes y debe existir al menos un cliente registrado.* |
| **Descripción:** *El sistema debe permitir al usuario editar los datos de un cliente existente seleccionando el ícono de edición en el listado. El sistema carga el formulario de edición con los datos actuales y valida que los campos obligatorios estén completos con retroalimentación visual en tiempo real. Las modificaciones realizadas quedan guardadas y son reflejadas de forma inmediata en todo el sistema.* |
| **DATOS DE ENTRADA** |
| **CAMPO/DATO** | **TIPO DE DATO** |
| *Razón Social* | *Cadena* |
| *Dirección* | *Cadena* |
| *Teléfono de Contacto* | *Cadena* |
| **ESCENARIO DE PRUEBAS** *EP01: Edición exitosa de datos de cliente existente* *EP02: Edición fallida con campos obligatorios vacíos* |
| **CRITERIOS DE ACEPTACIÓN** Al seleccionar el ícono de edición, el sistema carga el formulario de edición con los datos actuales del cliente. El sistema valida que los campos obligatorios estén completos con retroalimentación visual en tiempo real. Al hacer clic en "Guardar Cambios", el sistema valida, actualiza el registro en la base de datos del tenant y regresa al listado con la información actualizada de forma inmediata. |

##### c) CP03 – Buscar cliente

| **IDENTIFICADOR:** *CP03* | **NOMBRE:** *Buscar cliente* |
| --- | --- |
| **Requerimiento vinculado:** *RF-CLI-006* | **Prioridad de prueba:** *Media* |
| **Documentos de visualización asociados:** *Documento de Especificación de Requerimientos de Software — Sistema Punto de Venta Comercial.* |
| **Precondición:** *El usuario debe estar autenticado con permisos de acceso al módulo Clientes.* |
| **Descripción:** *El sistema debe permitir buscar clientes en tiempo real por nombre, razón social o número de documento (DNI o RUC) con autocompletado, filtrando el listado conforme el usuario escribe. Si la búsqueda no arroja resultados, el sistema muestra el listado vacío o un mensaje indicando que no se encontraron registros.* |
| **DATOS DE ENTRADA** |
| **CAMPO/DATO** | **TIPO DE DATO** |
| *Texto de búsqueda (nombre, razón social o número de documento)* | *Cadena* |
| **ESCENARIO DE PRUEBAS** *EP01: Búsqueda exitosa de cliente por nombre, razón social o número de documento* *EP02: Búsqueda sin resultados* |
| **CRITERIOS DE ACEPTACIÓN** El sistema realiza una búsqueda en tiempo real por nombre, razón social o número de documento (DNI o RUC) con autocompletado, filtrando el listado conforme el usuario escribe. Si la búsqueda no arroja resultados, el sistema muestra el listado vacío o un mensaje indicando que no se encontraron registros. |

---

#### 7.2. PROCEDIMIENTO DE PRUEBA

##### a) PP01 – Registro exitoso de nuevo cliente con datos válidos

| **IDENTIFICADOR:** | *PP01* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP01 – Registrar cliente* | **NOMBRE:** *Registro exitoso de nuevo cliente con datos válidos* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida el proceso de registro exitoso de un nuevo cliente en el sistema, verificando que el usuario pueda completar el formulario con los datos requeridos, que el sistema valide correctamente los campos según el tipo de documento seleccionado, y que el cliente quede registrado correctamente.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario hace clic en Clientes en el menú lateral o accede desde el acceso rápido "Ver Clientes" del Dashboard.* | *El sistema presenta el módulo con los indicadores: Total, Activos e Inactivos.* |
| *El usuario hace clic en "Nuevo".* | *El sistema carga el formulario de registro con los campos: Tipo de Documento, Número de Documento, Razón Social, Dirección y Teléfono de Contacto.* |
| *El usuario selecciona el Tipo de Documento (ej: RUC).* | *El sistema ajusta la validación del campo Número de Documento (11 dígitos para RUC) con retroalimentación visual en tiempo real.* |
| *El usuario ingresa el Número de Documento.* | *El sistema valida el formato según el tipo seleccionado.* |
| *El usuario ingresa la Razón Social.* | *El sistema valida que el campo no esté vacío y cumpla con el formato esperado.* |
| *El usuario ingresa la Dirección y Teléfono de Contacto.* | *El sistema registra los datos ingresados.* |
| *El usuario hace clic en "Guardar".* | *El sistema valida los campos obligatorios, registra el cliente en la base de datos del tenant y lo muestra en el listado. El nuevo cliente queda disponible para su uso en los módulos de Ventas, POS y Pedidos.* |

##### b) PP02 – Registro fallido por campos obligatorios vacíos

| **IDENTIFICADOR:** | *PP02* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP01 – Registrar cliente* | **NOMBRE:** *Registro fallido por campos obligatorios vacíos* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el sistema no permita registrar un nuevo cliente cuando los campos obligatorios (Tipo de Documento, Número de Documento y Razón Social) no han sido completados.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario se encuentra en el formulario de registro de nuevo cliente.* | |
| *El usuario selecciona el Tipo de Documento, pero no completa el Número de Documento ni la Razón Social.* | |
| *El usuario intenta hacer clic en "Guardar".* | *El sistema muestra mensajes de validación indicando que los campos obligatorios deben ser completados y no permite guardar el registro.* |

##### c) PP03 – Registro fallido por número de documento duplicado

| **IDENTIFICADOR:** | *PP03* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP01 – Registrar cliente* | **NOMBRE:** *Registro fallido por número de documento duplicado* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el sistema detecte la duplicidad de número de documento e impida el registro de un nuevo cliente con el mismo número de documento que uno ya existente en el sistema.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario se encuentra en el formulario de registro de nuevo cliente con todos los campos completados.* | |
| *El usuario ingresa en el campo "Número de Documento" un número ya asociado a un cliente existente en el sistema.* | |
| *El usuario hace clic en "Guardar".* | *El sistema muestra el mensaje: "Ya existe un cliente registrado con este número de documento." e impide el registro duplicado.* |

##### d) PP04 – Registro fallido por formato inválido de número de documento

| **IDENTIFICADOR:** | *PP04* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP01 – Registrar cliente* | **NOMBRE:** *Registro fallido por formato inválido de número de documento* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el sistema muestre una advertencia con retroalimentación visual en tiempo real cuando el Número de Documento ingresado no cumple el formato válido según el Tipo de Documento seleccionado (ej: DNI con menos o más de 8 dígitos, RUC con menos o más de 11 dígitos), e impida guardar el registro hasta que se corrija el valor.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario se encuentra en el formulario de registro de nuevo cliente.* | |
| *El usuario selecciona el Tipo de Documento "DNI" e ingresa en el campo "Número de Documento" un valor con menos de 8 dígitos (ej: "1234567").* | *El sistema muestra una advertencia con retroalimentación visual en tiempo real indicando que el Número de Documento no cumple el formato válido (8 dígitos para DNI), y no permite guardar el registro.* |

##### e) PP05 – Edición exitosa de datos de cliente existente

| **IDENTIFICADOR:** | *PP05* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP02 – Editar cliente* | **NOMBRE:** *Edición exitosa de datos de cliente existente* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el sistema permita editar correctamente los datos de un cliente existente y que los cambios queden guardados y reflejados de forma inmediata en todo el sistema.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario se encuentra en el módulo Clientes con el listado visible.* | |
| *El usuario selecciona el ícono de edición en un cliente del listado.* | *El sistema carga el formulario de edición con los datos actuales del cliente.* |
| *El usuario modifica el campo "Dirección" o "Teléfono de Contacto".* | *El sistema valida que los campos obligatorios estén completos con retroalimentación visual en tiempo real.* |
| *El usuario hace clic en "Guardar Cambios".* | *El sistema valida, actualiza el registro en la base de datos del tenant y regresa al listado con la información actualizada de forma inmediata.* |

##### f) PP06 – Edición fallida con campos obligatorios vacíos

| **IDENTIFICADOR:** | *PP06* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP02 – Editar cliente* | **NOMBRE:** *Edición fallida con campos obligatorios vacíos* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el sistema no permita guardar la edición de un cliente cuando un campo obligatorio ha sido vaciado, mostrando el mensaje de validación correspondiente.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario se encuentra en el formulario de edición de un cliente existente.* | |
| *El usuario elimina el contenido del campo "Razón Social" dejándolo vacío.* | *El sistema muestra un mensaje de validación con retroalimentación visual indicando que el campo es obligatorio y no permite guardar los cambios.* |

##### g) PP07 – Búsqueda exitosa de cliente por nombre, razón social o número de documento

| **IDENTIFICADOR:** | *PP07* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP03 – Buscar cliente* | **NOMBRE:** *Búsqueda exitosa de cliente por nombre, razón social o número de documento* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el sistema realice una búsqueda en tiempo real con autocompletado al ingresar texto en el campo de búsqueda del módulo Clientes, filtrando el listado por nombre, razón social o número de documento (DNI o RUC) conforme el usuario escribe.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario se encuentra en el módulo Clientes con el listado visible.* | |
| *El usuario ingresa texto en el campo de búsqueda (ej: parte de la razón social o número de RUC).* | *El sistema realiza una búsqueda en tiempo real con autocompletado, filtrando el listado conforme el usuario escribe y mostrando únicamente los clientes que coinciden con el criterio ingresado.* |

##### h) PP08 – Búsqueda sin resultados

| **IDENTIFICADOR:** | *PP08* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP03 – Buscar cliente* | **NOMBRE:** *Búsqueda sin resultados* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida el comportamiento del sistema cuando la búsqueda en el módulo Clientes no arroja ningún resultado coincidente con el criterio ingresado.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El usuario se encuentra en el módulo Clientes con el listado visible.* | |
| *El usuario ingresa en el campo de búsqueda un texto que no corresponde a ningún cliente registrado en el sistema.* | *El sistema muestra el listado vacío o un mensaje indicando que no se encontraron registros que coincidan con el criterio de búsqueda.* |

---

### 8. UC-07 – GESTIONAR USUARIOS

#### 8.1. CASOS DE PRUEBA

##### a) CP01 – Registrar usuario en el sistema POS

| **IDENTIFICADOR:** *CP01* | **NOMBRE:** *Registrar usuario en el sistema POS* |
| --- | --- |
| **Requerimiento vinculado:** *RF-ADM-007* | **Prioridad de prueba:** *Alta* |
| **Documentos de visualización asociados:** *Documento de Especificación de Requerimientos de Software — Sistema Punto de Venta Comercial.* |
| **Precondición:** *El usuario debe estar autenticado con el rol de Administrador para acceder al módulo de Administración > Acceso y Permisos > Usuarios y Roles.* |
| **Descripción:** *El sistema debe permitir al Administrador crear nuevos usuarios del sistema POS con nombre único, contraseña, clave de venta opcional y estado (Habilitado / Deshabilitado), asignándoles un rol. El sistema valida en tiempo real que el nombre de usuario no exista previamente y cumpla el formato requerido. El nombre de usuario es inmutable una vez creado.* |
| **DATOS DE ENTRADA** |
| **CAMPO/DATO** | **TIPO DE DATO** |
| *Nombre de usuario (único, inmutable)* | *Cadena* |
| *Contraseña* | *Cadena* |
| *Clave de venta (opcional)* | *Cadena* |
| *Estado (Habilitado / Deshabilitado)* | *Caracter (selección)* |
| *Rol asignado* | *Cadena (selección)* |
| **ESCENARIO DE PRUEBAS** *EP01: Registro exitoso de nuevo usuario con datos válidos* *EP02: Registro fallido por nombre de usuario duplicado* *EP03: Registro fallido por campos obligatorios vacíos* |
| **CRITERIOS DE ACEPTACIÓN** El sistema permite registrar un nuevo usuario con nombre único, contraseña, estado y rol. El sistema valida en tiempo real que el nombre de usuario no exista previamente. Si el nombre de usuario ya existe, el sistema muestra: "Ya existe un usuario registrado con este nombre." e impide el registro duplicado. Si no se completan los campos obligatorios (nombre, contraseña, estado y rol), el sistema muestra validaciones y no permite guardar. El nombre de usuario es inmutable una vez creado y no puede modificarse en ediciones posteriores. |

##### b) CP02 – Editar usuario en el sistema POS

| **IDENTIFICADOR:** *CP02* | **NOMBRE:** *Editar usuario en el sistema POS* |
| --- | --- |
| **Requerimiento vinculado:** *RF-ADM-007* | **Prioridad de prueba:** *Alta* |
| **Documentos de visualización asociados:** *Documento de Especificación de Requerimientos de Software — Sistema Punto de Venta Comercial.* |
| **Precondición:** *El Administrador debe estar autenticado y acceder a un usuario válido en Administración > Acceso y Permisos > Usuarios y Roles.* |
| **Descripción:** *El sistema debe permitir al Administrador editar los datos de un usuario existente del sistema POS, con la excepción de que el nombre de usuario es inmutable una vez creado y se presenta como no editable. Los campos habilitados para edición son: contraseña, clave de venta, estado y rol asignado. Los cambios se aplican de forma inmediata.* |
| **DATOS DE ENTRADA** |
| **CAMPO/DATO** | **TIPO DE DATO** |
| *Contraseña* | *Cadena* |
| *Clave de venta (opcional)* | *Cadena* |
| *Estado (Habilitado / Deshabilitado)* | *Caracter (selección)* |
| *Rol asignado* | *Cadena (selección)* |
| **ESCENARIO DE PRUEBAS** *EP01: Edición exitosa de usuario existente* *EP02: Edición fallida con campos obligatorios vacíos* *EP03: Verificación de inmutabilidad del nombre de usuario en edición* |
| **CRITERIOS DE ACEPTACIÓN** El sistema permite editar los campos habilitados (contraseña, clave de venta, estado, rol) de un usuario existente. El campo "Nombre de usuario" se presenta como no editable (inmutable). El sistema muestra errores si los campos obligatorios están vacíos. Los cambios se aplican de forma inmediata al confirmar con "Guardar Cambios". |

##### c) CP03 – Listar usuarios del sistema POS

| **IDENTIFICADOR:** *CP03* | **NOMBRE:** *Listar usuarios del sistema POS* |
| --- | --- |
| **Requerimiento vinculado:** *RF-ADM-007* | **Prioridad de prueba:** *Media* |
| **Documentos de visualización asociados:** *Documento de Especificación de Requerimientos de Software — Sistema Punto de Venta Comercial.* |
| **Precondición:** *El Administrador debe estar autenticado en el módulo de Administración > Acceso y Permisos > Usuarios y Roles.* |
| **Descripción:** *El sistema debe mostrar el listado de usuarios registrados en el sistema POS con sus datos correspondientes.* |
| **DATOS DE ENTRADA** |
| **CAMPO/DATO** | **TIPO DE DATO** |
| *Sin datos de entrada adicionales* | |
| **ESCENARIO DE PRUEBAS** *EP01: Listado completo de usuarios registrados* |
| **CRITERIOS DE ACEPTACIÓN** El sistema carga y muestra el listado completo de usuarios registrados en el sistema POS. |

---

#### 8.2. PROCEDIMIENTO DE PRUEBA

##### a) PP01 – Registro exitoso de nuevo usuario con datos válidos

| **IDENTIFICADOR:** | *PP01* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP01 – Registrar usuario en el sistema POS* | **NOMBRE:** *Registro exitoso de nuevo usuario con datos válidos* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el Administrador pueda registrar correctamente un nuevo usuario del sistema POS con nombre único, contraseña, estado y rol asignado.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El Administrador accede a Administración > Acceso y Permisos > Usuarios y Roles.* | *El sistema presenta el listado de usuarios registrados y el listado de roles disponibles.* |
| *El Administrador hace clic en "Nuevo Usuario".* | *El sistema carga el formulario con los campos: Nombre de usuario, Contraseña, Clave de venta (opcional), Estado y Rol asignado.* |
| *El Administrador ingresa el nombre de usuario.* | *El sistema valida en tiempo real que el nombre de usuario no exista previamente y cumpla el formato requerido.* |
| *El Administrador ingresa la contraseña y, opcionalmente, la clave de venta.* | *El sistema registra los datos ingresados.* |
| *El Administrador selecciona el estado (Habilitado) y el rol asignado al usuario.* | *El sistema registra la selección.* |
| *El Administrador hace clic en "Guardar".* | *El sistema valida los campos obligatorios, registra el nuevo usuario en la base de datos del tenant y lo presenta en el listado.* |

##### b) PP02 – Registro fallido por nombre de usuario duplicado

| **IDENTIFICADOR:** | *PP02* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP01 – Registrar usuario en el sistema POS* | **NOMBRE:** *Registro fallido por nombre de usuario duplicado* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el sistema detecte y rechace el registro de un nuevo usuario cuando el nombre de usuario ingresado ya existe en el sistema POS.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El Administrador se encuentra en el formulario de registro de nuevo usuario.* | |
| *El Administrador ingresa en el campo "Nombre de usuario" un nombre que ya está registrado en el sistema.* | *El sistema valida en tiempo real que el nombre de usuario ya existe.* |
| *El Administrador completa los demás campos y hace clic en "Guardar".* | *El sistema muestra el mensaje: "Ya existe un usuario registrado con este nombre." e impide el registro duplicado.* |

##### c) PP03 – Registro fallido por campos obligatorios vacíos

| **IDENTIFICADOR:** | *PP03* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP01 – Registrar usuario en el sistema POS* | **NOMBRE:** *Registro fallido por campos obligatorios vacíos* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el sistema no permita guardar el registro de un nuevo usuario cuando los campos obligatorios (nombre, contraseña, estado y rol) no han sido completados.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El Administrador se encuentra en el formulario de registro de nuevo usuario.* | |
| *El Administrador no completa el campo "Contraseña".* | |
| *El Administrador intenta hacer clic en "Guardar".* | *El sistema muestra mensajes de validación indicando que los campos obligatorios deben ser completados y no permite guardar el registro.* |

##### d) PP04 – Edición exitosa de usuario existente

| **IDENTIFICADOR:** | *PP04* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP02 – Editar usuario en el sistema POS* | **NOMBRE:** *Edición exitosa de usuario existente* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el Administrador pueda editar correctamente los datos habilitados de un usuario existente del sistema POS y que los cambios se apliquen de forma inmediata.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El Administrador se encuentra en Administración > Acceso y Permisos > Usuarios y Roles con el listado de usuarios visible.* | |
| *El Administrador selecciona el ícono de edición en un usuario del listado.* | *El sistema carga el formulario de edición. El campo "Nombre de usuario" se presenta como no editable (inmutable).* |
| *El Administrador modifica el estado del usuario (ej: de Habilitado a Deshabilitado) o el rol asignado.* | *El sistema valida los cambios en tiempo real.* |
| *El Administrador hace clic en "Guardar Cambios".* | *El sistema actualiza el registro y aplica los cambios de forma inmediata.* |

##### e) PP05 – Edición fallida con campos obligatorios vacíos

| **IDENTIFICADOR:** | *PP05* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP02 – Editar usuario en el sistema POS* | **NOMBRE:** *Edición fallida con campos obligatorios vacíos* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el sistema no permita guardar la edición de un usuario cuando un campo obligatorio ha sido vaciado en el formulario de edición.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El Administrador se encuentra en el formulario de edición de un usuario existente.* | |
| *El Administrador elimina el contenido del campo "Contraseña".* | *El sistema muestra un mensaje de validación indicando que el campo es obligatorio y no permite guardar los cambios.* |

##### f) PP06 – Verificación de inmutabilidad del nombre de usuario en edición

| **IDENTIFICADOR:** | *PP06* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP02 – Editar usuario en el sistema POS* | **NOMBRE:** *Verificación de inmutabilidad del nombre de usuario en edición* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba verifica que el campo "Nombre de usuario" se presente como no editable (inmutable) en el formulario de edición de un usuario del sistema POS, de acuerdo a la restricción definida en el caso de uso.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El Administrador selecciona el ícono de edición en un usuario del listado.* | *El sistema carga el formulario de edición. El campo "Nombre de usuario" se presenta con estado deshabilitado (solo lectura / no editable), impidiendo que el Administrador modifique el nombre de usuario.* |

##### g) PP07 – Listado completo de usuarios registrados

| **IDENTIFICADOR:** | *PP07* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP03 – Listar usuarios del sistema POS* | **NOMBRE:** *Listado completo de usuarios registrados* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el sistema cargue y muestre correctamente el listado completo de usuarios registrados en el sistema POS al acceder al módulo de Administración > Acceso y Permisos > Usuarios y Roles.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El Administrador accede a Administración > Acceso y Permisos > Usuarios y Roles.* | *El sistema presenta el listado de usuarios registrados en el sistema POS con sus datos correspondientes (nombre de usuario, estado, rol asignado).* |

---

### 9. UC-08 – GESTIONAR ROLES

#### 9.1. CASOS DE PRUEBA

##### a) CP01 – Registrar rol

| **IDENTIFICADOR:** *CP01* | **NOMBRE:** *Registrar rol* |
| --- | --- |
| **Requerimiento vinculado:** *RF-ADM-008* | **Prioridad de prueba:** *Alta* |
| **Documentos de visualización asociados:** *Documento de Especificación de Requerimientos de Software — Sistema Punto de Venta Comercial.* |
| **Precondición:** *El Administrador debe estar autenticado y acceder a Administración > Acceso y Permisos > Permisos por Rol.* |
| **Descripción:** *El sistema debe permitir al Administrador crear nuevos roles con nombre único, descripción y estado, asignándoles permisos por módulo mediante una matriz de permisos (Acceso, Creación, Edición, Anulación, Envío a SUNAT y otros disponibles). El sistema valida que el nombre del rol no esté duplicado y que los campos obligatorios estén completos.* |
| **DATOS DE ENTRADA** |
| **CAMPO/DATO** | **TIPO DE DATO** |
| *Nombre del rol (único)* | *Cadena* |
| *Descripción* | *Cadena* |
| *Estado (Activo / Inactivo)* | *Caracter (selección)* |
| *Permisos por módulo (Acceso, Creación, Edición, Anulación, Envío a SUNAT, etc.)* | *Booleano (matriz de selección)* |
| **ESCENARIO DE PRUEBAS** *EP01: Registro exitoso de nuevo rol con permisos asignados* *EP02: Registro fallido por nombre de rol duplicado* *EP03: Registro fallido por campos obligatorios vacíos* |
| **CRITERIOS DE ACEPTACIÓN** El sistema permite registrar un nuevo rol con nombre único, descripción, estado y permisos por módulo. Si el nombre del rol ya existe, el sistema muestra: "Ya existe un rol registrado con este nombre." e impide el registro duplicado. Si no se completan los campos obligatorios (nombre del rol y estado), el sistema muestra validaciones y no permite guardar. Los cambios en los permisos de un rol se aplican de forma inmediata a todos los usuarios que tienen ese rol asignado. |

##### b) CP02 – Editar rol y permisos

| **IDENTIFICADOR:** *CP02* | **NOMBRE:** *Editar rol y permisos* |
| --- | --- |
| **Requerimiento vinculado:** *RF-ADM-008* | **Prioridad de prueba:** *Alta* |
| **Documentos de visualización asociados:** *Documento de Especificación de Requerimientos de Software — Sistema Punto de Venta Comercial.* |
| **Precondición:** *El Administrador debe estar autenticado y acceder a un rol existente en Administración > Acceso y Permisos > Permisos por Rol.* |
| **Descripción:** *El sistema debe permitir al Administrador editar el nombre, descripción, estado y permisos de un rol existente. Los cambios de permisos se aplican de forma inmediata a todos los usuarios que tienen ese rol asignado. El sistema valida que el nuevo nombre no coincida con otro ya existente y que los campos obligatorios estén completos.* |
| **DATOS DE ENTRADA** |
| **CAMPO/DATO** | **TIPO DE DATO** |
| *Nombre del rol* | *Cadena* |
| *Descripción* | *Cadena* |
| *Estado (Activo / Inactivo)* | *Caracter (selección)* |
| *Permisos por módulo (Acceso, Creación, Edición, Anulación, Envío a SUNAT, etc.)* | *Booleano (matriz de selección)* |
| **ESCENARIO DE PRUEBAS** *EP01: Edición exitosa de rol existente y sus permisos* *EP02: Edición fallida por nombre de rol duplicado* *EP03: Edición fallida por campos obligatorios vacíos* |
| **CRITERIOS DE ACEPTACIÓN** El sistema actualiza correctamente los datos del rol si son válidos. El sistema valida que el nombre del rol sea único. Los cambios de permisos se aplican de forma inmediata a todos los usuarios con ese rol. El sistema muestra mensaje de éxito o error según el caso. |

##### c) CP03 – Listar roles

| **IDENTIFICADOR:** *CP03* | **NOMBRE:** *Listar roles* |
| --- | --- |
| **Requerimiento vinculado:** *RF-ADM-008* | **Prioridad de prueba:** *Media* |
| **Documentos de visualización asociados:** *Documento de Especificación de Requerimientos de Software — Sistema Punto de Venta Comercial.* |
| **Precondición:** *El Administrador debe estar autenticado en el módulo de Administración > Acceso y Permisos > Permisos por Rol.* |
| **Descripción:** *El sistema debe mostrar el listado de roles registrados con sus nombres, descripciones y estados.* |
| **DATOS DE ENTRADA** |
| **CAMPO/DATO** | **TIPO DE DATO** |
| *Sin datos de entrada adicionales* | |
| **ESCENARIO DE PRUEBAS** *EP01: Listado completo de roles registrados* |
| **CRITERIOS DE ACEPTACIÓN** El sistema muestra todos los roles registrados correctamente con sus nombres, descripciones y estados. |

---

#### 9.2. PROCEDIMIENTO DE PRUEBA

##### a) PP01 – Registro exitoso de nuevo rol con permisos asignados

| **IDENTIFICADOR:** | *PP01* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP01 – Registrar rol* | **NOMBRE:** *Registro exitoso de nuevo rol con permisos asignados* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el Administrador pueda registrar correctamente un nuevo rol en el sistema POS con nombre único, descripción, estado y permisos por módulo seleccionados en la matriz de permisos.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El Administrador accede a Administración > Acceso y Permisos > Permisos por Rol.* | *El sistema presenta el listado de roles con sus nombres, descripciones y estados.* |
| *El Administrador hace clic en "Nuevo Rol".* | *El sistema carga el formulario con los campos: Nombre del rol, Descripción, Estado y la matriz de permisos por módulo (Acceso, Creación, Edición, Anulación, Envío a SUNAT y otros disponibles).* |
| *El Administrador ingresa el nombre del rol.* | *El sistema valida que el nombre del rol no exista previamente.* |
| *El Administrador ingresa la descripción y selecciona el estado (Activo).* | |
| *El Administrador selecciona los permisos correspondientes en la matriz de permisos por módulo.* | *El sistema registra las selecciones realizadas.* |
| *El Administrador hace clic en "Guardar".* | *El sistema valida los datos, registra el nuevo rol con sus permisos y lo presenta en el listado.* |

##### b) PP02 – Registro fallido por nombre de rol duplicado

| **IDENTIFICADOR:** | *PP02* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP01 – Registrar rol* | **NOMBRE:** *Registro fallido por nombre de rol duplicado* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el sistema detecte y rechace el registro de un nuevo rol cuando el nombre del rol ingresado ya existe en el sistema POS.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El Administrador se encuentra en el formulario de registro de nuevo rol.* | |
| *El Administrador ingresa en el campo "Nombre del rol" un nombre que ya está registrado en el sistema.* | *El sistema valida que el nombre del rol ya existe.* |
| *El Administrador completa los demás campos y hace clic en "Guardar".* | *El sistema muestra el mensaje: "Ya existe un rol registrado con este nombre." e impide el registro duplicado.* |

##### c) PP03 – Registro fallido por campos obligatorios vacíos

| **IDENTIFICADOR:** | *PP03* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP01 – Registrar rol* | **NOMBRE:** *Registro fallido por campos obligatorios vacíos* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el sistema no permita guardar el registro de un nuevo rol cuando los campos obligatorios (nombre del rol y estado) no han sido completados.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El Administrador se encuentra en el formulario de registro de nuevo rol.* | |
| *El Administrador no completa el campo "Nombre del rol".* | |
| *El Administrador intenta hacer clic en "Guardar".* | *El sistema muestra mensajes de validación indicando que los campos obligatorios deben ser completados y no permite guardar el registro.* |

##### d) PP04 – Edición exitosa de rol existente y sus permisos

| **IDENTIFICADOR:** | *PP04* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP02 – Editar rol y permisos* | **NOMBRE:** *Edición exitosa de rol existente y sus permisos* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el Administrador pueda editar correctamente los datos y los permisos de un rol existente en el sistema POS, y que los cambios de permisos se apliquen de forma inmediata a todos los usuarios que tienen ese rol asignado.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El Administrador accede a Administración > Acceso y Permisos > Permisos por Rol con el listado de roles visible.* | |
| *El Administrador selecciona el ícono de edición en un rol del listado.* | *El sistema carga el formulario de edición con los datos actuales y la matriz de permisos asignados.* |
| *El Administrador modifica la descripción del rol y agrega o quita permisos en la matriz.* | *El sistema registra los cambios en tiempo real.* |
| *El Administrador hace clic en "Guardar Cambios".* | *El sistema actualiza el registro, aplica los cambios de permisos de forma inmediata a todos los usuarios con ese rol, y regresa al listado actualizado.* |

##### e) PP05 – Edición fallida por nombre de rol duplicado

| **IDENTIFICADOR:** | *PP05* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP02 – Editar rol y permisos* | **NOMBRE:** *Edición fallida por nombre de rol duplicado* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el sistema no permita guardar la edición de un rol cuando el nuevo nombre ingresado ya está registrado en otro rol del sistema.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El Administrador se encuentra en el formulario de edición de un rol existente.* | |
| *El Administrador cambia el campo "Nombre del rol" por un nombre que ya existe en otro rol del sistema.* | |
| *El Administrador hace clic en "Guardar Cambios".* | *El sistema muestra el mensaje: "Ya existe un rol registrado con este nombre." e impide guardar la edición.* |

##### f) PP06 – Edición fallida por campos obligatorios vacíos

| **IDENTIFICADOR:** | *PP06* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP02 – Editar rol y permisos* | **NOMBRE:** *Edición fallida por campos obligatorios vacíos* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el sistema no permita guardar la edición de un rol cuando un campo obligatorio ha sido vaciado en el formulario de edición.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El Administrador se encuentra en el formulario de edición de un rol existente.* | |
| *El Administrador elimina el contenido del campo "Nombre del rol".* | *El sistema muestra un mensaje de validación indicando que el campo es obligatorio y no permite guardar los cambios.* |

##### g) PP07 – Listado completo de roles registrados

| **IDENTIFICADOR:** | *PP07* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP03 – Listar roles* | **NOMBRE:** *Listado completo de roles registrados* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el sistema cargue y muestre correctamente el listado de roles registrados en el sistema POS al acceder al módulo de Administración > Acceso y Permisos > Permisos por Rol.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El Administrador accede a Administración > Acceso y Permisos > Permisos por Rol.* | *El sistema presenta el listado de roles registrados con sus nombres, descripciones y estados.* |

---

### 10. UC-09 – GESTIONAR FORMULARIOS

#### 10.1. CASOS DE PRUEBA

##### a) CP01 – Configurar campos de formularios por módulo y rol

| **IDENTIFICADOR:** *CP01* | **NOMBRE:** *Configurar campos de formularios por módulo y rol* |
| --- | --- |
| **Requerimiento vinculado:** *RF-SADM-009* | **Prioridad de prueba:** *Alta* |
| **Documentos de visualización asociados:** *Documento de Especificación de Requerimientos de Software — Sistema Punto de Venta Comercial.* |
| **Precondición:** *El Administrador debe estar autenticado y acceder a Administración > Acceso y Permisos > Campos de Formularios.* |
| **Descripción:** *El sistema debe permitir al Administrador configurar los campos de los formularios de cada módulo (Pedidos, Ventas, Clientes) definiendo para cada campo su visibilidad (visible o no), obligatoriedad (requerido o no) y editabilidad (editable o solo lectura), según el rol del usuario. Los cambios se aplican de forma inmediata sin requerir reinicio ni acciones adicionales.* |
| **DATOS DE ENTRADA** |
| **CAMPO/DATO** | **TIPO DE DATO** |
| *Módulo a configurar (Pedidos, Ventas o Clientes)* | *Cadena (selección)* |
| *Rol al que aplicará la configuración* | *Cadena (selección)* |
| *Visibilidad del campo (visible / no visible)* | *Booleano* |
| *Obligatoriedad del campo (requerido / no requerido)* | *Booleano* |
| *Editabilidad del campo (editable / solo lectura)* | *Booleano* |
| **ESCENARIO DE PRUEBAS** *EP01: Configuración exitosa de visibilidad de campo de formulario* *EP02: Configuración exitosa de obligatoriedad de campo de formulario* *EP03: Configuración exitosa de editabilidad de campo de formulario* *EP04: Verificación de aplicación inmediata de configuración de formularios* |
| **CRITERIOS DE ACEPTACIÓN** El Administrador puede seleccionar el módulo (Pedidos, Ventas o Clientes) y el rol al que aplicará la configuración. El sistema carga la lista de campos disponibles en el formulario del módulo seleccionado. El Administrador puede configurar visibilidad, obligatoriedad y editabilidad para cada campo. Al hacer clic en "Guardar", el sistema aplica la configuración de forma inmediata. Los usuarios con el rol configurado verán los formularios con los campos según las propiedades definidas. Los cambios no requieren reinicio ni acciones adicionales. |

---

#### 10.2. PROCEDIMIENTO DE PRUEBA

##### a) PP01 – Configuración exitosa de visibilidad de campo de formulario

| **IDENTIFICADOR:** | *PP01* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP01 – Configurar campos de formularios por módulo y rol* | **NOMBRE:** *Configuración exitosa de visibilidad de campo de formulario* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el Administrador pueda configurar correctamente la visibilidad de un campo de un formulario para un rol específico, y que el cambio se aplique de forma inmediata.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El Administrador accede a Administración > Acceso y Permisos > Campos de Formularios.* | *El sistema presenta la interfaz de configuración, permitiendo seleccionar el módulo y el rol a configurar.* |
| *El Administrador selecciona el módulo "Pedidos" y el rol "Cajero".* | *El sistema carga la lista de campos disponibles en el formulario del módulo seleccionado.* |
| *El Administrador deshabilita la visibilidad del campo "Dirección" para el rol "Cajero".* | *El sistema registra la configuración seleccionada.* |
| *El Administrador hace clic en "Guardar".* | *El sistema aplica la configuración de forma inmediata. Los usuarios con rol "Cajero" ya no verán el campo "Dirección" en el formulario de Pedidos.* |

##### b) PP02 – Configuración exitosa de obligatoriedad de campo de formulario

| **IDENTIFICADOR:** | *PP02* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP01 – Configurar campos de formularios por módulo y rol* | **NOMBRE:** *Configuración exitosa de obligatoriedad de campo de formulario* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el Administrador pueda configurar correctamente la obligatoriedad de un campo de un formulario para un rol específico, y que el cambio se aplique de forma inmediata.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El Administrador accede a Administración > Acceso y Permisos > Campos de Formularios y selecciona el módulo y el rol a configurar.* | *El sistema carga la lista de campos disponibles en el formulario del módulo seleccionado.* |
| *El Administrador marca como "Requerido" el campo "Teléfono de Contacto" para el rol seleccionado.* | *El sistema registra la configuración seleccionada.* |
| *El Administrador hace clic en "Guardar".* | *El sistema aplica la configuración de forma inmediata. Los usuarios con el rol configurado verán el campo "Teléfono de Contacto" como obligatorio en el formulario del módulo seleccionado.* |

##### c) PP03 – Configuración exitosa de editabilidad de campo de formulario

| **IDENTIFICADOR:** | *PP03* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP01 – Configurar campos de formularios por módulo y rol* | **NOMBRE:** *Configuración exitosa de editabilidad de campo de formulario* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el Administrador pueda configurar correctamente la editabilidad de un campo de un formulario para un rol específico (editable o solo lectura), y que el cambio se aplique de forma inmediata.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El Administrador accede a Administración > Acceso y Permisos > Campos de Formularios y selecciona el módulo y el rol a configurar.* | *El sistema carga la lista de campos disponibles en el formulario del módulo seleccionado.* |
| *El Administrador configura el campo "Precio Unitario" como "Solo lectura" para el rol "Cajero".* | *El sistema registra la configuración seleccionada.* |
| *El Administrador hace clic en "Guardar".* | *El sistema aplica la configuración de forma inmediata. Los usuarios con rol "Cajero" verán el campo "Precio Unitario" como solo lectura en el formulario del módulo seleccionado.* |

##### d) PP04 – Verificación de aplicación inmediata de configuración de formularios

| **IDENTIFICADOR:** | *PP04* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP01 – Configurar campos de formularios por módulo y rol* | **NOMBRE:** *Verificación de aplicación inmediata de configuración de formularios* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba verifica que los cambios de configuración de campos de formularios realizados por el Administrador se apliquen de forma inmediata a los usuarios del rol afectado, sin necesidad de que cierren y vuelvan a iniciar sesión.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El Administrador ha guardado una nueva configuración de campos de formulario para el rol "Cajero" (ej: campo "Dirección" configurado como no visible).* | *El sistema aplica la configuración de forma inmediata.* |
| *Un usuario con rol "Cajero" que tiene sesión activa accede al formulario del módulo configurado.* | *El sistema presenta el formulario con los campos según las propiedades recién configuradas por el Administrador, sin necesidad de que el usuario cierre y vuelva a iniciar sesión.* |

---

### 11. UC-10 – GESTIONAR FORMAS DE PAGO

#### 11.1. CASOS DE PRUEBA

##### a) CP01 – Habilitar o deshabilitar formas de pago en el POS

| **IDENTIFICADOR:** *CP01* | **NOMBRE:** *Habilitar o deshabilitar formas de pago en el POS* |
| --- | --- |
| **Requerimiento vinculado:** *RF-SADM-010* | **Prioridad de prueba:** *Alta* |
| **Documentos de visualización asociados:** *Documento de Especificación de Requerimientos de Software — Sistema Punto de Venta Comercial.* |
| **Precondición:** *El Administrador debe estar autenticado y acceder a Administración > Punto de Venta > Formas de Pago.* |
| **Descripción:** *El sistema debe permitir al Administrador habilitar o deshabilitar las formas de pago disponibles en el módulo POS (ej.: Efectivo, American Express, BBVA Visa). Solo las formas de pago habilitadas aparecerán disponibles al momento de registrar un cobro en el POS. Los cambios se aplican de forma inmediata. Si el Administrador deshabilita todas las formas de pago, el sistema muestra una advertencia indicando que se requiere al menos una forma de pago habilitada para registrar cobros en el POS.* |
| **DATOS DE ENTRADA** |
| **CAMPO/DATO** | **TIPO DE DATO** |
| *Estado de la forma de pago (Habilitado / Deshabilitado)* | *Booleano* |
| **ESCENARIO DE PRUEBAS** *EP01: Habilitación exitosa de una forma de pago en el POS* *EP02: Deshabilitación exitosa de una forma de pago en el POS* *EP03: Intento de deshabilitar todas las formas de pago* |
| **CRITERIOS DE ACEPTACIÓN** El Administrador puede habilitar o deshabilitar cada forma de pago individualmente. Solo las formas de pago habilitadas aparecen disponibles en el POS al momento de registrar un cobro. Los cambios se aplican de forma inmediata al guardar. Si el Administrador intenta deshabilitar todas las formas de pago, el sistema muestra una advertencia indicando que se requiere al menos una forma de pago habilitada para registrar cobros en el POS. |

##### b) CP02 – Establecer orden de formas de pago

| **IDENTIFICADOR:** *CP02* | **NOMBRE:** *Establecer orden de formas de pago* |
| --- | --- |
| **Requerimiento vinculado:** *RF-SADM-010* | **Prioridad de prueba:** *Media* |
| **Documentos de visualización asociados:** *Documento de Especificación de Requerimientos de Software — Sistema Punto de Venta Comercial.* |
| **Precondición:** *El Administrador debe estar autenticado y acceder a Administración > Punto de Venta > Formas de Pago.* |
| **Descripción:** *El sistema debe permitir al Administrador establecer el orden de presentación de las formas de pago en el POS mediante arrastrar y soltar o número de orden. Los cambios se aplican de forma inmediata, mostrando las formas de pago en el orden configurado al momento de registrar un cobro.* |
| **DATOS DE ENTRADA** |
| **CAMPO/DATO** | **TIPO DE DATO** |
| *Orden de presentación de cada forma de pago* | *Numérico* |
| **ESCENARIO DE PRUEBAS** *EP01: Establecer orden de presentación de formas de pago* |
| **CRITERIOS DE ACEPTACIÓN** El Administrador puede establecer el orden de presentación mediante arrastrar y soltar o número de orden. Los cambios se aplican de forma inmediata. Las formas de pago habilitadas aparecen en el POS en el orden configurado. |

---

#### 11.2. PROCEDIMIENTO DE PRUEBA

##### a) PP01 – Habilitación exitosa de una forma de pago en el POS

| **IDENTIFICADOR:** | *PP01* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP01 – Habilitar o deshabilitar formas de pago en el POS* | **NOMBRE:** *Habilitación exitosa de una forma de pago en el POS* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el Administrador pueda habilitar correctamente una forma de pago deshabilitada en el módulo de configuración, y que dicha forma de pago quede disponible en el POS al momento de registrar un cobro.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El Administrador accede a Administración > Punto de Venta > Formas de Pago.* | *El sistema presenta el listado de formas de pago disponibles (ej.: Efectivo, American Express, BBVA Visa) con su estado (Habilitado / Deshabilitado) y orden de presentación.* |
| *El Administrador cambia el estado de una forma de pago deshabilitada a Habilitado (ej.: BBVA Visa).* | *El sistema registra el cambio de estado.* |
| *El Administrador hace clic en "Guardar".* | *El sistema aplica los cambios de forma inmediata. La forma de pago "BBVA Visa" ahora aparece disponible en el POS al momento de registrar un cobro.* |

##### b) PP02 – Deshabilitación exitosa de una forma de pago en el POS

| **IDENTIFICADOR:** | *PP02* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP01 – Habilitar o deshabilitar formas de pago en el POS* | **NOMBRE:** *Deshabilitación exitosa de una forma de pago en el POS* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el Administrador pueda deshabilitar correctamente una forma de pago habilitada en el módulo de configuración, y que dicha forma de pago ya no aparezca disponible en el POS al momento de registrar un cobro.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El Administrador accede a Administración > Punto de Venta > Formas de Pago.* | *El sistema presenta el listado de formas de pago con su estado actual.* |
| *El Administrador cambia el estado de una forma de pago habilitada a Deshabilitado (ej.: American Express). Existen otras formas de pago habilitadas.* | *El sistema registra el cambio de estado.* |
| *El Administrador hace clic en "Guardar".* | *El sistema aplica los cambios de forma inmediata. La forma de pago "American Express" ya no aparece disponible en el POS al momento de registrar un cobro.* |

##### c) PP03 – Intento de deshabilitar todas las formas de pago

| **IDENTIFICADOR:** | *PP03* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP01 – Habilitar o deshabilitar formas de pago en el POS* | **NOMBRE:** *Intento de deshabilitar todas las formas de pago* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el sistema muestre una advertencia cuando el Administrador intenta deshabilitar todas las formas de pago disponibles, indicando que se requiere al menos una forma de pago habilitada para registrar cobros en el POS.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El Administrador accede a Administración > Punto de Venta > Formas de Pago.* | *El sistema presenta el listado de formas de pago con su estado actual, algunas habilitadas.* |
| *El Administrador deshabilita todas las formas de pago cambiando su estado a Deshabilitado.* | |
| *El Administrador hace clic en "Guardar".* | *El sistema muestra una advertencia indicando que se requiere al menos una forma de pago habilitada para registrar cobros en el POS, e impide guardar la configuración con todas las formas de pago deshabilitadas.* |

##### d) PP04 – Establecer orden de presentación de formas de pago

| **IDENTIFICADOR:** | *PP04* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP02 – Establecer orden de formas de pago* | **NOMBRE:** *Establecer orden de presentación de formas de pago* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba valida que el Administrador pueda establecer correctamente el orden de presentación de las formas de pago en el POS, y que las formas de pago aparezcan en el orden configurado al momento de registrar un cobro.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El Administrador accede a Administración > Punto de Venta > Formas de Pago.* | *El sistema presenta el listado de formas de pago con su orden de presentación actual.* |
| *El Administrador reordena las formas de pago mediante arrastrar y soltar o modificando el número de orden (ej.: coloca "Efectivo" en primer lugar).* | *El sistema registra el nuevo orden de presentación.* |
| *El Administrador hace clic en "Guardar".* | *El sistema aplica el nuevo orden de forma inmediata. Las formas de pago habilitadas aparecen en el POS en el orden configurado por el Administrador.* |

##### e) PP05 – Verificación de que formas de pago deshabilitadas no aparecen en el POS

| **IDENTIFICADOR:** | *PP05* |
| --- | --- |
| **CASO DE PRUEBA ASOCIADO:** *CP01 – Habilitar o deshabilitar formas de pago en el POS* | **NOMBRE:** *Verificación de que formas de pago deshabilitadas no aparecen en el POS* |
| **Encargado de prueba:** *Mariela Estefany Ramos Loza* |
| **Descripción:** *Este escenario de prueba verifica que las formas de pago deshabilitadas por el Administrador en la configuración no aparezcan disponibles en el formulario "Cobrar venta" del módulo POS al momento de registrar un cobro.* |
| **FLUJO DEL ESCENARIO** |
| **ENTRADA:** | **SALIDA:** |
| *El Administrador ha deshabilitado la forma de pago "American Express" en Administración > Punto de Venta > Formas de Pago y ha guardado los cambios.* | *El sistema aplica los cambios de forma inmediata.* |
| *Un usuario accede al módulo Punto de Venta, agrega artículos al carrito y hace clic en "Cobrar".* | *El sistema abre el formulario "Cobrar venta". En la lista de formas de pago disponibles, la opción "American Express" no aparece, ya que fue deshabilitada por el Administrador.* |

---

***** CONFIDENCIAL *****

*Versión 1.0 — 09/05/2026 — Mariela Estefany Ramos Loza*
