# How to Install Stata 18 on the UKB RAP

Stata can be used on the UKB RAP for analysing data provided you have an active licence. Unfortunately the built-in version of Stata on the RAP is v16, whereas UCL licences are from v17 - v19.

The below instructions will allow you to install Stata 18 on the RAP and link it to an existing UCL licence for use.

## 1. Download Stata to your local machine

Go to https://download.stata.com/download and select "64-bit Stata for Linux on x86-64". This will download a file called "Stata18Linux64.tar.gz" to your computer.

## 2. Upload this file to your UKB-RAP project

This can be done by using the Add > File bottom within the project.

## 3. Start a JupyterLab Job

Open the dialogue box by going to Tools > JupyterLab. Rename job to something meaningful (like Install_STATA for example), assign it to your UKB project, and then In Feature, select "PYTHON_R".

![Jupyter Lab Job Screen](Jupyterlabjob.jpg)

## 4. Install Stata

Once inside JupyterLab, open a terminal window and execute the code below in sequence

```
cd usr/local
mkdir stata18
cd stata18
dx download /path/to/Stata18Linux64.tar.gz
tar -xzvf Stata18Linux64.tar.gz
./install      ## this will be followed by two prompts where you should press y for yes##
export PATH=/usr/local/stata18:$PATH
./stinit      ## this also will be followed by two prompts where you should press y for yes##
```


