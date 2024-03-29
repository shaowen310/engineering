# Conda

## Installation

Miniconda installation guide: [doc](https://docs.conda.io/en/latest/miniconda.html)

## Environment Management

### Create environment

```
conda create --name myenv python=3.7
```

### List environments

```
conda info -e
```

### Remove environment

```
conda remove -n myenv --all
```

### Rename environment (work around)

```
conda create --name new_name --clone old_name
conda remove --name old_name --all
```

### Update environment

```
conda update --all
```

### Clean cache

```
conda clean -a
```

### Don't activate base environment automatically

```
conda config --set auto_activate_base false
```

### Hide environment info

```
conda config --set changeps1 False
```

## Update installation location

1. Move installation folder
2. Download conda installer
3. Run script with `-u` parameter

## Launch shell with Conda environment

### PowerShell

```
powershell.exe -ExecutionPolicy ByPass -NoExit -Command & 'conda\\shell\\condabin\\conda-hook.ps1' ; conda activate 'conda' ; cd ~ 
```

## Use Conda with Visual Studio Code

### Numpy DLL not found

Reasons:

1. Not launching vscode from anaconda-prompt. Environment variable is not set.
2. Installing numpy using pip. Anaconda environment uses a different installation folder. Should install numpy using command `conda install numpy`.
