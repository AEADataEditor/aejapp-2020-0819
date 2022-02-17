# Reproducing aejapp-2020-0819

## Purpose

Build a container to reproduce the analysis in aejapp-2020-0819.

## Source

- [https://github.com/AEADataEditor/stata-project-with-docker](https://github.com/AEADataEditor/stata-project-with-docker) for the setup
- [http://doi.org/10.3886/E151441V1](http://doi.org/10.3886/E151441V1) (pre-print version as of 2022-02-17)

## Requirements

You will need 

- [ ] A Stata license file `stata.lic`. You will find this in your local Stata install directory.
- [ ] [Docker](https://docs.docker.com/get-docker/) or [Singularity](https://github.com/sylabs/singularity/releases). 


## Steps

0. For detailed instructions, see the [AEADataEditor/stata-project-with-docker](https://github.com/AEADataEditor/stata-project-with-docker) repository
1. Clone
2. Download [http://doi.org/10.3886/E151441V1](http://doi.org/10.3886/E151441V1) 
3. Unzip. The resultant directory structure should look like this:
```
aejapp-2020-0819/
    run.sh
    ...
    V2/
       (contents of the ZIP file)
```
4. Execute `run.sh V2/code/master.do`. This will re-use the [existing Docker image](https://hub.docker.com/r/aeadataeditor/aearep-2656).
5. If you wish to rebuild the Docker image, edit `init.config.txt`, remove `config.txt`, and run `build.sh`.

