
GPT-3.5 Code Documentation Repository
=====================================



 This repository showcases the use of OpenAI's GPT-3.5 language model for
 generating documentation for code automatically. The generated documentation
 is then turned into a "doc as code" site for easy access and sharing.
 


Getting Started
---------------


To use this repository, you will need to have the following:


* A valid OpenAI API key for GPT-3.5 language model.
* A codebase that you want to generate documentation for.


Usage
-----


1. Clone or download this repository to your local machine.
2. Set up your OpenAI API key by creating a `.env` file in the
 root directory and adding the following line, you can rename the example.env:
 

```
OPENAI_API_KEY=<your-api-key>
```
1. Install the required dependencies, [python](https://www.python.org/downloads/), then once installed use the following command:



```
cd ./MKAutoDocs/
pip install -r requirements.txt
```
4. Edit the configuration file to point to your code repository.
   1. docs_path: relative path to the desired doc folder (should match with mkdocs in config file).
   2. root_dir: absolute path or relative path to the desired project root directory.
   3. source_to_document:
       - Absolute path or relative path to the folders you want parsed and documented in your root directory.
   4. requirements: A list of python dependencies to run your doc as code site.
       - mkdocs: 1.4.2
       - pymdown-extensions: 9.11
   5. ignore_folders: A list of regex of folders/subfolders to ignore. Remove any or all if you like.
       - .+\.git
       - \.pytest
       - Include
       - Lib
       - Scripts
   6. ignore_files:  A list of regex of files to ignore. Remove any or all if you like.
       - __.*__
       - ^(?!.*\.py$).*
   7.   use_state: A boolean value, this will keep files from being regenerated on each run. Feel free to turn off if you want to update the docs.
5. Run the following command to generate documentation for your code:


```
python Auto_Doc.py
```


 This will use the GPT-3.5 language model to generate documentation for
 your codebase and output the generated documentation as Markdown files
 in the configured `docs` directory.
1. Run The static site generator 
 [MkDocs](https://www.mkdocs.org/) to turn the
 generated documentation into a "doc as code" site.
 



 For example, to use MkDocs, run the following command in the root
 directory to preview the site:
 



```
mkdocs serve
```

 Or use MkDocs, to build a site:

```
mkdocs build
```

 This will generate a static website in the `site` directory,
 which you can host on a server or a service like GitHub Pages.

 If you want to host on GitHub Pages. You can set up github actions to autodeploy your doc as code site [mkdocs how to](https://www.mkdocs.org/user-guide/deploying-your-docs/) or deploy manually using:

 ```
mkdocs gh-deploy
 ```



Contributing
------------



 If you want to contribute to this repository, please feel free to open a
 pull request or an issue. We welcome any feedback, suggestions, or
 improvements to the code.
 


License
-------



 This repository is licensed under the MIT License. See the
 `LICENSE` file for more information.
 



