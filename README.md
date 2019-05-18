# ProyectoBigData

setwd("~/Documents/Big Data/Proyecto final")

bots <-read.csv("bots_data.csv", stringsAsFactors = F)
str(bots)

nonbots <- read.csv("nonbots_data.csv")
str(nonbots)

intersect(names(bots), names(nonbots))
identical(names(bots), names(nonbots))

Data <- merge(bots , nonbots,  by= intersect(names(bots), names(nonbots)), all= TRUE)
