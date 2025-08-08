# Laboratorio práctica de Firewall con Containerlab
---
La topología creada tiene por objetivo poveer un entorno controlado para la configuración de un firewall.

# Requisitos previos
---
La imagen utilizada del firewall Fortigate se provee como una VM basada en QEMU y requiere del proyecto vrnetlab para ejecutar la VM dentro de un contenedor docker, en pocas palabras se trata de
"una VM disfrazada de contenedor"
Siga los siguientes pasos:

* Crear una cuenta en Github e importar el repositorio https://github.com/ernestosv73/ipv6sec.git
* Crear una cuenta en https://networkingsupport.hpe.com/
* Descargar la imagen Aruba_AOS-CX_Switch_Simulator_10.14.1000.ova desde https://networkingsupport.hpe.com/downloads/software/RmlsZTo3YmRlNGViZS01ZTY3LTExZWYtYTQzYy0wZjBjOGRmMzJkZmU%3D.
* Instalar VSCode e instalar las extensiones GitHub Codespaces y Dev Containers.
* Desde el repositorio importado, crear un nuevo codespace.
* Desde el directorio /workspaces ejecutar git clone https://github.com/hellt/vrnetlab.git para descargar los archivos requeridos para crear la imagen docker de ArubaOS-CX
* Para copiar la imagen .ova al repositorio remoto debemos iniciar sesión desde VSCode ejecutando Ctrl+Shift+P y escribir GitHub: Sign in. Seguir los pasos hasta completar el proceso.
* Conectarse al codespace ejecutando Ctrl+Shift+P y escribir Connect to Codespace.
* Para copiar la imagen .ova del host local al repositorio remoto, ejecutamos Ctrl+Shift+P y escribir File: Open Folder...y no posicionamos en el directorio /workspaces/vrnetlab/aoscx/
* Finalemente, arrastramos la imagen .ova al arbol de directorio en vscode.
* Desde el directorio remoto ../aoscx descomprimimos la imagen .ova ejecutando tar -xvf ArubaOS-CX_10_14_1000.ova
* Generar el contenedor docker ejecutando make docker-image
  
# Ejecución de topología
