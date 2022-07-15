# Overview of useful python resources & common commands.

## Resources
- [PEP-8](https://realpython.com/python-pep8/)
- [Writing Structure](https://docs.python-guide.org/writing/structure/)
- [Google's Python Writing Guide](https://google.github.io/styleguide/pyguide.htm)

## Poetry
navigate to folder in powershell ensure poetry config --list contains the "poetry config virtualenvs.in-project true" if not, add it
>   poetry config virtualenvs.in-project true

Install poetry based on pyproject.toml
>   poetry shell
>   poetry install
>   poetry update
>   code .

Add poetry dependencies
>   poetry add MODULE

Add poetry developer module
>   poetry add -D MODULE

## Common Commands
To activate
> .venv\Scripts\activate

Advanced flake8
> flake8 src --exit-zero --format=html --htmldir reports/flake8 --statistics --tee --output-file reports/flake8/flake8stats.txt

Coverage
>  py -m coverage run -m unittest discover -s tests

> coverage xml -o reports/coverage/coverage.xml

For genbadge (must do both those modules (ie flake8/coverage) commands first)
> genbadge flake8 --output-file ./reports/flake8/badge.svg
> genbadge coverage --output-file ./reports/coverage/badge.svg  


Pre-commit setup

> pre-commit install

> pre-commit run --all-files

> pre-commit autoupdate
