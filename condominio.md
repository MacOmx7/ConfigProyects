# Copiar a application-local.properties (excluido de Git).
# Arrancar Maven o el JAR desde condominio-backend.
spring.datasource.url=jdbc:postgresql://localhost:5432/curancurani
spring.datasource.username=postgres
spring.datasource.password=postgres
# Secreto aleatorio >= 32 bytes, distinto de la contraseña de PostgreSQL.
app.jwt-secret=REEMPLAZAR_CON_SECRETO_ALEATORIO_DE_32_BYTES_O_MAS
app.bootstrap-username=admin
# Obligatorio sólo en el primer arranque sobre una base sin usuarios.
app.bootstrap-password=REEMPLAZAR_CON_CLAVE_INICIAL_DE_AL_MENOS_12_CARACTERES
app.cors-origins=http://localhost:5173,http://127.0.0.1:5173,http://localhost:4173,http://127.0.0.1:4173

# Libelula: completar aqui los valores privados o exportar LIBELULA_* al proceso.
# Appkey y registration-url: datos del comercio entregados por Libelula.
# Callback: URL publica HTTPS del backend terminada en /api/pago-exitoso.
# Retorno: URL del frontend terminada en /#/payments.
# Confirmar el callback POST y la conservacion de token antes de habilitar su confirmacion.
app.libelula.enabled=true
app.libelula.test-mode=true
app.libelula.appkey=4399e333-e112-8819-f857-a42212227e11
app.libelula.registration-url=https://api.libelula.bo/rest/deuda/registrar
app.libelula.callback-url=http://127.0.0.1:8084/api/pago-exitoso
app.libelula.return-url=http://127.0.0.1:5173/#/payments
app.libelula.callback-token-confirmed=false
app.libelula.timeout-seconds=20
# La consulta autenticada confirma pagos sin depender de un callback publico en pruebas.
app.libelula.status-url=https://api.libelula.bo/rest/deuda/consultar_deudas/por_identificador
