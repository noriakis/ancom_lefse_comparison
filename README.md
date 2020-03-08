# ancom_lefse_comparison
Comparing ANCOM and LEfSe for differential abundance testing.

## Input data
Sample input file (hmp_small_aerobiosis.txt) provided in wikipedia of LEfSe (https://bitbucket.org/biobakery/biobakery/wiki/lefse). I removed class Mid_O2, thus comparing Low_O2 and High_O2.

## LEfSe
All level
- Without subclass
- With subclass (body_site)

## ANCOM
Used R scripts for ANCOM (https://github.com/FrederickHuangLin/ANCOM).
Modifed to reject null hypothesis by setting W threshold automatically.
Genus only
- Without covariate
- With covariate (body_site)

## Visualization
ComplexHeatmap (https://github.com/jokergoo)  
firatheme (https://github.com/vankesteren/firatheme/)

![volcano_plot](https://raw.githubusercontent.com/nrsat/ancom_lefse_comparison/master/volcano_plot.png)
![upset_plot](https://raw.githubusercontent.com/nrsat/ancom_lefse_comparison/master/upset_plot.png)