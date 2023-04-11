
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


1. Clone this repository to your local machine.
2. Set up your OpenAI API key by creating a `.env` file in the
 root directory and adding the following line:
 



```
`OPENAI_API_KEY=<your-api-key>`
```
3. Install the required dependencies using the following command:



```
Copy code`pip install -r requirements.txt`
```
4. Add your codebase to the `code` directory.
5. Run the following command to generate documentation for your code:



```
`python Auto_Docs.py`
```


 This will use the GPT-3.5 language model to generate documentation for
 your codebase and output the generated documentation as Markdown files
 in the configured `docs` directory.
6. Use a static site generator like
 [MkDocs](https://www.mkdocs.org/) to turn the
 generated documentation into a "doc as code" site.
 



 For example, to use MkDocs, run the following command in the root
 directory:
 



```
Copy code`mkdocs build`
```


 This will generate a static website in the `site` directory,
 which you can host on a server or a service like GitHub Pages.


Contributing
------------



 If you want to contribute to this repository, please feel free to open a
 pull request or an issue. We welcome any feedback, suggestions, or
 improvements to the code.
 


License
-------



 This repository is licensed under the MIT License. See the
 `LICENSE` file for more information.
 



