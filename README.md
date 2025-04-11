# OpenBIS-Ontology

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Python Version](https://img.shields.io/badge/python-3.x-blue.svg)](https://www.python.org/downloads/)

OpenBIS-Ontology is a small yet powerful ontology designed to semantically model data from the [openBIS](https://openbis.ch/) system. In addition to the ontology specification, the repository includes a Python-based parser that converts JSON output from the openBIS API into semantic data (e.g., RDF) ready for further integration or querying.

## Overview

Many research groups and laboratories use openBIS for managing complex datasets. However, bridging the gap between raw API outputs and semantic technologies (like linked data and RDF) can be challenging. **OpenBIS-Ontology** addresses this by:

- **Defining a Domain Ontology:** Formalizing the entities, relationships, and concepts inherent to openBIS.
- **Providing a Python Parser:** Transforming JSON data from the openBIS API into semantic data conforming to the ontology.
- **Enabling Data Integration:** Allowing users to integrate openBIS data into semantic web applications, enhancing interoperability and reusability.

## Features

- **Ontology Definition:** An easy-to-extend ontology that encapsulates key openBIS entities.
- **Python-Based Parser:** A tool to convert JSON from openBIS API outputs to RDF or other semantic formats.
- **Extensibility:** Simple integration mechanisms to expand the ontology or update the parser for custom use cases.
- **Validation & Testing:** Unit tests to ensure robust data conversion and ontology compliance.

## Installation

### Prerequisites

- Python 3.6 or later
- [Pip](https://pip.pypa.io/)

### Setup

1. Clone the repository:

   ```bash
   git clone https://github.com/Mat-O-Lab/OpenBIS-Ontology.git
   cd OpenBIS-Ontology
   ```

2. Create and activate a virtual environment (recommended):

   ```bash
   python3 -m venv env
   source env/bin/activate  # On Windows use `env\Scripts\activate`
   ```

3. Install the required dependencies:

   ```bash
   pip install -r requirements.txt
   ```

## Usage

### Parsing openBIS API Output

To convert JSON output from the openBIS API into semantic data using the parser:

1. Place your JSON file in the `examples/` directory (or specify the path to your file).
2. Run the parser:

   ```bash
   python parser/openbis_parser.py --input examples/sample.json --output examples/sample.rdf
   ```

3. The generated semantic data (e.g., in RDF format) will be available at the specified output location.

### Options & Configuration

The parser supports the following command-line options:

- `--input`: Path to the input JSON file.
- `--output`: Path where the converted output will be saved.
- (Optional) Additional flags for verbose logging or custom mapping configurations.

_For detailed information on usage and configuration, refer to the script’s internal help:_

```bash
python parser/openbis_parser.py --help
```

## Development

Contributions are welcome! If you wish to enhance or extend the functionality:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/your-feature`).
3. Commit your changes and push to your branch.
4. Open a pull request describing your changes.

### Running Tests

To run the provided tests:

```bash
pytest tests/
```

Ensure that any new changes maintain compatibility with the existing ontology and parser functionality.

## Contributing

Contributions, issues, and feature requests are welcome. For major changes, please open an issue first to discuss what you would like to change. Please make sure to update tests as appropriate.

## Contact

For questions, bug reports, or further discussions, please open an issue on GitHub or contact the repository maintainers.

## Acknowledgments

- [openBIS](https://openbis.ch/) for the inspiration behind the data management efforts.
- All contributors and the open-source community for their valuable input and collaboration.
