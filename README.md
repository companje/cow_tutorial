# cow_tutorial
[CoW](https://github.com/CLARIAH/COW) :cow: is a csv to Linked Data converter with [wiki](https://github.com/clariah/cow/wiki) user documentation and developer documentation in [readthedocs](https://csvw-converter.readthedocs.io/en/latest/) and [pypi](https://pypi.org/project/cow-csvw/). 
CoW is intended for anyone who has Python installed, can use the command line and can edit a text file. Examples of CoW conversions can be found [here](https://github.com/CLARIAH/wp4-cow-conversions). CoW is part of the [CLARIAH datalegend ecosystem](https://www.sciencedirect.com/science/article/abs/pii/S1570826818300106?via%3Dihub) and amongst others being used to transpose part of the [Dutch civil registry](https://repository.ubn.ru.nl/bitstream/handle/2066/225728/225728pub.pdf?sequence=1) to Linked Data.

# getting started
Open a terminal and follow the commands below. [Call for help](https://github.com/CLARIAH/COW/issues/new), if you get stuck.


_in a terminal clone this repository_
```
git clone https://github.com/rlzijdeman/cow_tutorial.git
cd cow_tutorial
```

_next install cow using [pypi](https://pypi.org/project/cow-csvw/)_
```
pip3 install cow-csvw
```

_create metadata file (the recipe)_
```
cow_tool build db_harderwijk_1888_1909.csv
```

_inspect the metadata-json or edit it, see [here](https://github.com/clariah/cow/wiki) how to_
```
less db_harderwijk_1888_1909.csv-metadata.json
```

_create triples from the csv using the metadata.json file as recipe_
```
cow_tool convert db_harderwijk_1888_1909.csv
```

_inspect triples_
```
less db_harderwijk_1888_1909.csv.nq
```
