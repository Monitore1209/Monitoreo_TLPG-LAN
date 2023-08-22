Monitorear direcciones IP mediante solicitudes ICMP (ping) por medio de consultas.
Se proporciona una aplicación web mediante Flask para ver los estados de las direcciones IP y el historial de encuestas.
La encuesta se ejecuta como un servicio como parte de la aplicación web.
Se utiliza una base de datos SQLite para almacenar hosts, resultados de encuestas, cuentas de usuario, etc.

**Configuración**
Los siguientes ajustes deberán realizarse para la configuración:

```Cambiar Politicas (solo Windows)```

 En windows cambiar las politicas, ejecute Powershell como administrdor y ejecute el siguiente comando:

     Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser


```Instalar Python```

1.- Python 3.0+ debe estar instalado


```Clonar el repositorio```

2.- clonar el repositorio

    git clone https://github.com/Monitore1209/Monitoreo.git 


```Entorno Virtual```

3.- Crear el entorno virtual con el siguiente comando:

     Python -m venv .venv

4.- Activar el entorno virtual con el siguiente comando:

    .\.venv\Scripts\activate


5.- Desde el directorio principal de este repositorio, ejecute el siguiente comando:

     pip install -r requirements.txt

```Actualizar PIP```

6.-  ejecute el siguiente comando:

    python.exe -m pip install --upgrade pip
     

   ```Iniciar el Servidor```

7.- poner en marcha el servidor, ejecute el siguiente comando:

    flask run

  Flask corre pór defecto en el puerto 5000 si desea cambiar el puerto ejecute el siguiente comando:

    flask run --port 6000

  Para aceptar peticiones de otros ordenadores de nuestra red lanzaremos el servidor de la siguiente manera:

     flask run --host 0.0.0.0


