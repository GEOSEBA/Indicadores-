# Indicadores-
library(sf); library(tidyverse); library(ggplot2); library(glue); library(readxl)
#Definir carpeta de trabajo
root_folder <- "C:/Users/USUARIO/Desktop/GGPLOT"
data_folder <- "/Input/"
input_fldr <- glue("{root_folder}/{data_folder}64._Consumo_de_agua_potable_BOX")
#Importar tabla de datos indicadores
consumo_agua <- read_excel("C:/Users/USUARIO/Desktop/GGPLOT/Input/64._Consumo_de_agua_potable_BOX.xlsx")
#Dividir layout en 4
matrix(c(1:4), nrow=2, byrow=FALSE)
layout(matrix(c(1:4), nrow=2, byrow=FALSE))
layout.show(4)
#Crear histogramas 
ggplot(consumo_agua,aes(x = Ciudades, y = a)) + geom_boxplot()
