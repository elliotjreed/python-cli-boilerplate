# Python Command Line Boilerplate / Example Project

This repository shows a basic setup for a command-line application in Python.

## Getting Started

Python 3 and Pip is expected to be installed on our system.

### Installing Pip

For instructions on how to install Pip visit [pypi.org/project/pip](https://pypi.org/project/pip/).

### Installing

After cloning this repository, change into the newly created directory and run:

```bash
pip install -r requirements.txt
```

Note: if you are on a Debian-based system such as Ubuntu where the default Python version is 2, you will need to use `pip3` in place of `pip`:

```bash
pip3 install -r requirements.txt
```

This will install all dependencies needed for the project from `requirements.txt`. As this is a simple boilerplate, there are no requirements here as we're using just native Python functionality.

## Running the Tests

Unit testing in this project is via Python's built-in unit testing, [unittest](https://docs.python.org/3/library/unittest.html).

All unit tests can be run by executing:

```bash
python -m unittest discover -s tests/
```

Note, if you are on a Debian-based system such as Ubuntu where the default Python version is 2, you will need to use `python3` in place of `python`:

```bash
python3 -m unittest discover -s tests/
```

### Code Coverage

##### Installing coverage

Code coverage reports can be generated via [Coverage.py](https://coverage.readthedocs.io).

`coverage` can be installed by running:

```bash
pip install coverage
```

Note: if you are on a Debian-based system such as Ubuntu where the default Python version is 2, you will need to use `pip3` in place of `pip`:

```bash
pip3 install coverage
```

###### Running coverage

To generate a coverage report, run the tests via `coverage` then generate the report from the results:

```bash
coverage run --source=. -m unittest discover -s tests/
coverage report -m
```

To generate an HTML report:

```bash
coverage run --source=. -m unittest discover -s tests/
coverage html
```

### Testing Approach

The test for the function `say_hello` verifies that the return value of the `say_hello` method returns the string "Hello {name}", where {name} is the value passed through to the function.

The test for the function `run` verifies that the return value of the `run` method returns the string "Hello {name}", where {name} is the value passed through to the function via console input. Here we mock the input one would normally enter in via the command-line by using `patch` to mock the return value of `input` and specify the return value as `Monty`.

## Running the Application

To run the application execute `python main.yml` or `python3 main.yml`.

You should see the text "Hello Monty" being printed.

```bash
python main.yml
```

## Built With

  - [Python](https://www.python.org/)
  - [Pip](https://pypi.org/project/pip/)

## License

This project is licensed under the MIT License - see the [LICENCE.md](LICENCE.md) file for details.

