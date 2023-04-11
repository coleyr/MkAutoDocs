# `auto_doc.py` Module

The `auto_doc` module is a Python code export optimised for auto generating documentation in [MkDocs](https://www.mkdocs.org/).

## Dependencies

OpenAI, YAML, os, pathlib, dotenv and re.

## Functions

### `chat_completion(user:str, system:str, model:str="gpt-3.5-turbo", temperature=None, max_tokens=None)->openai.ChatCompletion.create:`

Generates chat completions using Open AI's Chat model API. 

#### Inputs

* `user:str`: The user's input to generate a response.
* `system:str`: The response provided by the Chat model API.
* `model:str`: The name of the model to use for generating completions. The first time you use a new model, OpenAI will cache the model to your computer, so it may take a short amount of extra time to generate the first completion. Defaults to "gpt-3.5-turbo".
* `temperature=None`: What sampling temperature to use. Higher values means the model will take more risks. Try 0.9 for more creative applications, and 0 (argmax sampling) for ones with a well-defined answer.
* `max_tokens=None`: The maximum number of tokens(common sequences of characters found in text) to generate in the completion. If both duration and max_tokens are set, the API will return whichever response is generated first. 

#### Output

OpenAI ChatCompletion.create object.

### `folder_structure(path:str) -> dict:`

Returns a dictionary of the file and folder structure from the folders.

#### Inputs

* `path:str`: The path to the folder.

#### Output

Dictionary of the file and folder structure.

### `write_md_documentation(code: str) -> str:`

Returns a string of markdown format from a given python code.

#### Inputs

* `code: str`: The python code to generate the documentation for.

#### Output

Returns a string of markdown format.

### `make_dir(path)`

Method creates a directory.

#### Inputs

* `path:str`: The path to create the directory in.

### `ignore_checks(path_string)`

Method checks if the path_string regex can be ignored.

#### Inputs

* `path_string:str`: The path of the string value to check.

### `make_save_folder(folder:str, root_dir:str, docs_path:str) -> Path`

Returns Path Object.

#### Inputs

* `folder:str`: The name of the folder.
* `root_dir:str`: The root directory.
* `docs_path:str`: Path in the document directory.

#### Output

Returns Path Object.

### `get_file_documentation(files:list, save_path:Path) -> None:`

Method to create an MD file for the given file.

#### Inputs

* `files:list`: The files to create documentation for.
* `save_path:Path`: The path to the directory to save MD files in.

### `get_markdown(source_folder_dir:dir, save_folder:Path, root_doc:str, docs_path:str):`

Method to generate markdown and access nested directories.

#### Inputs

* `source_folder_dir:dir`: The directory to create documentation for.
* `save_folder:Path`: The path to the directory to save MD files in.
* `root_doc:str`: The path to the root directory.
* `docs_path:str`: The folder structure and paths.

### `make_mkdocs_yaml(root_dir:str) -> None:`

Generates mkdocs.yml.

#### Inputs

* `root_dir:str`: The root directory.

### `update_requirements(requirement: str, version: str, file_path: str = "requirements.txt")->None:`

Updates versions in requirements.txt.

#### Inputs

* `requirement:str`: The required package.
* `version`: The version of the package.
* `file_path:str = requirements.txt`: The file path for the `requirements.txt` file.

### `make_mkdocs_documents():`

Generates the documentation.