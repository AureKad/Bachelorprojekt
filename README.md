# Bachelorprojekt
The added code is primarly in the RoutePayment class, but there is some small things that there added to the PaymentTest class, so we are going to start there 

## PaymentTest
Line 51-57: 8 Epochs for Transaction size 50-400. This is done 3 times per protocol as you can see by the i. The i adds a very small amount to the transaction size, so that a new data folder is created instead of an old one being overwritten. 
Transaction size is 100,000, network is Barbarasi-Albert with 25,000 nodes and 6 edges per node, basically all the parameters are the same as described for Figure 2(b) in the paper, besides the total- and endtime being 10,000 instead of 1,000. 

Line 83-87: The parameters are described that were chosen for the figure in the evaluation. 

Line 89: FUFi1.4 with normal setting. The sleep and wakeup parameters there also added to the constructor variables, with in this case the 0.009 being the sleep probability value and the 0.003 being the wake ip probability value. 

## RoutePayment 
Line 
