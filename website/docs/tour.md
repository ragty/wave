---
title: A Tour of Q
---
import StartQ from './_start_q.md'

Your H2O Q release download ships with [over 150 examples](/gallery).

You can play around with these examples in your browser using `tour.py`, a Python script (itself a Q app) located in `examples/`:

```none title="Contents of $HOME/q"
q/
├── docs/           
├── examples/       <-- Examples live here.
|   └── tour.py     <-- The H2O Q Tour.
├── test/           
├── www/            
└── qd              
```

To run the tour, as with any Q app, we need to start both the Q server (`qd`) and the tour (`tour.py`). Let's go ahead and do that.

## Step 1: Start the Q server

<StartQ/>

## Step 2: Run the tour

To run the tour, create a [virtual environment](https://docs.python.org/3/tutorial/venv.html), install the tour's dependencies, and finally execute `tour.py`.  

:::important
Do this from a new terminal window!
:::

```shell 
cd $HOME/q
python3 -m venv venv
./venv/bin/pip install -r examples/requirements.txt
./venv/bin/python examples/tour.py
```

## Step 3: Enjoy the tour

Go to [http://localhost:55555/tour](http://localhost:55555/tour) to access the tour. 

![tour](assets/tour__tour.png)

`tour.py` is an ordinary Q app that runs other apps. The tour itself runs at the route `/tour`, and each of the examples runs at `/demo`. 

:::tip
To play with the tour's active example in isolation, simply open a new browser tab and head to [http://localhost:55555/demo](http://localhost:55555/demo).
:::

## Wrapping up

In this section, we started the Q server and then launched `tour.py` to experience the tour. In general, this is how you'd typically launch any app, including your own. There is nothing special about `tour.py`. In fact, to run any example, all you need to do is repeat the steps above in a new terminal window. For example, to run `todo.py`, simply run:

```shell 
cd $HOME/q
./venv/bin/python examples/todo.py
```

You can now access the example at [http://localhost:55555/demo](http://localhost:55555/demo). Simple!
