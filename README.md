# README - Crear Payload para Android con Meterpreter

## Descripción

Este script automatiza el proceso de creación de un payload para Android utilizando Meterpreter y `msfvenom`. El payload generado permite establecer una conexión inversa desde un dispositivo Android a una máquina atacante, facilitando pruebas de penetración en entornos controlados y legales.

## Requisitos

- **Sistema Operativo**: Kali Linux o cualquier sistema compatible con Metasploit.
- **Metasploit Framework**: Asegúrate de tener Metasploit Framework instalado.
- **Conexión ADB**: Necesitarás ADB instalado si deseas transferir el APK al dispositivo Android.

## Instalación

1. **Clona o descarga el script**:
   - Crea un archivo llamado `create_payload.sh` y copia el contenido del script proporcionado.

2. **Dale permisos de ejecución**:
   ```bash
   chmod +x create_payload.sh
   ```

3. **Asegúrate de que Metasploit esté instalado**:
   ```bash
   sudo apt update
   sudo apt install -y metasploit-framework
   ```

## Uso

1. **Edita el script**:
   - Abre `create_payload.sh` y reemplaza `<tu_ip>` con la dirección IP de tu máquina atacante.
   - Reemplaza `<puerto>` con el puerto que deseas usar (por ejemplo, 4444).

2. **Ejecuta el script**:
   ```bash
   ./create_payload.sh
   ```

3. **Transfiere el APK**:
   - Usa ADB o cualquier otro método para transferir `payload.apk` al dispositivo Android.
   - Asegúrate de que el dispositivo tenga habilitadas las instalaciones de fuentes desconocidas.

4. **Inicia el listener en Metasploit**:
   - El script ya configura y activa el listener automáticamente.

5. **Captura la sesión**:
   - Cuando el usuario abra el APK en el dispositivo Android, deberías ver una sesión Meterpreter activa en tu terminal de Metasploit.

## Notas Importantes

- **Ética y Legalidad**: Este script es solo para fines educativos. Asegúrate de tener el consentimiento adecuado antes de realizar pruebas de penetración. La creación y ejecución de payloads sin autorización es ilegal y antiética.
- **Seguridad**: Mantén el entorno seguro y no utilices este script en dispositivos o redes sin permiso.

## Contribuciones

Si deseas contribuir a mejorar este script o agregar nuevas funcionalidades, siéntete libre de enviar un pull request o abrir un issue.

## Licencia

Este proyecto está bajo la Licencia MIT. Consulta el archivo LICENCIA para más información.
