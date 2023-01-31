# Getting Started

[{% octicon arrow-left height:32 class:"right left" vertical-align:middle aria-label:hi %}](index.md) [{% octicon home height:32 class:"right left" aria-label:hi %}](index.md) [{% octicon arrow-right height:32 class:"right left" aria-label:hi %}](GS_T.md)

----



## Prerequisites

MAGsearcher is implemented to be executed via the command line on linux based systems. This page gives detailed instructions on how to set up the required software to run the tool on Linux and MacOS operating systems. 



### Conda
**Install Miniconda3 latest version** 

A full installation guide for Condo can be found on the [here][https://conda.io/projects/conda/en/latest/user-guide/install/index.html].

> **IMPORTANT**:  Make sure that you select the correct installer for your machine. Here we show how to do it for Linux 

1. Download the installer:

   - [Miniconda installer for Linux](https://docs.conda.io/en/latest/miniconda.html#linux-installers).

     ```
     $ wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
     ```

   - [Anaconda installer for Linux](https://www.anaconda.com/download/).

2. [Verify your installer hashes](https://conda.io/projects/conda/en/latest/user-guide/install/download.html#hash-verification).

3. In your terminal window, run:

   - Miniconda:

     ```
     bash Miniconda3-latest-Linux-x86_64.sh
     ```

   - Anaconda:

     ```
     bash Anaconda-latest-Linux-x86_64.sh
     ```

4. Follow the prompts on the installer screens.

   ```
   Do you accept the license terms? [yes|no]
   [no] >>> yes
   ```

   ```
   Do you wish the installer to prepend the Miniconda3 install location
   to PATH in your /your/home/.bashrc ? [yes|no]
   [no] >>> yes
   ```

   If you are unsure about any setting, accept the defaults. You can change them later.

5. To make the changes take effect, close and then re-open your terminal window.

6. Test your installation. In your terminal window or Anaconda Prompt, run the command `conda list`. A list of installed packages appears if it has been installed correctly.

   

**Updating Anaconda or Miniconda**

Open a terminal window and run

```bash
conda update conda
```






----
 Once all prerequisites have been installed on your system, you can continue with [installing MAGsearcher](GS_T.md)
