# CompuGamers
Proyecto final Sistemas Organizacionales Y Gerenciales 2

## Prerrequisitos
* Docker
* Docker Compose

## Instalación de Odoo

1. Configurar el archivo **docker-compose.yml**
    ```yml
        version: '3'
        services: 
            odoo:
                image: odoo:12.0
                container_name: Odoo
                restart: always
                links: 
                    - db
                ports: 
                    - "8069:8069"
            
            db:
                image: postgres:10
                container_name: Postgres
                restart: always
                environment: 
                    - POSTGRES_DB=postgres
                    - POSTGRES_PASSWORD=odoo
                    - POSTGRES_USER=odoo
    ```

2. Correr en consola el comando ``docker-compose up -d``

## Configuar base de datos en Odoo

1. Abrir en el navegador la url **http://localhost:8069**
2. Llenar el formulario
    ![Formulario](imgs/odooForm.png)

3. Crear database

## Contribuidores
- [Erik Flores](https://github.com/erflod5) <br> 201701066

## Licencia
Este proyecto está desarrollado bajo la [Licencia MIT](LICENSE).
