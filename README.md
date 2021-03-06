# COVID_data_tool
Paquetería de JULIA creada con el fín de unir datos abiertos sobre casos COVID-19 y demografía de México.\
Compatible con JULIA 1.x.x

### Prerrequisitos
Paquetes de JULIA necesarios para el funcionamiento de la paquetería.\
    `HTTP`\
    `DataFrames`\
    `CSV`\
    `JSON`\
    `InfoZIP`\
    `ZipFile`\
    `XLSX`\
    `ExcelFiles`\
    `Dates`\
Pueden instalarse con el administrador de paquetes de JULIA pulsando la tecla `]` en el REPL\
    `add HTTP DataFrames CSV JSON InfoZIP ZipFile XLSX ExcelFiles Dates`\
    \
    ![](images/prerequisitos.GIF)
    \
Si ya tienes estas paqueterías previamente mencionadas puedes omitir este paso.

### Instalación
**Si utilizas Linux debes ejecutar JULIA como superusuario para la instalación.**
Haciendo uso del REPL de JULIA presiona la tecla `]` para al administrador de paquetes de JULIA e ingresar\
    `add https://github.com/OscarJVP/COVID_data_tool.jl`\
    \
    ![](images/instalacion_1.GIF)
    \
Por último regresar a la línea de comandos de JULIA presionando la tecla `backspace` y compilar la paquetería ingresando\
    `using COVID_data_tool`\
    \
    ![](images/instalacion_2.gif)
    \
Puedes probarla con\
    `COVID_data_tool.indicadores_disponibles()`\
    \
    ![](images/instalacion_4.GIF)


### Funciones
`indicadores_disponibles()`\
Muestra la lista de indicadores disponibles para consulta.


`dato_estado(indicador::String, estado::String)`\
Recibe el indicador a consultar como `String` y el estado como `String`.\
Crea un .csv con la información deseada en la entrada de la función y muestra el nombre del archivo creado con éxito.


`conjunto_estado(indicadores::Vector{String}, estado::String)`\
Recibe los indicadores a consultar como un `array` de tipo `String`,el estado como `String` y el municipio como `String`.\
Crea un .csv con la información deseada en la entrada de la función y muestra el nombre del archivo creado con éxito.


`comp_CovInd(indicadores::Vector{String},estado::String,municipio::String)`\
Recibe los indicadores a consultar como un `array` de tipo `String`,el estado como `String` y el municipio como `String`.\
Crea un .csv con la información deseada adicional a información de COVID-19 en la entrada de la función y muestra el nombre del archivo creado con éxito.


`downloadCD()`\
Realiza la descarga de datos acerca del COVID-19 para poder ser consultados.


### Notas
* Las funciones que requieran un estado como entrada necesitan el nombre oficial del estado v. gr. Michoacán se deben introducir como Michoacán de Ocampo.\
* Las funciones que requieran un indicador como entrada necesitan introducirse como están en el listado. Este se puede observar utilizando la función `indicadores_disponibles().`
* Todos los archivos .csv se generan en una carpeta con nombre archivos_CSV_COVID_data_tool dentro de C:\\archivos_CSV_COVID_data_tool en Windows, /home/archivos_CSV_COVID_data_tool en Linux.

## Fuentes de información
<a href="https://www.inegi.org.mx/" target="_blank">INEGI</a>\
<a href="https://www.coneval.org.mx/Paginas/principal.aspx" target="_blank">CONEVAL</a>\
<a href="https://www.mx.undp.org/content/mexico/es/home.html" target="_blank">Programa de las Naciones Unidas para el Desarrollo</a>\
<a href="https://www.gob.mx/conapo" target="_blank">CONAPO</a>\
<a href="http://www.municipios.mx/" target="_blank">Municipios</a>\
<a href="https://www.gob.mx/correosdemexico" target="_blank">Correos de México</a>

## Equipo de Trabajo
Deep Alpha\
<img src="images/deep_alpha.jpg" width="200">\
    - **Carlos Espadín** - *Director de proyecto* -\
    - **Luis Moysén** - *SCRUM Master* -\
    - **Luis Roa** - *Miembro del equpo desarrollador* -\
    - **Rodrígo Vazquez** - *Miembro del equpo desarrollador* -\
    - **Oscar Vargas** - *Miembro del equpo desarrollador* -\
    - **Susan Rodríguez** - *Tester* -\
    - **Eduardo Bacelis** - *Tester* -

## Licencia
Proyecto bajo [MIT License](LICENSE.md) licencia del MIT - Consulte [LICENSE.md](LICENSE.md) para mas detalles.
