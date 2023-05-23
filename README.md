# Scraping en Indeed y Bumeran
En el archivo "Scraping Jobs.ipynb" se encuentra la versión final del script que automatiza la búsqueda de las ofertas laborales de acuerdo a tu interés.

## Cambios a realizar para personalizar la búsqueda

### 1. Búsquedas
Mi proyecto lo desarrollé en torno a seis búsquedas en específico: DATA SCIENCE, DATA ANALYST, ANALISTA DE PLANEAMIENTO, ANALISTA DE RIESGO, ALISTA JUNIOR y BUSINESS INTELLIGENCE.
Para personalizar la búsqueda, se deberá actualizar la URL que se debe analizar según sea el caso en el driver.get:
![image](https://github.com/Kevinmanuelogamarra/Scrapingjobs/assets/109931089/b7824127-7e87-4d1d-8b51-6b51754f8386)
* Recordar que se debe cambiar la URL tanto en la sección de Indeed, como en la de Bumeran.

### 2. Filtro de ofertas
Una vez se recopiló toda la información, se debe filtrar los trabajos que no son de nuestro interés. 
En ese sentido, coloqué condicionales en los campos JOB, DESCRIPTION y DATE.
Cada uno de estos filtros excluyen los registros de acuerdo a las siguientes lógicas:
* JOB: Se eliminan todos los registros que contienen las palabras listadas en "excluir". En algunos casos el motivo es la jerarquía del puesto y en otros las competencias asociadas.
* DESCRIPTION: Se eliminan registros de acuerdo a la cantidad de años de experiencia requerida.
* DATE: Recopila las publicaciones anunciadas solo los últimos 5 días. Esto dependerá de la frecuencia que cada uno revise la lista de ofertas laborales.
* COMPANY: No coloqué ningún filtro, pero también se podría añadir un condicional de exclusión.
![image](https://github.com/Kevinmanuelogamarra/Scrapingjobs/assets/109931089/70ced579-e125-486b-b246-b28403783782)

