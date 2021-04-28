# Craigslist-Rental-Stats

## Step 1: Install Miniconda
Open an ubuntu shell and enter the following command:
```bash
  wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
  bash Miniconda3-latest-Linux-x86_64.sh
```

Run 
```bash
conda -V
```

If you see `conda x.x.x` as result, you know you successfully installed it. 

## Step 2: Clone Repository

In the ubuntu shell, type:
```bash
git clone https://github.com/kivalu/Craiglist-Rental-Stats.git
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
