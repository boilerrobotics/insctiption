# Inscription

Knowledge center for Boiler Robotics club.
It is powered by [Jupyter-Book](https://jupyterbook.org/en/stable/intro.html).
The book is hosted by Github page and can be accessed by this [link](https://boilerrobotics.github.io/insctiption/)

## Usage

The Jupyter-Book only requires Python to operate.
Therefore, you should be able to edit and build this book regardless of your operating system.
Check official Python [website](https://www.python.org/downloads/) to download Python if you have not had it installed (or upgrade Python version if you have Python 3.8 or older).

### Building the book

If you'd like to develop and/or build the inscription book, you should:

1. Clone this repository
2. Run `pip install -r requirements.txt` (it is recommended you do this within a virtual environment)
3. (Optional) Edit the books source files located in the `inscription/` directory
4. Run `jupyter-book clean inscription/` to remove any existing builds
5. Run `jupyter-book build inscription/`

A fully-rendered HTML version of the book will be built in `inscription/_build/html/`.

You can preview the book by open the file in your browser.
If you use VS Code, you can use [Live Preview](https://marketplace.visualstudio.com/items?itemName=ms-vscode.live-server) extension.

### Hosting the book

This book (repository) has been configured to be hosted on GitHub Page.
If you want to explore other options or create another book, please see the [Jupyter Book documentation](https://jupyterbook.org/publish/web.html).
If you only intend to edit this book, you can skip this section.

To summarize the work process to create and configure this repository:

1. Install [Jupiter-Book](https://pypi.org/project/jupyter-book/) and [Cookiecutter](https://pypi.org/project/cookiecutter/).
2. Use `jupyter-book create --cookiecutter .` to create a new book.
3. Edit `.github\workflows\deploy.yml` as follow

```
# Upload the book's HTML as an artifact
      - name: Upload artifact
        uses: actions/upload-pages-artifact@v2
        with:
          path: "[your_book_name]/_build/html" <- edit this line
```

4. Config GitHub Page setting to deploy with GitHub Action ([more detail](https://jupyterbook.org/en/stable/publish/gh-pages.html)).
5. Push change(s) to GitHub.

By using Cookiecutter, most of the necessary files will be generated automatically.
You should be able to edit, build, and preview without touching configuration file.
However, GitHub Action configuration needs to be fixed.
By default, the build process will compile html files to `[your_book_name]/_build/html` while GitHub Page will look for those files at `_build/html`.
So, the files won't be found unless you edit the deploy workflow as instructed in step 3.

## Editing

To be continue

## Credits

This project is created using the excellent open source [Jupyter Book project](https://jupyterbook.org/) and the [executablebooks/cookiecutter-jupyter-book template](https://github.com/executablebooks/cookiecutter-jupyter-book).
