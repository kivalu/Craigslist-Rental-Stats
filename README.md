# Craigslist-Rental-Stats

## Step 0: Install Ubuntu for Windows
Open powershell as an admin and run the following command:
```bash
[Net.ServicePointManager]::SecurityProtocol = 
  [Net.SecurityProtocolType]::Tls12 -bor `
  [Net.SecurityProtocolType]::Tls11 -bor `
  [Net.SecurityProtocolType]::Tls
```
Then, run:
```bash
Invoke-WebRequest -Uri https://aka.ms/wsl-ubuntu-1604 -OutFile Ubuntu.appx -UseBasicParsing
```
This will take a minute to download. Once it does, run:
```bash
Add-AppxPackage .\Ubuntu.appx
```

You will then need to enable WSL positions as described [here] and restart your computer.

[here]: https://ubuntu.com/tutorials/ubuntu-on-windows#3-enable-wsl

When the computer is restarted, open ubuntu and follow prompts to allow it to fully install. 

## Step 1: Install Miniconda
Open an ubuntu shell and enter the following command:
```bash
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
bash Miniconda3-latest-Linux-x86_64.sh
```
Say yes to all the prompts that you get. Once it is finished installing, close ubuntu, then reopen.

Now, run:
```bash
conda -V
```

If you see `conda x.x.x` as result (where x is a number), you know you successfully installed it. 

## Step 2: Clone Repository

In the ubuntu shell, type:
```bash
git clone https://github.com/kivalu/Craigslist-Rental-Stats.git
```

Then type:
```bash
cd Craigslist-Rental-Stats
```

## Step 3: Create Your Environment
Type the following command into your ubuntu shell:
```bash
conda env create -f environment.yml
```
That may take a minute. After installing, type in the following command:
```bash
conda activate rentstats
```

You will now be working in the `rentstats` enivironment. Anytime you want to run the Craigslist Rental Stat program, you will need to first run the above command. 

## Step 4: Open Jupyter Notebook

To interact with the craigslist stat noteboo, you will need to open a jupyter notebook by entering the following command (in an ubuntu shell while in the `rentstats` environment:
```bash
jupyter notebook
```
A web browswer window should open with access to the file. If after ~20 seconds, a browswer window does not open, a url should be displayed in the ubuntu shell. Paste it into your browswer and you should be able to access your notebook.
