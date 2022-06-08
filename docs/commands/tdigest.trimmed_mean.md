Get the mean value from the sketch, excluding values outside the low and high cutoff quantiles.

#### Parameters:

* **key**: The name of the sketch.
* **low_cut_quantile**: Exclude values lower than this quantile.
* **high_cut_quantile**: Exclude values higher than this quantile.

@return

@simple-string-reply of mean value from the sketch.
Will return __DBL_MAX__ if the sketch is empty.

@examples

```
redis> TDIGEST.TRIMMED_MEAN t-digest 0.1 0.9
"9.500001"
```