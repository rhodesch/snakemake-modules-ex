# snakemake-modules-ex
Snakemake modules examples

Toy example that incorporates 2 snakemake modules into a large workflow.

Independent modules (similar to subworkflows):
- hello
- goodbye

merged workflow:
- hello-goodbye

Uses snakemake's suggested directory structure [here](https://snakemake.readthedocs.io/en/stable/snakefiles/deployment.html#)

In the `hello-goodbye` Snakefile, prefixes are different than the module name to emphasize prefixes can be any string. In practice, it would be best to use module names, e.g. 'results/hello' instead of 'results/foo'.
