## Sesion 1-2 R -- 24/10/2022

## 1. Cálculos básicos

### 1.1 Suma
1+1

### 1.2 Calcular el 15% de $1.900
0.15*1900

### 2. Instalar estos Paquetes 
install.packages("tidyverse")
install.packages("dplyr")
install.packages("plyr")
install.packages("tidyr")
install.packages("mlogit")
install.packages("stargazer")
install.packages("rsq")
install.packages("sjPlot")
install.packages("dslabs")

### 2.1 Cargar desde la biblioteca estos Paquetes
library(tidyverse)
library(dplyr)
library(plyr)
library(tidyr)
library(mlogit)
library(stargazer)
library(rsq)
library(sjPlot)
library(dslabs)

## 2. Encuesta CEP
### 2.1 Link: https://www.cepchile.cl/cep/encuestas-cep/encuestas-2010-2021/estudio-nacional-de-opinion-publica-n-86-abril-mayo-de-2022

### 2.2 Importar base de datos
library(haven)
base_86 <- read_excel("C:/Users/Acer/Desktop/encuesta_cep_abr_may2022/encuesta_cep_abr-may2022/base_86.xlsx")
View(base_86)

# 2.3Variable numérica
base_86[sapply(base_86, is.numeric)] <- lapply(base_86[sapply(base_86, is.numeric)], as.factor)

## 3. Análisis descriptivo

### 3.1 Frecuencias

### Variable Inicial: sexo
table(base_86$sexo)

### Variable segunda: pobreza
table(base_86$pobreza_111)

### variable tercera: religión
table(base_86$religion_82)

### variable cuarta: situación política
table(base_86$percepcion_38)

### variable quinta: identidad política
table(base_86$iden_pol_2)

### variable sexta: evaluación del Gobierno
table(base_86$eval_gob_1)
