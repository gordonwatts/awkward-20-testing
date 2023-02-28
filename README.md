# awkward-20-testing

Trying some stuff out with awkward 2.0 and dask

Specifically - how much of this can work with ServiceX?

## Log

### 2/28/2023

* Looks like the complete schema needs to be known ahead of time
* No obvious way to deal with function calls or method calls (like specifying the jet collection).

In short, this might work if we have to deal with a separate dataset that then turns into `dask` - but the user still has to use `func_adl` to build the dataset. Presumably, some work could be done so that a `dask` call to `cull` means only interesting columns are fetched from `servicex`.
