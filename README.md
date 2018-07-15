#######Initial Environment#######
library(quantmod)
library(dplyr)
library(MASS)
library(progress)
library(xts)
library(ggplot2)
library(scales)

##### Functions #####
shift <- function(x, n){
xMat <- as.matrix(x)
c(xMat[-(seq(n))], rep(NA, n))
}

# setwd("/Users/shin-yehhee/Desktop/R") # Home
setwd("C:/Users/yehhee.shin/Desktop/# Temp/0. Stocks") # At work

rm(list = setdiff(ls(), lsf.str()))
invisible(Sys.setlocale("LC_ALL","C"))

###### 2. Extraction ######
TermD = 730; ToD = Sys.Date(); FromD_E = ToD - TermD
TermD = 2; ToD = Sys.Date(); FromD_S = ToD - TermD
# Import
File_name = readline("File name without extension: ")
20180208_Company_List
Clist = read.csv(paste(File_name, ".csv", sep=""))[,3] ### At work
# 20180119_Company_List2
# Clist = read.csv(paste(File_name, ".csv", sep=""))[,1] ### Home


###### 3. Analysis ######
TermD = 730; ToD = Sys.Date(); FromD_A = ToD - TermD
# Setup Variables
n = 3 # width of bound
p = 0.03 # % of bound
#P can be revised by global (maxima-minima) ratio
# Import
File_name = readline("File name without extension: ")
2018-03-13.A
ImportDF = read.csv(paste(File_name, ".csv", sep=""))[,-1] ### At work


###### 4. Prediction ######
TermD = 30; ToD = Sys.Date(); FromD_P = ToD - TermD
