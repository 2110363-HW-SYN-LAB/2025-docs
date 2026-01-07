## Icarus Verilog and GTKWave Installation

### Windows
Download Icarus Verilog and GTKWave from this link: https://bleyer.org/icarus/. For Windows, GTKWave comes with iverlog, so no need to install GTKWave by yourself.
### MacOS
You can install Icarus Verilog using Homebrew:

```bash
brew install icarus-verilog
```

Sadly, some MacOS do not support GTKWave. Try these methods:
- Try to install GTKWave by following these steps in the [official wiki](https://gtkwave.github.io/gtkwave/install/mac.html). You may have to compile GTKWave by yourself.
- If it does not work, you may use other applications such as [Surfer](https://app.surfer-project.org/). You can import .vcd or .fst files into the website.

### Linux
  You can install Icarus Verilog and GTKWave using package manager, e.g.
```bash
sudo apt install iverilog gtkwave
```

### Verifying
Check if Icarus Verlog works or not by running:

```bash
iverilog
```

It should show some messages like this:
	
```bash
iverilog: no source files.
Usage: iverilog [-EiSuvV] [-B base] [-c cmdfile|-f cmdfile]
                [-g1995|-g2001|-g2005|-g2005-sv|-g2009|-g2012] [-g<feature>]
                [-D macro[=defn]] [-I includedir] [-L moduledir]
                [-M [mode=]depfile] [-m module]
                [-N file] [-o filename] [-p flag=value]
                [-s topmodule] [-t target] [-T min|typ|max]
                [-W class] [-y dir] [-Y suf] [-l file] source_file(s)
See the man page for details.
```

## Cocotb Installation
You can follow the instructions from this link. However, we recommend using Conda to separate the environment from the other ones. If you want to use Conda, you can follow the steps below.

1. Install Miniconda by following steps on this official website (Some of you may have already installed Miniconda, you can skip this step). To verify your installation, you can check by running this command in your terminal, it should show your installed Conda’s version.
```bash
conda –-version
```

2. Create a new environment, let’s name it “cocotb”, with Python version 3.10.
```bash
conda create -n cocotb python=3.10
```
Activate your created environment.
```bash
conda activate cocotb
```
Now, your prompt should have an environment name at the front like this.

![Image title](/2025-docs/installation/image1.png){ loading=lazy }

4. Install tools related to GNU Make.
```bash
conda install -c msys2 m2-base m2-make
```
5. Install Cocotb and Pytest libraries.
```bash
pip install cocotb pytest
```
