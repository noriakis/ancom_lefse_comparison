# ancom_lefse_comparison
Comparing ANCOM and LEfSe for differential abundance testing.

## Input data
Sample input file provided in wikipedia of LEfSe. I removed class Mid_O2, thus comparing Low_O2 and High_O2 
(hmp_small_aerobiosis.txt, https://bitbucket.org/biobakery/biobakery/wiki/lefse).

## LEfSe
All level
- Without subclass
- With subclass (body_site)

```
format_input.py hmp_lefse_sub.txt ./lefse.lefse -f r -u 2 -c 1 -o 1000000
run_lefse.py -s 0 --verbose 0 -l 2 --wilc 0 -b 100 -r lda ./lefse.lefse ./lefse.sub.res

format_input.py hmp_lefse_all.txt ./lefse.lefse -f r -u 3 -c 1 -s 2 -o 1000000
run_lefse.py -s 0 --verbose 0 -l 2 --wilc 1 -b 100 -r lda ./lefse.lefse ./lefse.all.res
```

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