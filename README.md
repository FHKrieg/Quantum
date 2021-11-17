# Visual analysis of the error term 

In Pennylane the optimizer was showing a weird behaviour (it appeared to be maximizing the error term in stead of minimizing)
 when applied to the dataset we took from here:
<https://archive.ics.uci.edu/ml/datasets/wine+quality>

So we wanted to do a visual analysis of the linear regression dependig on the y-intersect and the gradient in the linear regression.

Conclusion, the step had to be set very small because we have a canyon like shape when looking at the gradient and the y intersect on an equal scale.
The senesetivit for the gradient appears to be much greate when compared to the y intersect. With the step selected to large the optimizer was overcorrecting 
more and more leading to the appearence of the optimzation towards the maximum.

Unfortunately the documentation on the optimzer was semi-optimal, and so we didn't have enough time to investigate how the optimzer actually works.




