## Descripción de las columnas

Cada fila del dataset representa a un cliente de la empresa. Las columnas
contienen información personal, servicios contratados, datos de facturación y
si el cliente abandonó o no el servicio.

### Identificación del cliente

- **`customerID`**: identificador único de cada cliente. Se utiliza para reconocer
  al cliente, pero no describe ninguna característica útil para la predicción.

### Datos personales

- **`gender`**: género registrado del cliente. Sus valores son `Male` y `Female`.

- **`SeniorCitizen`**: indica si el cliente es un adulto mayor. Está representada
  con `1` para sí y `0` para no.

- **`Partner`**: indica si el cliente tiene pareja. Sus valores son `Yes` y `No`.

- **`Dependents`**: indica si el cliente tiene personas a cargo. Sus valores son
  `Yes` y `No`.

### Antigüedad

- **`tenure`**: cantidad de meses que el cliente lleva utilizando los servicios
  de la empresa.

### Servicio telefónico

- **`PhoneService`**: indica si el cliente tiene contratado el servicio
  telefónico. Sus valores son `Yes` y `No`.

- **`MultipleLines`**: indica si el cliente tiene más de una línea telefónica.
  Puede tomar los valores `Yes`, `No` o `No phone service`.

  `No` significa que tiene servicio telefónico, pero solamente una línea.
  `No phone service` significa que directamente no tiene contratado el servicio
  telefónico.

### Servicio de Internet

- **`InternetService`**: indica el tipo de servicio de Internet contratado.
  Puede tomar los valores `DSL`, `Fiber optic` o `No`.

- **`OnlineSecurity`**: indica si el cliente tiene contratado un servicio de
  seguridad en línea. Sus valores son `Yes`, `No` o `No internet service`.

- **`OnlineBackup`**: indica si el cliente tiene contratado un servicio de copia
  de seguridad en línea. Sus valores son `Yes`, `No` o
  `No internet service`.

- **`DeviceProtection`**: indica si el cliente tiene protección para sus
  dispositivos. Sus valores son `Yes`, `No` o `No internet service`.

- **`TechSupport`**: indica si el cliente tiene contratado soporte técnico.
  Sus valores son `Yes`, `No` o `No internet service`.

- **`StreamingTV`**: indica si el cliente utiliza un servicio de streaming de
  televisión. Sus valores son `Yes`, `No` o `No internet service`.

- **`StreamingMovies`**: indica si el cliente utiliza un servicio de streaming
  de películas. Sus valores son `Yes`, `No` o `No internet service`.

En estas columnas, `No` significa que el cliente tiene Internet pero no contrató
ese servicio adicional. En cambio, `No internet service` significa que el
cliente directamente no tiene conexión a Internet contratada.

### Contrato y facturación

- **`Contract`**: indica la duración del contrato. Puede ser mensual
  (`Month-to-month`), de un año (`One year`) o de dos años (`Two year`).

- **`PaperlessBilling`**: indica si el cliente utiliza facturación electrónica.
  Sus valores son `Yes` y `No`.

- **`PaymentMethod`**: indica el medio utilizado para pagar el servicio. Las
  opciones son cheque electrónico, cheque enviado por correo, transferencia
  bancaria automática o tarjeta de crédito automática.

- **`MonthlyCharges`**: importe que se le cobra al cliente mensualmente.

- **`TotalCharges`**: importe total acumulado que el cliente pagó durante el
  tiempo que permaneció en la empresa. Aunque debería ser numérica, inicialmente
  es leída como texto debido a la presencia de espacios en blanco en algunos
  registros.

### Variable objetivo

- **`Churn`**: indica si el cliente abandonó el servicio. Toma el valor `Yes`
  cuando el cliente abandonó y `No` cuando permaneció.

Esta es la variable que se quiere predecir a partir del resto de la información.
