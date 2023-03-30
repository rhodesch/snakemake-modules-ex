# snakemake-modules-ex
Snakemake modules examples

Toy example that incorporates 2 snakemake modules into a larger workflow.


### Background

Independent snakemake workflows:
- hello
- goodbye

Main snakemake workflow imports independent workflows as modules (conceptually similar to snakemake subworkflows):
- hello-goodbye

Each workflow, including the main/merged workflow, use snakemake's suggested directory structure [here](https://snakemake.readthedocs.io/en/stable/snakefiles/deployment.html#). A results directory will be created during execution of each snakemake workflow, e.g. `hello`, `goodbye`, `hello-goodbye`.


### Instructions

Assumes snakemake has been installed. If not, refer to documentation [here](https://snakemake.readthedocs.io/en/stable/getting_started/installation.html) 

Clone repository and move into cloned directory
```
git clone git@github.com:rhodesch/snakemake-modules-ex.git
cd snakemake-modules-ex
```

Move into main workflow directory
```
cd hello-goodbye
```

Alternatively, move into the component/subworkflow workflow directories
```
cd hello
```
or
```
cd goodbye
```

Test workflow with default values
```
snakemake -n
```

Execute workflow with default values
```
snakemake -j 1
```


### Directory structure

The example workflows use Snakemake's suggested workflow directory structure, [here](https://snakemake.readthedocs.io/en/stable/snakefiles/deployment.html)

### Relative paths

Refer to Snakemake documentation for detailed information about relative paths, [here](https://snakemake.readthedocs.io/en/stable/project_info/faq.html#how-does-snakemake-interpret-relative-paths)

Of note:
- Snakefile paths for each module are relative to the currently evaluated Snakefile. In the first example above, that would be located `hello-goodbye/workflows/Snakefile`

Params paths are relative to the working directory. In the first example above, that would be located `hello-goodbye`
