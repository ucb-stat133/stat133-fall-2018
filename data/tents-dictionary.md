
## Data dictionary for file `tents.RData`

Here's the description of the R objects in `tents.RData`:

  - tent:     name of camping tent (`character`)
  - brand:    brand (`character`)
  - price:    price in dollars (`double`)
  - weight:   weight in grams (`double`)
  - height:   height in cms (`integer`)
  - bestuse:  suggested use (`character`)
  - season:   seasons classification (`character`)
  - capacity: number of persons sleeping comfortably (`character`)


Although each object has its own data type, you can think of each of them as a variable from a statistics standpoint like so:

| Object     | Variable     |
|:-----------|:-------------|
| `tent`     | categorical  |
| `brand`    | categorical  |
| `price`    | quantitative |
| `weight`   | quantitative |
| `height`   | quantitative |
| `bestuse`  | categorical |
| `season`   | categorical |
| `capacity` | categorical/quantitative |
