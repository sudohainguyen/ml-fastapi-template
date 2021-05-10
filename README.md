
# ML FastAPI template

A Cookiecutter-based code structure template for a simple API to serve ML/DL models using FastAPI.




## Features

- `flake8` for code styling.
- Auto clean code before making commits with `pre-commit`.
- Pre-written Dockerfile.
- Requirements split into multiple files (base, dev, prod).
- Cookiecutter will generate entire FastAPI project based on given info. The project stucture should include:
  - `data`: where ml models or static files stored
  - `envs`: env files for dev, staging or prod environment.
  - `requirements`: python packages requirements
  - `src`: where to put your code

  
## Run Locally

You can either create a virtual env python or use existing one

Install Cookiecutter

```bash
  pip install cookiecutter
```

Clone the project using cookiecutter, while cloning, you need to specify some information such as `project_name` or `short_description`, etc...

```bash
  cookiecutter https://link-to-project
```

Go to the project directory

```bash
  cd [your_project_name]
```

Install dependencies

```bash
  pip install requirements/dev.txt
```

Start the server

```bash
  python src/api.py
```

  
## Deployment

To deploy this project, please use Dockerfile to build image for the API.

```bash
  docker build -t [image_name]:[tag] --build-arg PROD .
```

  
## Running Tests

Recommended to use `pytest` for automation test purposes. All test cases should be placed in `test` folder.

```bash
  pytest -s
```

  
## Contributing

Contributions or suggestions are always welcome! Please feel free to contact me or create new PRs.


  
## Acknowledgements

Inspired by [cookiecutter-spacy-api](https://github.com/microsoft/cookiecutter-spacy-fastapi) and [topdup](https://github.com/forummlcb/topdup).

  