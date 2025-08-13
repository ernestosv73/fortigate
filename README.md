# Laboratorio práctica de Firewall con Containerlab
---
La topología creada tiene por objetivo poveer un entorno controlado para la configuración de un firewall.

# Requisitos previos
---
La imagen utilizada del firewall Fortigate se provee como una VM basada en QEMU y requiere del proyecto vrnetlab para ejecutar la VM dentro de un contenedor docker, en pocas palabras se trata de
"una VM disfrazada de contenedor"
Siga los siguientes pasos:

* Crear una cuenta en Github e importar el repositorio https://github.com/ernestosv73/fortigate
* Descargar la imagen fortios-v6.0.3.qcow2 en su dispositivo local.
* Desde el servidor Linux, clonar vrnetlab ejecutando: git clone https://github.com/hellt/vrnetlab.git
* Asignar permisos de escritura a la carpeta /home/usuario/vrnetlab/fortigate
* Copiar el archivo descargado, (fortios-v6.0.3.qcow2) a la carpeta fortigate en el Servidor Linux
* Generar el contenedor docker ejecutando `make` 
  
# Ejecución de topología
---
Desde el directorio /home/usuario/fortigate ejecutar `clab deploy -t forti.yml` 
