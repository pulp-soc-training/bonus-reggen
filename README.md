# Instructions
We are assuming you run on a centos 7 machine (with `python3.6` from EPEL).

There is a *symlink to the regtool.py script in this directory*.

## *Python dependencies to run* `./regtool.py`
```
python3.6 -m pip install --user hjson
python3.6 -m pip install --user mistletoe
python3.6 -m pip install --user mako
```

## Documentation of `./regtool.py`

```
https://docs.opentitan.org/util/reggen/README/
https://docs.opentitan.org/doc/rm/register_tool/

```

## Example hjson description

`example/gpio_example.hjson` is an example how a more complicated `hjson` description
could look like.


## Generating C header files with `./regtool.py`

```
python3.6 ./regtool.py --cdefines example/gpio_example.hjson  --outdir sv/
```

## Generating SystemVerilog files with `./regtool.py`
```
python3.6 ./regtool.py -r example/gpio_example.hjson  --outdir sv/
```

