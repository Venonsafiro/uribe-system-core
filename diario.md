* ESPACIO PARA NOTAS RAPIDAS DE APRENDIZAJE

* Hoy aprendí que pasa cuando dejo una línea abierta sin cerrar comíllas.
* Usar Ctrl + C me ayuda a destrabar un comando trabado.
* Cada uno de los comandos practicado varias veces me enseña mas.

## 2026-08-18: Configuración de Credenciales en Git
- **Problema:** Git rechazaba el envio por falta de token de acceso.
- **Solución:** Se generó un Personal Access Token (PAT) en GitHub y se ejecutó `git config --global credential.helper store` para no volver a escribir las credenciales en cada `git push`.
