# Project Idea: jsonToClass — Zero-effort Python Classes from API JSON

## Purpose:
Automatically generate Python classes from API JSON responses so that developers can directly import the class and use attributes, without any manual mapping or extra code.

MVP Workflow:

1. Developer writes in define_classes.py:
- `CreateClass("Me", "/me")`

2. When run run define_class.py:

- CreateClass Sends a request to /me

- Fetches and decodes the JSON response

- Generates a Python file me.py in Classes/ folder with a class Me containing fields matching the JSON keys


3. In the project, the developer can import and use the class directly:

- `from Classes.me import Me`
- `print(Me.name)  # works immediately, no extra mapping`


## Key Features (MVP):

- One-time code generation; no runtime initialization needed

- Direct access to all API fields as class attributes

- Basic types only (str, int, float, bool, list)

- Supports IDE autocomplete and type checking (Pylance-friendly)


## Why it’s useful:

- Eliminates boilerplate mapping from JSON → dict → attributes

- Reduces runtime errors from typos

- Makes working with APIs feel like working with normal Python objects

