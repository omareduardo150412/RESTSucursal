# RESTSucursal
URL con el gateway:
http://localhost:8090/api/citibanamex/sucursal/buscar

Se obtuvo la información del JSON con resttemplate como un string y se realizo un análisis del texto de Procesamiento del Lenguaje Natural donde se remplazaron datos que estaban en UTF-8 a ASCII y los datos que estan entre corchetes se extrajeron mediante un split.
[
          "278",
          "110",
          "C.F. Lindavista",
          "Av. PolitÃ©cnico 1700,",
          "Col. Lindavista, Gustavo A. Madero, C.P. 07730, Ciudad de MÃ©xico",
          "2",
          "Ricarte y Montevideo",
          "Ricarte and Montevideo",
          "0",
          "1",
          "09:00",
          "16:00",
          "16",
          "09:00",
          "16:00",
          "-99.1340422",
          "19.4885074",
          "Ciudad de MÃ©xico",
          "0",
          "Sucursal Digital",
          "9",
          "0",
          "7"
]

Mediante otro split usando como referencia las comillas "" se obtuvo cada dato del arreglo. 
Para obtener los datos de la ubicación se realizo una tokenización mediante las comas también se removieron los espacios al inicio y al final de cada dato 
