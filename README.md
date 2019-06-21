# Indicadores-
library(sf); library(tidyverse); library(ggplot2); library(glue); library(readxl)
#Definir carpeta de trabajo
home_dir <- "C:/Users/USUARIO/Desktop/GGPLOT"
input_folder <- glue("{home_dir}/Input")
output_folder <- glue("{root_floder}")
#Importar tabla de datos indicadores
consumo_agua <- read.csv(glue("{input_folder}/64._Consumo_de_agua_potable.csv"))
#Filtrar data
consumo <- select(consumo_agua, Litros.per.capita.al.dia)
a <- select(consumo_agua, Litros.per.capita.al.dia) %>% unlist

p <- ggplot(consumo, aes(x = Litros.per.capita.al.dia)) + geom_histogram() 
ggplot(consumo, aes(x = Litros.per.capita.al.dia)) + geom_histogram() + stat_bin(bins = 30)

