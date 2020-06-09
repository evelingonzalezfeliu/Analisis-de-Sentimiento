Objetivo
--------

El objetivo es encontrar el motivo de la discrepancia del perfil de mutaciones de pacientes chilenos con cáncer de mama, con respecto a los datos de MSK o TCGA (en cBioportal). Para esto se aplicarán diferentes filtros adiccionales a los datos de OCA anotados con ANNOVAR.

Carpeta de trabajo
------------------

Carpeta local

`/Users/evelin/Desktop/CGI_VCF_QC_PASS/Annovar_OCA/Breast_Cancer/`

Script que realiza los filtros y gráficos. *Otros\_filtros\_OCA\_annovar\_BreastCancer.R*

Procedimiento y Resultados
--------------------------

Las variantes de OCA fueron filtradas inicialmente con VAF (frecuencia alélica de la variante) mayor o igual a 5% y con un FAO (lecturas del alelo alternativo normalizadas) mayor o igual a 10. Para las 57 muestras de *Breast\_Cancer* se reportan un total de 11.048 variantes, solo con estos filtros. A partir de estas variantes se fueron realizando diferentes filtros.

### Filtro 1: Variantes con efecto en la proteina, con filtro en gnomAD\_genoma\_ALL

Filtros inicial, donde podemos observar el perfil de variantes somáticas de cáncer de mama.

-   Solo variantes que produce un cambio en la proteína. (Variantes sinónimas se eliminan)
-   Variantes con AF en genomAD\_genome\_ALL menor o igual a 0.01 o campo vacio (sin AF poblacional reportada)

Datos:

-   *Total de variantes: 369*
-   Excel con las 369 variantes: 08-06-20-Filtros\_ANNOVAR\_OCA\_Breast\_Cancer. Pestaña: Filtro1\_369\_variantes [1](https://drive.google.com/file/d/1PMcfG4-yyJSEI9M2pp7Gyl1v-QWkosvt/view?usp=sharing)

<img src="369 filtro1.png" title=" thumb|none| 369 variantes - Filtro 1" alt=" thumb|none| 369 variantes - Filtro 1" width="700" />

### Filtro 2: Filtro 1 + variantes tipo InDels con VAF mayor o igual a 7%

A las 369 variantes del filtro 1, se le aplicó el siguiente filtro:

-   Solo variantes tipo InDels con VAF mayor o igual a 7%.

Datos:

-   *Total de variantes 325*
-   Excel con las 325 variantes: 08-06-20-Filtros\_ANNOVAR\_OCA\_Breast\_Cancer. Pestaña: Filtro2\_325\_variantes [2](https://drive.google.com/file/d/1PMcfG4-yyJSEI9M2pp7Gyl1v-QWkosvt/view?usp=sharing)

<img src="325 filtro2 InDels.png" title=" thumb|none| 325 variantes - Filtro 2" alt=" thumb|none| 325 variantes - Filtro 2" width="700" />

### Filtro 3: Filtro 2 + filtro de FA poblacional (GnomAD, 1000genomas, ExAC y ESP)

A las 325 variantes del filtro 2, se le aplica el siguiente filtro adicional:

-   Se seleccionan variantes con frecuencia alélica poblacional menor o igual a 0.01 (En todas las bases de datos poblacionales. gnomAD, ExAC, 1000genomas y ESP) o que no presentan AF reportada en estas.

Datos:

-   *Total de variantes: 256*
-   Excel con las 256 variantes: 08-06-20-Filtros\_ANNOVAR\_OCA\_Breast\_Cancer. Pestaña: Filtro3\_256\_variantes [3](https://drive.google.com/file/d/1PMcfG4-yyJSEI9M2pp7Gyl1v-QWkosvt/view?usp=sharing)

<img src="256 filtro3 AFpoblacional.png" title=" thumb|none| 256 variantes - Filtro 3" alt=" thumb|none| 256 variantes - Filtro 3" width="700" />

### Filtro 4: Filtro 3 + solo variantes con COSMIC-ID

A las 256 variantes del filtro 3, se le aplica el siguiente filtro adicional:

-   Solo variantes que tienen COSMIC-ID reportado.

Datos:

-   *Total de variantes: 67*
-   Excel con las 67 variantes: 08-06-20-Filtros\_ANNOVAR\_OCA\_Breast\_Cancer. Pestaña: Filtro4\_67\_variantes [4](https://drive.google.com/file/d/1PMcfG4-yyJSEI9M2pp7Gyl1v-QWkosvt/view?usp=sharing)

<img src="67 filtro4 cosmic v2.png" title=" thumb|none| 67 variantes - Filtro 4" alt=" thumb|none| 67 variantes - Filtro 4" width="700" />

<Category:Egonzalez-log>
