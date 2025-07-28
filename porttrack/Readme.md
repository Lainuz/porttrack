
Se incluye pipeline con las configuraciones de monitoreo.

---

Allí podrás agregar los siguientes secretos requeridos para que el pipeline funcione correctamente.

---

## 🔑 Secretos requeridos

| Nombre del Secreto        | Descripción                                                                 |
|---------------------------|-----------------------------------------------------------------------------|
| `AWS_ACCESS_KEY_ID`       | Clave pública de acceso para la cuenta de AWS con permisos de despliegue.  |
| `AWS_SECRET_ACCESS_KEY`   | Clave secreta asociada a `AWS_ACCESS_KEY_ID`.                              |
| `SLACK_WEBHOOK_URL`       | (Opcional) URL del webhook entrante de Slack para notificaciones de alertas. |
| `DOCKER_USERNAME`         | (Opcional) Usuario de Docker Hub, si se publica la imagen allí.            |
| `DOCKER_PASSWORD`         | (Opcional) Contraseña o token de acceso a Docker Hub.                      |

---

## ✅ Buenas prácticas

- Nunca incluir estas claves directamente en archivos de código o configuración.
- Rotar periódicamente las credenciales en AWS y Docker Hub.
- Validar que los secretos estén correctamente nombrados y disponibles antes de ejecutar el pipeline.
- Usar permisos mínimos para las claves de AWS (principio de **mínimo privilegio**).

---

## 🧪 Verificación

Puedes probar que los secretos están funcionando correctamente ejecutando un push o pull request hacia la rama `develop` o `main`, y observando el resultado en la pestaña **Actions** de GitHub.

---

