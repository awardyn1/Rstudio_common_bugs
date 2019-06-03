# Rstudio_common_bugs
Dealing with Rstudio bugs for common biodata analysis problems (begginer level)
#This code deals with rJava incompatibility with Rstudo environment due to the differences in their architecture 
#e.g. 64bit vs 32bit
#write.xlsx (part of the readxl library)
#check the version of R studio and Java:

sessionInfo()

#Download compatible- 64-offline Java at:
#https://www.java.com/en/download/manual.jsp
#Then write down the path of new file so you can link rJava to it later
#Instal rJava
install.packages("rJava")

#Then set the path
Sys.setenv(JAVA_HOME="C:/Program Files/Java/jre1.8.0_211/")

#then open the library:
library(rJava)
#check Java verison

system("java -version")

#you should be able to use write.xlsx now whoop whoop
