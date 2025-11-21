📝 **Resumen de la clase – Invocaciones síncronas de Lambda**

---

🔑 **Puntos Clave para el Examen AWS Developer Associate**

- **AWS Lambda**: ejecuta código sin aprovisionar ni administrar servidores.
- **Formas de invocación**:
  - `RequestResponse` (síncrona): el solicitante espera la respuesta.
  - `Event` (asíncrona): evento en cola, Lambda procesa cuando puede.
  - `DryRun`: valida permisos, no ejecuta el código.
- **Configuraciones en AWS CLI**: 
  - `InvocationType` define la forma de invocar.
  - Por defecto es síncrona.
- **Uso típico**:
  - Síncrona para API Gateway o apps que necesitan respuesta inmediata.
  - Asíncrona para procesamiento en background (ej. S3, SNS/SQS).
- **Dead Letter Queue (DLQ)**:
  - Para manejo de errores en invocaciones asíncronas.
- **Permisos e IAM**:
  - Roles y políticas para ejecutar Lambda y acceso a servicios.
  - Permisos: _en el recurso_ (quién puede invocar) y _por identidad_ (roles para Lambda).

---

📚 **Datos adicionales de internet e IA (documentación oficial AWS)**

- **Modos de invocación Lambda**:
  - Síncrona: cliente espera la respuesta. Usada por API Gateway, consola, SDK.[8][16][20]
  - Asíncrona: procesamiento en segundo plano y reintentos en caso de error. Fallos pueden enviarse a DLQ.
- **Permisos Lambda/IAM**:
  - **Rol de ejecución** necesario para acceso a otros servicios.
  - Políticas mínimas recomendadas (principio de menor privilegio).[13][17][21]
  - IAM regula quién invoca la función y cómo (por identidad o recurso).
- **Buenas prácticas**:
  - Configura DLQ para invocaciones críticas.
  - Usa CloudWatch/X-Ray para auditoría y monitoreo.[7][19]

---

**Referencias oficiales AWS:**
- [Documentación Lambda](https://aws.amazon.com/documentation-overview/lambda/)
- [API Invoke Lambda](https://docs.aws.amazon.com/lambda/latest/api/API_Invoke.html)
- [Permisos IAM Lambda](https://docs.aws.amazon.com/lambda/latest/dg/lambda-intro-execution-role.html)

---

✔️ **Iconos usados**:  
📝 resumen | 🔑 puntos clave | 📚 doc oficial | ✔️ buenas prácticas
