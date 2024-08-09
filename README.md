<h1 align="center" style="font-size: 3em;">Generate Difference</h1>

### Hexlet tests and linter status:
[![Actions Status](https://github.com/Dema63/python-project-50/actions/workflows/hexlet-check.yml/badge.svg)](https://github.com/Dema63/python-project-50/actions)
[![Maintainability](https://api.codeclimate.com/v1/badges/63e87e9e0b1416478930/maintainability)](https://codeclimate.com/github/Dema63/python-project-50/maintainability)
[![Test Coverage](https://api.codeclimate.com/v1/badges/63e87e9e0b1416478930/test_coverage)](https://codeclimate.com/github/Dema63/python-project-50/test_coverage)

---

Generate Difference-This is a universal program created within the framework of the Hexlet educational process, which takes as input the path to configuration files and returns a description of the differences between the structures of these files. 
Using the gendiff tool eliminates the need for an additional and original copy of the directory.

* Format support: json/yaml
* Generating reports: plain, stylish, json

---

### Program capabilities:

* Comparison of flat files (JSON)
* Comparison of flat files (YAML)
* Recursive comparison
* Flat format
* Output to JSON

---

## How to install:

```bash
git clone https://github.com/Dema63/python-project-50
cd python-project-50/
make package-install
```

---

### Instructions for comparing files: 
Users have two ways to compare files - from the root directory of the project or directly from the directory where the files being compared are located. The choice of method depends on 
where you are in the file system:
1. From the project root directory:
Specify a relative path from the root directory to the files. For example, if you are at the root of your project and the files are located in the tests/fixtures subdirectory, use the following 
command:
```sh
gendiff tests/fixtures/file1.json tests/fixtures/file2.json
``` 
2. From the files directory:
If you are in the same directory as the files being compared, you can run gendiff specifying only the file names. For example:
```sh
gendiff file1.json file2.json
```
Below are the commands to start comparing files from the directory where the files themselves are located.

---

### Help output:
To display help, use the command:
```sh
gendiff -h
```

[![asciicast](https://asciinema.org/a/1slmrh61FmEormRgVPlC09HvZ.svg)](https://asciinema.org/a/1slmrh61FmEormRgVPlC09HvZ)

---

### Comparison of flat files (JSON):
The comparison is based on how the content in the second file has changed relative to the first, allowing you to quickly identify changes in the data structure of JSON files.
To compare two files, use the command:
```sh
gendiff flat_file1.json flat_file2.json
```

[![asciicast](https://asciinema.org/a/n4jLTe1LPLAJWzy3r1DfQFxy2.svg)](https://asciinema.org/a/n4jLTe1LPLAJWzy3r1DfQFxy2)

---

### Comparison of flat files (YAML):
Find differences between two simple, single-level YAML files without nested structures. Easy-to-read syntax helps you quickly navigate the differences between files. 
To compare two files, use the command:
```sh
gendiff flat_file1.yml flat_file2.yml
```

[![asciicast](https://asciinema.org/a/0xnar2Z6Cl1ufjgijWmkwYz7N.svg)](https://asciinema.org/a/0xnar2Z6Cl1ufjgijWmkwYz7N)

---

### Recursive comparison:
This diff example describes what happened to each key in the diff. For example, whether it was added, changed or deleted.
To compare two files, use the command:
```sh 
gendiff file1.json file2.json
```

[![asciicast](https://asciinema.org/a/GnDWjPGgSHYq42f5kSLXJCR8J.svg)](https://asciinema.org/a/GnDWjPGgSHYq42f5kSLXJCR8J)

---

### Flat format:
Plain format represents data in a linear form. 
This is ideal for visual reference to differences between files, as well as for simple text reports if there is no need for additional parsing.
To compare two files, use the command:
```sh
gendiff --format plain file1.json file2.json
```

[![asciicast](https://asciinema.org/a/qvYaPIVGFV8G3O25xMNAxh6YO.svg)](https://asciinema.org/a/qvYaPIVGFV8G3O25xMNAxh6YO)

---

### Output to JSON:
This output is convenient for wide use, since the JSON format is supported by all modern programming languages. It is easy to parse and process data using the many available libraries and tools. JSON supports complex data structures such as nested objects and arrays, allowing you to accurately and completely represent data.
To compare two files, use the command:
```sh
gendiff --format json file1.json file2.json
```

[![asciicast](https://asciinema.org/a/UviHG4QVVAWHmRe9JMRBJ3N44.svg)](https://asciinema.org/a/UviHG4QVVAWHmRe9JMRBJ3N44)