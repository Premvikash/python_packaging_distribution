# Its simple Python project for packaging and distribution.

### Packaging and distribution
We requires wheel to create built distribution

We requires twine to upload the package into https://pypi.org/manage/project/python_packaging_distribution/releases/

Command to install wheel and twine

``` 
$pip install wheel
$pip install twine
```

Command to create source distribution

```
$python setup.py sdist
```

Command to create the built distribution 

```
$python setup.py bdist_wheel 
```

Command to upload everything under dist once above both source and build package is created to pypi

```
$twine upload dist/*
```
### CI
The file .travis.yml is created for integrating the Travis CI into the github

https://travis-ci.org/

### Documentation
The doc under docs/ will be used to create documentation https://readthedocs.org/, which you can integrate with the github

https://python_packaging_distribution.readthedocs.io/en/latest/index.html

### Cookiecutter
You also can use below project to create the folder structure + the setup.py and setup.cfg file + configuration which will be required for packaging and distribution

https://github.com/audreyr/cookiecutter

Command to run Cookiecutter

```
$cookiecutter https://github.com/audreyr/cookiecutter-pypackage
```

Once you run the above command it will ask for some values, provide those and it will create the structure with configuration  files.

### Travis secure password

We requires travis-encrypt to encryt the password

``
$pip install travis-encrypt
``

Once above done, run the below commnand to update the file .travis.yml with encrypted password, premvikash is my github username and python_packaging_distribution is the github repo name

``
$travis-encrypt --deploy Premvikash python_packaging_distribution /Users/prem/Desktop/codebase/python_packaging_distribution/.travis.yml
``
