# Mount-Google-Drive-on-Ubuntu
Existen varias formas de montar Google Drive en Linux, pero una de las más populares es utilizando la herramienta google-drive-ocamlfuse. Esta herramienta te permite montar tu cuenta de Google Drive en un directorio de tu sistema de forma transparente.

## Pasos generales:


### Instalar google-drive-ocamlfuse:

```bash
sudo add-apt-repository ppa:alessandro-strada/ppa
sudo apt update
```
Fuente PPA: https://launchpad.net/~alessandro-strada/+archive/ubuntu/ppa

### Autorizar el acceso:

Este proceso es bastante sencillo y te guiará a través de un navegador web. Aquí te detallo los pasos:
- Ejecutar el comando:
-- Abre tu terminal y ejecuta el siguiente comando, reemplazando /ruta/a/tu/carpeta/de/montaje con la ruta donde deseas que se monte tu Google Drive:
  ```bash
  google-drive-ocamlfuse /ruta/a/tu/carpeta/de/montaje -id <tu_id_de_cliente> -secret <tu_secreto_de_cliente>
  ```

  IMPORTANTE: Crear un directorio de montaje: Antes de ejecutar el comando, asegúrate de que el directorio de montaje exista. Puedes crearlo con el comando mkdir /mnt/google_drive.

#### Para obtener el id y secret sigue estos pasos:

- Crea un proyecto en la Consola de API de Google:
  Ve a https://console.developers.google.com y crea un nuevo proyecto.
- Habilita la API de Drive:
  En tu proyecto, busca y habilita la API de "Google Drive API".
- Crea credenciales:
  En la sección "Credenciales" de tu proyecto, crea un conjunto de "Credenciales OAuth 2.0". Elige el tipo de "Aplicación web" y proporciona un nombre para tu aplicación.
- Obtén el ID de cliente y el secreto de cliente:
  Una vez creada la aplicación, anota el "ID de cliente" y el "Secreto de cliente" que se te proporcionen.

Listpo!

Una vez que hayas autorizado el acceso, puedes montar tu cuenta de Google Drive en un directorio específico de tu sistema utilizando un comando similar a este:
