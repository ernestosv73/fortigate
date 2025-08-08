# Laboratorio práctica de Firewall con Containerlab
---
La topología creada tiene por objetivo poveer un entorno controlado para la configuración de un firewall.

# Requisitos previos
---
La imagen utilizada del firewall Fortigate se provee como una VM basada en QEMU y requiere del proyecto vrnetlab para ejecutar la VM dentro de un contenedor docker, en pocas palabras se trata de
"una VM disfrazada de contenedor"
Siga los siguientes pasos:

* Crear una cuenta en Github e importar el repositorio https://github.com/ernestosv73/fortigate
* Descargar la imagen fortinet-6.0.3.qcow2 en su dispositivo laptop o PC desde .
* Instalar VSCode e instalar las extensiones GitHub Codespaces y Dev Containers.
* Desde el repositorio importado, crear un nuevo codespace.
* Desde el directorio /workspaces ejecutar git clone https://github.com/hellt/vrnetlab.git para descargar los archivos requeridos para crear el docker de vr-fortios
* Para copiar la imagen .qcow2 al repositorio remoto debemos iniciar sesión desde VSCode ejecutando Ctrl+Shift+P y escribir GitHub: Sign in. Seguir los pasos hasta completar el proceso.
* Conectarse al codespace ejecutando Ctrl+Shift+P y escribir Connect to Codespace.
* Para copiar la imagen .qcow2 del host local al repositorio remoto, ejecutamos Ctrl+Shift+P y escribir File: Open Folder...y no posicionamos en el directorio /workspaces/vrnetlab/fortigate/
* Finalemente, arrastramos la imagen .qcow2 al arbol de directorio en vscode.
* Generar el contenedor docker ejecutando make 
  
# Ejecución de topología
---
Desde el directorio /workspaces/ipv6sec/ ejecutar clab deploy -t forti.yml 

# Actualizar topología en Codespaces
---
Para actualizar en codespaces los cambios en la configuración de la topolgía del repositorio, ejecutar en la terminal 
de codespaces `git pull origin main` 
