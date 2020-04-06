# litex-data-cpu-mor1kx

Non-Python data files required to use the mor1kx with
[LiteX](https://github.com/enjoy-digital/litex.git).

The data files can be found under the Python module `litex.data.cpu.mor1kx`. The
`litex.data.cpu.mor1kx.location` value can be used to find the files on the file system.
For example;

```python
import litex.data.cpu.mor1kx

my_data_file = "abc.txt"

with open(os.path.join(litex.data.cpu.mor1kx.location, my_data_file)) as f:
    print(f.read())
```


The data files come from https://github.com/openrisc/mor1kx.git
and are imported using `git subtrees` to the directory
[litex/data/cpu/mor1kx/verilog](litex/data/cpu/mor1kx/verilog).



## Installing

## Manually

You can install the package manually, however this is **not** recommended.

```
git clone https://github.com/litex-hub/litex-data-cpu-mor1kx.git
cd litex-data-cpu-mor1kx
sudo python setup.py install
```

## Using [pip](https://pip.pypa.io/)

You can use [pip](https://pip.pypa.io/) to install the data package directly
from github using;

```
pip install --user git+https://github.com/litex-hub/litex-data-cpu-mor1kx.git
```

If you want to install for the whole system rather than just the current user,
you need to remove the `--user` argument and run as sudo like so;

```
sudo pip install git+https://github.com/litex-hub/litex-data-cpu-mor1kx.git
```

You can install a specific revision of the repository using;
```
pip install --user git+https://github.com/litex-hub/litex-data-cpu-mor1kx.git@<tag>
pip install --user git+https://github.com/litex-hub/litex-data-cpu-mor1kx.git@<branch>
pip install --user git+https://github.com/litex-hub/litex-data-cpu-mor1kx.git@<hash>
```

### With `requirements.txt` file

Add to your Python `requirements.txt` file using;
```
-e git+https://github.com/litex-hub/litex-data-cpu-mor1kx.git
```

To use a specific revision of the repository, use the following;
```
-e https://github.com/litex-hub/litex-data-cpu-mor1kx.git@<hash>
```