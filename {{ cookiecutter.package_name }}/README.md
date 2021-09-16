# {{ cookiecutter.plugin_name}} plugin for [Tutor](https://docs.tutor.overhang.io)

This README was generated using [cookiecutter-tutor-plugin-poetry](https://github.com/SkillUpTech/cookiecutter-tutor-plugin-poetry/). It includes instructions for:

- Installing this plugin through its git repository
- Managing the development of this plugin using [Poetry](https://python-poetry.org)
- Building the plugin to .whl and .tar formats
- Installing a build of this plugin
- Enabling the plugin in Tutor

You (the creator of this plugin) should ultimately delete this section and replace it with information about your plugin (its purpose, how to use it, etc).

Installation
------------

```bash
pip install git+{{ cookiecutter.git_repo }}
```

Usage
-----

```bash
tutor plugins enable {{ cookiecutter.module_name }}
```

Development
-----------

### Setting Up

First, install poetry on your system using the [official installation instructions](https://python-poetry.org/docs/)
or with the following command:

```bash
curl -sSL https://raw.githubusercontent.com/python-poetry/poetry/master/install-poetry.py | python -
```

Next, clone the {{ cookiecutter.plugin_name }} git repository and enter the directory:

```bash
git clone {{ cookiecutter.git_repo }}.git
cd {{ cookiecutter.package_name }}
```

Now, generate and activate a poetry-managed virtualenv:

```bash
poetry install
poetry shell
```

### Building the Project

Do this each time you make a change to your plugin that you would like to use.

```bash
poetry build
```

### Installing the Built Plugin

If your Tutor installation lives in a separate environment from the Poetry-managed environment created above,
navigate to that environment (for instance, if it is the system-wide environment, just type `exit` from within the poetry shell).
Then, use:

```bash
pip install [the location of your package]/{{ cookiecutter.package_name }}/dist/{{ cookiecutter.module_name }}-[your current version].whl
```

If {{ cookiecutter.plugin_name }} and Tutor live in the same environment, simply using:

```bash
poetry install
```

from within the `{{ cookiecutter.package_name }}` directory should suffice.

For further details on using Poetry, please refer to the [official docs](https://python-poetry.org/docs/).

### Adding the Plugin to Tutor

You should now see `{{ cookiecutter.module_name }}` plugin listed when you type:

```bash
tutor plugins list
```

Use:

```bash
tutor plugins enable {{ cookiecutter.module_name }}
```

to enable it.

License
-------

This software is licensed under the terms of the {{ cookiecutter.license }}.
