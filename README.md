# ECE346
ECE346 Engineering Math Course Web

## How to edit and publish this course web

I recommned [vscode](https://code.visualstudio.com/) to edit and publish it.

- Python 3.10.11

### How to install required Python packages? 
- Open a terminal.
- Navigate to the root folder and find requirements.txt
- run `pip install -r requirements.txt` for Windows machines
- run `pip install -r requirements_linux.txt` for Linux machines
- I recommned using a virtual environment.

### How to build and publish?
- Run the following under the `docs` folder.
- Build: `jupyter-book build --all .`  
- Publish: `ghp-import -n -p -f _build/html` 

### Recommended extensions for vscode
- Python, Python Extension Pack
- Jupyter, MyST-Markdown

### Convert Jupyter notebooks to markdown files
- jupytext notebook.ipynb --to md

### Convert jupyter notebook to markdown
- jupytext https://jupytext.readthedocs.io/en/latest/using-cli.html
- install: pip install jupytext
- How to use: jupytext lab2.ipynb --to md


### Settings inside settings.json
```
{
    "python.envFile": "${workspaceFolder}/.venv",
    "python.terminal.activateEnvInCurrentTerminal": true,
}
```

### To remove version constraints

To remove version constraints from a requirements.txt file (e.g., turning numpy==1.23.4 into numpy), you can use a simple shell command or Python script.
```bash
sed -E 's/[<=>~!]=?.*//' requirements.txt > requirements_no_versions.txt
```
