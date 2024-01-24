Los archivos referidos a los años 2018 y 2019 estaban en el formato correcto o al menos el más cómodo para trabajar con los datos. El archivo de 2023 tiene otro formato de fecha y fue lo único que tuve que transformar.

Por otra parte, los archivos 2020, 2021 y 2022 dentro de sus mismos archivos no respetaban o seguían un formato de fecha especifico. Al principio tuve muchos valores nulos y duplicados al tratar de separarlos de forma correcta. Luego, opte por analizar y separar con cuidado los intervalos de meses con ‘x’ tipo de formato.
Por ejemplo, en el archivo ‘molinetes-2020’, enero y febrero tienen el formato fecha dd/MM/yyyy mientras que de marzo a octubre, el formato cambia a MM/dd/yyyy y en noviembre y diciembre vuelve al primer formato mencionado. 

Al final, me quedaron algunos valores nulos que representan un 0.0015% del dataset lo cual es casi irrelevante para su posterior análisis.
En el archivo ‘molinetes-2021’ los meses de febrero y marzo tenían un formato de fecha distinto, así que lo solucione con un filtrado de fecha. 
El zip ‘molinetes-2022’ tiene algunos archivos con diferentes tipos de registros que me daban error al importarlos todos juntos. Entonces tuve que separar por algunos meses, corregir el tipo de dato y volver a unirlos para guardar el dataset.

Finalmente, realizando las visualizaciones en PowerBI me di cuenta que la columna ´ESTACION´ contaba con dos estaciones que estaban varias veces repetidas quizás por un cambio en el idioma del teclado o el programa al procesarse. Por ejemplo, la estación “Agüero” tenía otros valores como: “Ag´3ero” o varios otros con error en la letra ‘ü’. También la estación “Saenz Peña” sufría la misma alteración en el dataset. Esto lo corregi dentro del Query Editor por ser pocos errores, pero si fueran demasiados lo hubiera llevado a Python para lograr una solución más escalable.

Mi dashboard supera el limite establecido por github de 100mb por lo tanto dejo el archivo pdf y proximamente un link para tener acceso