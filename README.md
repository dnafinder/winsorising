# Winsorising
Winsorising extreme values.<br/>
Winsorising or Winsorization is the transformation of statistics by
limiting extreme values in the statistical data to reduce the effect of
possibly spurious outliers. It is named after the engineer-turned-biostatistician 
Charles P. Winsor (1895–1951). The effect is the same as clipping in 
signal processing. The distribution of many statistics can be heavily 
influenced by outliers. A typical strategy is to set all outliers to a
specified percentile of the data; for example, a 90% Winsorisation would
see all data below the 5th percentile set to the 5th percentile, and data
above the 95th percentile set to the 95th percentile. Winsorised
estimators are usually more robust to outliers than their more standard
forms, although there are alternatives, such as trimming, that will
achieve a similar effect. Note that Winsorizing is not equivalent to
simply excluding data, which is a simpler procedure, called trimming. 
In a trimmed estimator, the extreme values are discarded; in a Winsorized
estimator, the extreme values are instead replaced by certain percentiles
(the trimmed minimum and maximum).  
Thus a Winsorized mean is not the same as a truncated mean. For instance,
the 5% trimmed mean is the average of the 5th to 95th percentile of the
data, while the 90% Winsorised mean sets the bottom 5% to the 5th
percentile, the top 5% to the 95th percentile, and then averages the data   

Syntax:<br/>
          Y=WINSORISING(X,W)

          X - data matrix or vector
          For vectors, WINSORISING(X) is the winsorized X array. 
          For matrices, WINSORISING(X) is a matrix containing the 
          winsorized element from each column. 

          W - Amount of winsoritazion (90 by default). If you set W=90 this 
          means that the remaing 10% (0-5th percentile and 95-100th
          percentile) will be substituted.

     Example: 

x=[92 19 101 58 103 91 26 78 10 13 0 101 86 85 15 89 89 25 2 41];

          Calling on Matlab the function: winsorizing(x)

          Answer is:

y=92 19 101 58 102 91 26 78 10 13 1 101 86 85 15 89 89 25 2 41

          Created by Giuseppe Cardillo
          giuseppe.cardillo-edta@poste.it

To cite this file, this would be an appropriate format:
Cardillo G. (2011). WINSORISING: WINSORISING Data
http://www.mathworks.com/matlabcentral/fileexchange/
