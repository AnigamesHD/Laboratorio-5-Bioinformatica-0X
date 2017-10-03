# Laboratorio 05 Bioinformática

## Nombre: Byron Guzmán Marín

## Profesor(a): Katterinne Méndez Carrasco

 ## Plataforma MG-RAST y exploración de metagenomas

## Responde:
__¿Cuántas secuencias fueron subidas?__ 

En la plataforma de MG-RAST para el proyecto metagenoma de JVCI Global Ocean Sampling Expedition, para la muestra tomada del sitio de buceo de Dirty Rock en las Islas Cocos de Costa Rica, se indican 120,671 secuencias subidas (Upload: Sequences Count). 

__¿Qué tipo de plataforma de secuenciamiento fue usada para producir estos datos?__

En primer lugar, luego de que obtuvieron la muestra, realizaron a cabo un secuenciamiento mediante el método de metagenómica de Shotgun, el cual desde la muestra tomada directamente del ambiente, el DNA se corta en pequeños fragmentos que se secuencian de manera independiente, dando lugar a reads los cuales se alinean posteriormente. Posteriormente, de todas las secuencias para realizar un control de calidad, utilizaron la plataforma de DRISEE la cual provee un método para validar la calidad al detecar errores en genomas completos obtenidos por secuenciamiento a través de metagenómica de Shotgun, y utilizar estos datos para descubrir errores no caracterizados previamente en las plataformas de secuenciación de 454 e Illumina. Para esta muestra, DRISEE no pudo producir un perfil, ya que la muestra falló en cubrir los requerimientos mínimos de ADR (artificial duplicate reads) para calcular un perfil de error. Por ello, prosiguieron a realizar perfiles mediante kmers, en donde la abundancia en el espectro de kmers son herramientas para resumir la redundancia (repeticiones) de un conjunto de datos de secuencias; y luego un histograma de posición de nucleotidos, en donde los perfiles de posición de nucleótidos muestran la abundancia relativa de las cuatro pares de bases en todos los reads. Posterior al control de calidad, las secuencias fueron procesadas y analizadas mediante el sistema de metagenómica de MG-RAST para obtener los resultados mostrados en la página, en donde a las características proteicas predichas, se les asignó una anotación al utilizar la base de datos de proteinas de M5NR.

__¿Cuántas secuencias pasaron el control de calidad? ¿A qué crees que se refiere esto?__

120671 secuencias pasaron el control de calidad (QC, Quality Control), las cuales fueron las secuencias subidas en primer lugar, ya que 0 fallaron en pasar el QC (0,0%). El control de calidad (QC) se refiere al filtro de datos para secuenciación de nucleótidos, incluyendo la remoción de "artificial duplicate reads" (reads que pueden conducir a una interpretación incorrecta de la abundancia de genes y especies en estudios de metagenómica), recortes de reads basados en calidad, recortes de reads basados en longitud, y detección (screening) de ADN de organismos modelos no humanos.

__¿Cuántos otros metagenomas están disponibles para el bioma “marine habitat”?__

Si se dirige hacia el buscador de metagenomas y se flitran los resultados para la bioma "marine habitat", se encuentran 6055 metagenomas anotados.

__¿Cuántas reads fueron asignadas a eucariontes según MG-RAST?__

Del proyecto por JVCI Global Ocean Sampling Expedition, para la muestra tomada del sitio de buceo de Dirty Rock, si se dirige hacia "Taxonomic Hits Distribution", en donde se ilustra la distribución taxónomica en donde cada trozo de los gráficos indican el porcentaje de reads con proteinas y genes de RNA ribosomoles predichos (segpun las bases de datos que MG-RAST utiliza), en el gráfico de dominios, éste indica que 20128 reads pertenecen al dominio de eucariontes.

__¿Cuál es el filo (Phylum) más abundante en la muestra?__

Según el gráfico de filo (Phylum), el más abundante es el de Cyanobacterias, con 39919 reads (29.56%).

__¿A cuántas secuencias se les asignó una función de acuerdo a la base de datos KEGG con un e-value entre -10 y -20?__

 Si se dirige hacia "Source Hits Distribution", la base de datos de Kegg, asignó una función según las características de las proteinas predichas que puedan tener similitud a proteinas con función conocida que estén anotadas en la base de datos, mostrando un color específico según el rango de e-value (número de alineamientos diferentes con puntajes equivalentes o mejore sque los que se esperan ocurran por chance). Para un e-value entre -10 y -20, Kegg asignó una función a 7960 secuencias.

__¿Por qué hay tan pocas secuencias con funciones asignadas según SwissProt?__

 Los hits resultantes por la base de datos de SwissProt, son considerablemente menores en comparación al resto. En MG-RAST, las barras en Source Hits Distribution, representan las reads anotadas, en donde las bases de datos tienen un número diferente de hits, que depende de la cantidad de datos que la base de datos tenga para que la secuencia colocada se le asigne una función dentro de esa base de datos según la similitud que haya, produciendo hits. El hecho de que SwissProt haya producido un menor número de hits, se debe a que es una base de datos curada, es decir, que la información que la base de datos contiene está revisada, lo cual la diferencia de por ejemplo, otras bases de datos que producieron un mayor número de hits, como GenBank y TREMBL, dado que estas últimas corresponden a bases de datos no-curadas. Al estar no curadas, esto hace rfrencia a que pueden contener secuencias redundantes, más entradas referentes a un sólo proyecto, secuencias hipotéticas, etc, por lo que generará un mayor número de hits al contener más entradas. SwissProt por su parte, contiene anotaciones de alta calidad, es no-redundante, y es de referencia cruzada con otras bases de datos, por lo que resultará en un menor número de hits al contener menos anotaciones, pero éstas estarán revisadas; por lo que la diferencia en secuencias similares a las predichas de la muestra recae en el estado de curación que existe entre las bases de datos.

## Análisis de metagenomas

## Responde:

__¿Cuántas secuencias mapearon en contra de Proteobacteria? (Usa la opción Redraw para usar reads en vez de proporciones (raw))__


 Al realizar el análisis del metagenoma anterior con los parámetros requeridos (con un e-value máximo de 1e-10 comparando los datos mediante M5NR), en la pestaña de "Organism barchart 1", se muestra la distribución de dominios, y al presionar sobre el dominio de bacterias, se lista la distribución por filo (Phylum), indicando que para la categoría de Proteobacterias, se encuentran 26387 secuencias.
 
__¿Cuántas secuencias de Salmonella ( Proteobacteria; Gammaproteobacteria; Enterobacteriales; Enterobacteriaceae) fueron identificadas?__ 

 Del filo de bacterias anterior, al realizar la búsqueda de este dato en las tablas, análisis, filtración  por medio de genus, se observo que para Salmonella, se encuentran 77 secuencias

