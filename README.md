# Rate_of_Change  
  
  
Take a current weight = cw = 2, let's assume the new weight is = nw = 3 and the rate after change is 3 / 2 = 1.5, so the rate of change is 1.5.
  
  Squared we can handle negative values too, the new square rate of change is 3 * 3 / 2 * 2 = 2.25. 
A bit bigger, so I was asking me how big must be a value, that all rate of changes can pass to update the weights in a neural network.
Starting with a fixed setup I increased the value till there was no change in the prediction anymore.

That was the condition where every weight in the neural network was updated like without this condition.
```
    if (weightSquaredNew / weightSquaredOld < 1000000000000)
    {
       // update weights
    }

```

  
And this was the condition where the prediction was changed and some weights was stopping the update process.
```
    if (weightSquaredNew / weightSquaredOld < 100000000000)
    {
       // update weights
    }

```

So some square rate of changes are more than this value = 100.000.000.000, crazy or?
And more crazy was the fact that an incredibly small rate was also performing well like the big value 100.000.000.000 or without using a rate of change.

The moral of the story is that in a neural network a lot of things going on and to train a neural network is possible in so many ways.
From a perspective of gain there was no progress, it is not clear to say anything that would make sense about this experiment, it was just an accomplice to mystify neural networks more.


