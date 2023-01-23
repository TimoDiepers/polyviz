## ``polyviz``: An interface between ``brightway2`` and [D3.js](https://d3js.org/)

This is a Python package that provides an interface between the
[`brightway2`](https://brightway.dev) LCA framework and the [`D3.js`](https://d3js.org) JavaScript library.
It is designed to be used in Jupyter notebooks, and provides
interactive visualizations of LCA results.

<div style="text-align:center">
<img src="https://github.com/romainsacchi/polyviz/raw/main/assets/chord_sample.png" height="300"/>
</div>

This interface extends the capabilities of  [``d3blocks``](https://github.com/d3blocks/d3blocks), a Python package developed
by [Erdogan Taskesen](https://github.com/erdogant).

``polyviz`` allows the following visualizations to be created from LCA results:
* Sankey diagrams ([example 1](https://htmlpreview.github.io/?https://github.com/romainsacchi/polyviz/blob/main/examples/sankey_1.html), [example 2](https://htmlpreview.github.io/?https://github.com/romainsacchi/polyviz/blob/main/examples/sankey_2.html))
* Chord diagrams ([example 1](https://htmlpreview.github.io/?https://github.com/romainsacchi/polyviz/blob/main/examples/chord_1.html), [example 2](https://htmlpreview.github.io/?https://github.com/romainsacchi/polyviz/blob/main/examples/chord_2.html))
* Force-directed graphs ([example 1](https://htmlpreview.github.io/?https://github.com/romainsacchi/polyviz/blob/main/examples/force_1.html), [example 2](https://htmlpreview.github.io/?https://github.com/romainsacchi/polyviz/blob/main/examples/force_2.html))
* Tree maps ([example 1](https://htmlpreview.github.io/?https://github.com/romainsacchi/polyviz/blob/main/examples/treemap_1.html), [example 2](https://htmlpreview.github.io/?https://github.com/romainsacchi/polyviz/blob/main/examples/treemap_2.html))
* Choropleth maps ([example 1](https://htmlpreview.github.io/?https://github.com/romainsacchi/polyviz/blob/main/examples/choro_1.html), [example 2](https://htmlpreview.github.io/?https://github.com/romainsacchi/polyviz/blob/main/examples/choro_2.html))
* Violin plots ([example 1](https://htmlpreview.github.io/?https://github.com/romainsacchi/polyviz/blob/main/examples/violin_1.html), [example 2](https://htmlpreview.github.io/?https://github.com/romainsacchi/polyviz/blob/main/examples/violin_2.html))

## Limitations

Tested only with ``brightway2`` version 2.4.5.

Probably works with version 2.5 too, but not tested.

## Installation

Install ``polyviz`` from PyPI:

```bash
pip install polyviz
```

Usage
-----

### Sankey diagrams

```python
from polyviz import sankey
import bw2data

act = bw2data.get_activity(("some db", "some activity"))
method = ("some method", "some method")
sankey(activity=act, method=method)
```

`sankey()` returns a filepath to an HTML file that can be opened in a browser.

Alternatively, you can track a specific flow:

```python

from polyviz import sankey
import bw2data

act = bw2data.get_activity(("some db", "some activity"))
flow_type = "kilowatt hour"
sankey(activity=act, flow_type=flow_type)
```

Other examples are available in the [examples](github.com/romainsacchi/polyviz/tree/master/examples) folder.

## Support

Do not hesitate to report issues in the Github repository.

## Maintainers

* [Romain Sacchi](https://github.com/romainsacchi)

## Contributing

See [contributing](https://github.com/romainsacchi/carculator/blob/master/CONTRIBUTING.md).

## License

[BSD-3-Clause](https://github.com/romainsacchi/polyviz/blob/master/LICENSE).
