# CSV Merge

A one-file Python script that combines any number of CSV files with the same
columns into one, adding a `filename` column so each row still says where it
came from.

## Run it

```bash
python3 combining_csv_files.py first.csv second.csv third.csv > merged.csv
```

The header is taken from the first file and written once; every row from every
file follows, with the source file name appended as the last column.

```text
id, name, filename
1, Alice, first.csv
2, Bob, second.csv
```

All input files must have exactly the same columns, in the same order. Only
the standard library is used, so there is nothing to install.
