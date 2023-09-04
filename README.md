# Influxify: Convert CSV to InfluxDB Line Protocol

[![PyPI](https://img.shields.io/pypi/v/influxify.svg)](https://pypi.org/project/influxify/)
[![Python Versions](https://img.shields.io/pypi/pyversions/influxify.svg)](https://pypi.org/project/influxify/)
[![License](https://img.shields.io/github/license/saniauzma/influxify)](https://github.com/saniauzma/Influxify/blob/main/LICENSE)

**Influxify** is a Python package that simplifies the process of converting time-series data from a CSV file into the InfluxDB Line Protocol format. With Influxify, you can seamlessly import your existing data into InfluxDB for efficient storage and analysis.

## Features

- Easily convert CSV data to InfluxDB Line Protocol format.
- Supports custom field and tag mappings for flexible data transformation.
- Can write data into a .lp (Line Protocol) file for convenient import into InfluxDB by simply dragging the file into a bucket.
- Compatible with Python 3.6+.
- Open-source and available under the MIT License.


## Installation

You can install Influxify via pip:

```sh
pip install influxify
```

## Usage

Influxify simplifies the process of converting time-series data from a CSV file into InfluxDB Line Protocol format. Follow these steps to get started:

1. Import the `InfluxConverter` class in your Python script:

```python
from influxify import InfluxConverter
```


2. Initialize the converter:

```python
converter = InfluxConverter('csv_file_name.csv', 'measurement', ['tag_columns'], ['field_columns'], 'timestamp_column', 'timestamp_format')
```

3. Convert the CSV data to InfluxDB Line Protocol format:

```python
line_protocols = converter.convert_csv_to_lineprotocol()
```

4. Optionally, write the converted data into a (.line or .lp or .txt) file for easy import into InfluxDB by dragging the file into a bucket:

```python
lp_file_path = "path/to/save/data.lp"
converter.write_to_lp_file(lp_file_path, line_protocols)
```

5. Now, you can use the generated `line_protocols` to insert data into InfluxDB or use the line protocol file for quick and convenient import.


# Contributing
We welcome contributions from the community! If you'd like to contribute to Influxify.

# License
Influxify is distributed under the MIT License. See [LICENSE](https://github.com/saniauzma/Influxify/blob/main/LICENSE) for more information.

# Support
If you have any questions, issues, or feature requests, please [open an issue](https://github.com/saniauzma/Influxify/issues) on our GitHub repository.
