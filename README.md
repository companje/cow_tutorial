# cow_tutorial
[CoW](https://github.com/CLARIAH/COW) is a csv to Linked Data converter with user documentation [here](https://github.com/clariah/cow/wiki) and developer documentation in [readthedocs](https://csvw-converter.readthedocs.io/en/latest/) and [pypi](https://pypi.org/project/cow-csvw/). 
CoW is intended for anyone who has Python installed, can use the command line and can edit a text file.

### getting started
Open a terminal and follow the commands below. [Call for help](https://github.com/CLARIAH/COW/issues/new), if you get stuck.

#### in a terminal clone this repository
git clone https://github.com/rlzijdeman/cow_tutorial.git
cd cow_tutorial

#### next install cow using [pypi](https://pypi.org/project/cow-csvw/)
pip3 install cow-csvw

#### create metadata file (the recipe)
cow build db_harderwijk_1888_1909.csv

#### inspect the metadata-json or edit it. for help see https://github.com/clariah/cow/wiki
less db_harderwijk_1888_1909.csv-metadata.json

#### create triples from the csv using the metadata.json file as recipe
cow_tool convert db_harderwijk_1888_1909.csv

#### inspect triples
less db_harderwijk_1888_1909.csv.nq
