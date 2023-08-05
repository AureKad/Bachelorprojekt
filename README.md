# Bachelorprojekt
The added code is primarly in the RoutePayment class, but there are also some small changes to the PaymentTest class, so we are going to start there.

## PaymentTest
Line 51-57: 8 Epochs for Transaction sizes 50-400. This is done 3 times per protocol as you can see by the i. The i adds a very small amount to the transaction size, so that a new data folder is created instead of an old one being overwritten. 
Transaction size is 100,000, network is Barbarasi-Albert with 25,000 nodes and 6 edges per node, basically all the parameters are the same as described for Figure 2(b) in the paper, besides the total- and endtime being 10,000 instead of 1,000. 

Line 83-87: The parameter values are described that were chosen for the figure in the evaluation. 

Line 89: FUFi1.4 with normal setting. The sleep and wakeup parameters were also added to the constructor. In this case, the 0.009 is the sleep probability and the 0.003 is the wake ip probability. 

## RoutePayment 
Line 39-41: Changed total- and endTime from 1,000 to 10,000 so that forcibally waking up the source and destination node does not impact the average amount of sleeping nodes that much. 

Line 94-95: nodeSleep and nodeWakeUp are added as global variables in the class. 

Line 112-123: nodeSleep and nodeWakeUp are added to the constructor

Line 542: offline array is added. It stores all the nodes that are asleep. 

Line 544-554: The average amount of sleeping nodes is calculated based on the sleep and wakeup probability. Then by using an Index list (has elems from 0 to nodes.length) we can randomly put nodes to sleep. We loop through a for-loop until the avgSleepingNodes amount of nodes are put to sleep. 

Line 563-572: Each node is checked if it falls asleep/wakes up. 

Line 606-610: All the sleeping nodes from the offline array are transferred to the excluded array. 

Line 611: The destination node is forcibly woken up (I removed the src node so that this is less impactful to the total amount of sleeping nodes (though thinking about it I could have also removed the dst node without it impacting the algorithm))
