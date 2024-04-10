# Advanced: Analyse list

## Instructions

Write a function, `analyse_list`, that takes a string and an arbitrarily complex nested list. 

It should build a dictionary where the **keys** are the given string and numbers indicating the index path to each element. The **value** stored on each key should be the value of each list element.

You can assume that the list contains only strings and other nested list.


## Example

```py
random_list = ["carrot", ["car", "boat", "plane"], "turtle", ["house"]]

analyse_list("mabel", random_list)
```

Should return:

```py
{
  "mabel.0":  "carrot",
  "mabel.1.0": "car",
  "mabel.1.1" : "boat",
  "mabel.1.2": "plane",
  "mabel.2": "turtle",
  "mabel.3.0": "house"
}

```