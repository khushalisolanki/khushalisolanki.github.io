# khushalisolanki.github.io
> R code for PCA a machine learning technique used in wine quality dataset.
```
wine_data=read.csv("C:/Users/Khushali/Downloads/winequality-red - winequality-red.csv")
head(wine_data)
summary(wine_data)
pc.wine<- princomp(wine_data,cor=TRUE)
pc.wine
summary(pc.wine)
eigenvectors<- pc.wine$loadings
eigenvectors
eigenvalues<- pc.wine$sdev*pc.wine$sdev
eigenvalues
screeplot(pc.wine,type="l",main="Scree Plot of PCA")
abline(1,0, col="blue", lty=2)
```
And results for this are given below:
> pc.wine

Call:
princomp(x = wine_data, cor = TRUE)

Standard deviations:

   Comp.1    Comp.2    Comp.3    Comp.4    Comp.5    Comp.6    Comp.7    Comp.8    Comp.9   Comp.10   Comp.11   Comp.12 
   
1.7666827 1.4972916 1.2972739 1.1022799 0.9865412 0.8139977 0.7863319 0.7112472 0.6413326 0.5726425 0.4245216 0.2439629 

 12  variables and  1599 observations.
 
 > eigenvalues
 
 Comp.1     Comp.2     Comp.3     Comp.4     Comp.5     Comp.6     Comp.7     Comp.8     Comp.9    Comp.10    Comp.11    Comp.12 
 
 3.12116770 2.24188204 1.68291969 1.21502087 0.97326362 0.66259224 0.61831780 0.50587256 0.41130754 0.32791939 0.18021863 0.05951792 

![image](https://user-images.githubusercontent.com/118449918/206855018-55a41215-f6b0-4dd6-b4ac-778acef8f3c9.png)
