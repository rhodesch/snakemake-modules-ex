# snakemake-modules-ex
Snakemake modules examples

Toy example that incorporates 2 snakemake modules into a large workflow.

Independent modules (similar to subworkflows):
- hello
- goodbye

merged workflow:
- hello-goodbye

Uses snakemake's suggested directory structure [here](https://snakemake.readthedocs.io/en/stable/snakefiles/deployment.html#)

Use:

clone repository and move into cloned directory
```
git clone git@github.com:rhodesch/snakemake-modules-ex.git

cd snakemake-modules-ex
```

move into any workflow directory, e.g. `hello`, `goodbye`, `hello-goodbye`.
```
cd hello-goodbye
```

test workflow with default values
```
snakemake -n
```

execute workflow with default values
```
snakemake -j 1
```
