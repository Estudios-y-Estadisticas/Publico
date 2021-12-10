<table width="auto" border="0px">
<tbody>
<tr>
<td width="25%"><img src="logofonasa.jpg" alt="logofonasa" width="auto" /></td>
<td width="75%"><h1>Anexo: Informe de PMG Género - Medida 8</h1>
<p><strong>Efectos de la pandemia en la población beneficiaria con perspectiva de género</strong><br>
Departamento de Estudios y Estadísticas<br>
División Desarrollo Institucional<br>
Fonasa, 2021</p></td>
</tr>
</tbody>
</table>


## Cálculos

En el presente repositorio se encuentran disponibles gráficos y tablas correspondiente al análisis realizado para el estudio *Efectos de la pandemia en la población beneficiaria con perspectiva de género*. Cada gráfico tiene un *link* asociado a un archivo de *Excel* con los datos **Originales** con los cuales se construyeron los indicadores. Al respecto existen 4 estadísticas principales.

- **Recuentos**: Corresponde a la número total de sujetos para un grupo y/o período determinado

- **Indice de feminidad a partir de recuentos**: Corresponde a la división del recuento (N) de mujeres por el recuento de hombres con base 100. Global o por grupo según corresponda

- **Tasas**: Expresada como `N x 1000`, corresponde a la cantidad de hombres o mujeres, divido por el total de la población Fonasa para el período y/o grupo correspondiente.

- **Indice de feminidad a partir de tasas**: Corresponde a la división entre la tasa (`N x 1000`) de hombres y mujeres expresado con base 100. Global o por grupo según corresponda.

Para el **cálculo de tasas** y sus derivados se debe contar con los datos del indicador y además de los datos de población para cada mes y/o grupo que corresponda.

> Los datos deberán estar en formato longitudinal para un correcto desarrollo informático.

## Desarrollo informático

Todo el proceso fue desarrollado y programado en **lenguaje R**, el cual permite automatizar la mayoría de las tareas relativas a los cálculos y construcción gráfica, en este contexto las principales características son:

1. Los datos de entrada deben todos tener el mismo formato
2. Los cálculos (antes explicados) son siempre iguales lo cual limita el error
3. Una vez validados los algoritmos de cálculo se pasa la data de entrada directamente al gráfico, no hay productos intermedios.

> Contar con un sistema que tiene una **entrada** (datos) y una **salida** (gráfico) sin la producción de elementos intermedios reduce errores, permite replicar y modificar de manera sencilla y por sobre todo deja el sistema disponible para otro período, sin la necesidad de construir todo desde cero.

Las librerías (principales) utilizadas son:

- `ggplot2` para los gráficos
- `data.table` para el data management
- `stringr` para el tratamiento de texto
- `ROracle` para conectar **R** a las bases de datos de Fonasa

----

## Gráficos y fuentes de datos

### Dimensión laboral

**Figura 1**: Tasa de participación laboral nacional por sexo (2018-2021)       
[Acceso a Datos](dataInforme/02_dataDes.xlsx?raw=true)

<img src="02 Situacion laboral/Participacion_Tasa.png" style="max-width:70% !important" />

----

**Figura 2**: Población beneficiaria de Fonasa que entra y sale desde/hacia las Isapres (2019-2021)    
[Acceso a Datos Entrada](dataInforme/01_data2Fonasa.xlsx?raw=true)   
[Acceso a Datos Salida](dataInforme/01_data2Isapres.xlsx?raw=true)

<img src="01 Evolucion de la poblacion beneficiaria/movimiento_N.png" style="zoom: 25%;" />

----

**Figura 3**: Índice de feminidad del movimiento de la población por tipo de seguro (2018-2021)   
[Acceso a Datos a Fonasa](dataInforme/01_data2Fonasa.xlsx?raw=true)   
[Acceso a Datos a Isapre](dataInforme/01_data2Isapres.xlsx?raw=true)

<img src="01 Evolucion de la poblacion beneficiaria/aFonasa_fem.png" alt="aFonasa_fem" style="zoom: 25%;" />

<img src="01%20Evolucion%20de%20la%20poblacion%20beneficiaria/aIsapre_fem.png" alt="aIsapre_fem" style="zoom: 25%;" />

----

**Figura 4**: Población de Fonasa por sexo e índice de feminidad (2018-2021) [Acceso a Datos](dataInforme/ ?raw=true)

<img src="01 Evolucion de la poblacion beneficiaria/pobla_N.png" alt="pobla_N" style="zoom: 25%;" />

<img src="01 Evolucion de la poblacion beneficiaria/pobla_fem.png" alt="pobla_fem" style="zoom: 25%;" />

----

**Figura 5**: Cotizante de Fonasa por sexo (2018-2021) [Acceso a Datos](dataInforme/ ?raw=true)

<img src="02 Situacion laboral/cotiza_N.png" alt="cotiza_N" style="zoom: 25%;" />

----

### Dimensión sanitaria

**Figura 6**: Casos confirmados de Covid-19 por 1000 beneficiarios/as por sexo (marzo 2020 – septiembre 2021) [Acceso a Datos](dataInforme/ ?raw=true)

<img src="03 contagio hospi fallec vacuna/covid_tasa.png" alt="covid_tasa" style="zoom: 25%;" />

----
**Figura 7**: Tasa de hospitalizaciones por 1000 beneficiarios/as por sexo (2018-2021) [Acceso a Datos](dataInforme/ ?raw=true)

<img src="03 contagio hospi fallec vacuna/egreso_tasa_total-covid.png" alt="egreso_tasa_total-covid" style="zoom:25%;" />

----

**Figura 8**: Tasa de hospitalizaciones Covid-19 por 1000 beneficiarios/as por sexo (marzo 2020 – septiembre 2021) [Acceso a Datos](dataInforme/ ?raw=true)


<img src="03 contagio hospi fallec vacuna/EgresoCovid_tasa.png" alt="EgresoCovid_tasa" style="zoom:25%;" />

----

**Figura 9**: Defunciones por Covid-19 por 1000 beneficiarios/as por sexo (marzo 2020 – septiembre 2021) [Acceso a Datos](dataInforme/ ?raw=true)


<img src="03 contagio hospi fallec vacuna/defuncion_tasa_covid.png" alt="defuncion_tasa_covid" style="zoom:25%;" />

----

**Figura 10**: Defunciones por otras causas por 1000 beneficiarios/as por sexo (2018-2021) [Acceso a Datos](dataInforme/ ?raw=true)


<img src="03 contagio hospi fallec vacuna/defuncion_tasa_NOcovid.png" alt="defuncion_tasa_NOcovid" style="zoom: 25%;" />

----

**Figura 11**: Porcentaje de beneficiarios/as vacunados contra el Covid-19 por sexo, edad y mes [Acceso a Datos](dataInforme/ ?raw=true)


<img src="03 contagio hospi fallec vacuna/vacuna_TasaAcu_18-29.png" alt="vacuna_TasaAcu_18-29" style="zoom:25%;" />

<img src="03 contagio hospi fallec vacuna/vacuna_TasaAcu_30-59.png" alt="vacuna_TasaAcu_30-59" style="zoom:25%;" />

<img src="03 contagio hospi fallec vacuna/vacuna_TasaAcu_60mas.png" alt="vacuna_TasaAcu_60mas" style="zoom:25%;" />

----

### Acceso a Salud Preventiva


**Figura 12**: Evolución de examen de Papanicolau realizados (2018-2021) [Acceso a Datos](dataInforme/ ?raw=true)

<img src="04 DEIS Medicina preventiva/papN.png" alt="papN" style="zoom:25%;" />

----

**Figura 13**: Evolución de examen de Mamografía realizados (2018-2021) [Acceso a Datos](dataInforme/ ?raw=true)


<img src="04 DEIS Medicina preventiva/mamoN.png" alt="mamoN" style="zoom:25%;" />

----

**Figura 14**: Evolución de Examen de Medicina Preventiva realizados por 1000 beneficiarios/as (2018-2021) [Acceso a Datos](dataInforme/ ?raw=true)


<img src="04 DEIS Medicina preventiva/emp_tasa.png" alt="emp_tasa" style="zoom:25%;" />

----

### Resolución de necesidades de salud (GES y no GES)

**Figura 15**: Tasa de Garantías activas y retrasadas por sexo por mil beneficiarios/as (2018-2021) [Acceso a Datos](dataInforme/ ?raw=true)

<img src="05 Ges y no ges/gesAbiertoRetrasado_tasa.png" alt="gesAbiertoRetrasado_tasa" style="zoom:25%;" />

<img src="05 Ges y no ges/cancerAbiertoRetrasado_tasa.png" alt="cancerAbiertoRetrasado_tasa" style="zoom:25%;" />

<img src="05 Ges y no ges/depreAbiertoRetrasado_tasa.png" alt="depreAbiertoRetrasado_tasa" style="zoom:25%;" />

----

**Figura 16**: Personas que entraron a la lista de espera no GES por sexo (2018-2021) [Acceso a Datos](dataInforme/ ?raw=true)


<img src="05 Ges y no ges/NoGes_entradas_N.png" alt="NoGes_entradas_N" style="zoom:25%;" />

<img src="05 Ges y no ges/NoGes_entradas_fem_prestacion.png" alt="NoGes_entradas_fem_prestacion" style="zoom:25%;" />

----

**Figura 17**: Lista de espera no GES por sexo y tipo de prestación (2019-2021) [Acceso a Datos](dataInforme/ ?raw=true)


<img src="05 Ges y no ges/NoGes_espera_N_prestacion.png" alt="NoGes_espera_N_prestacion" style="zoom:25%;" />

<img src="05 Ges y no ges/NoGes_espera_fem_prestacion.png" alt="NoGes_espera_fem_prestacion" style="zoom:25%;" />

----

### Uso de Licencias Médicas

**Figura 18**: Evolución de Licencias Médicas relacionadas al Covid-19 (2018-2021) [Acceso a Datos](dataInforme/ ?raw=true)

<img src="06 Licencias/stackLM.png" alt="stackLM" style="zoom:25%;" />

<img src="06 Licencias/covid_n.png" alt="covid_n" style="zoom:25%;" />

----

**Figura 19**: Evolución de Licencias Médicas de salud mental (2018-2021) [Acceso a Datos](dataInforme/ ?raw=true)


<img src="06 Licencias/mental_n.png" alt="mental_n" style="zoom:25%;" />

<img src="06 Licencias/mental_n_fem.png" alt="mental_n_fem" style="zoom:25%;" />

----

**Figura 20**: Evolución de Licencias Médicas de salud mental (2018-2021) [Acceso a Datos](dataInforme/ ?raw=true)


<img src="06 Licencias/mental_media.png" alt="mental_media" style="zoom:25%;" />

<img src="06 Licencias/mental_media_fem.png" alt="mental_media_fem" style="zoom:25%;" />

----

