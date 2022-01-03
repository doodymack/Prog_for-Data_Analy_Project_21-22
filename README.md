# Programming for  Data Analytics 2021-2022
## Winter Semester Assessment- Paul Mc Grath
***
<br>

This repository contains a jupyter notebook and other relevant files used to demonstrate my work on:
-  Simulation of Data using Numpy Random in PANDAS
<br>

 for my module: 
 Programming for Data Analytics


### Project Requirements:

Choose a real-world phenomenon that can be measured and for which you could collect at least one-hundred data points across at least four different variables. <br>
Investigate the types of variables involved, their likely distributions, and their relationships with each other.<br>
Synthesise/simulate a data set as closely matching their properties as possible. <br>
Detail your research and implement the simulation in a Jupyter notebook – the data set itself can simply be displayed in an output cell within the notebook <br>

---
---

# Install

Steps to install
---
<br>

The work is based on **Python 3** code and executed via a **Jupyter Notebook** <br>
Jupyter allows the creation of a Notebook that contains summary text and image files while also allowing the running of of Python code. <br><br>
The key files to run in the repository are:  **Pyplot.ipynb** and **CAO_points.ipynb**. <br>
To execute the work you should have **Python 3**  and  **Jupyter** notebooks installed. <br><br>


### How to install the necessary packages:
While Jupyter runs code in many programming languages, Python is a requirement (Python 3.3 or greater, or Python 2.7) for installing the Jupyter Notebook. It is recommended to use the Anaconda distribution to install **Python** and **Jupyter**. <br>
Anaconda conveniently installs Python, the Jupyter Notebook, and other commonly used packages for scientific computing and data science.

***Note the packages and dependencies are in my 'requirements.txt' file*** <br> <br>

### Installation instructions:

- [Download Anaconda](https://www.anaconda.com/products/individual) <br>
 Its recommended to download Anaconda’s latest Python 3 version (currently Python 3.5).
- Install the version of Anaconda which you downloaded, following the instructions on the download page.
This should also have installed Jupyter Notebook. <br>
---
<br>

## Running the notebook in Github:

Note: 
- The notebook is created to automatically run all code if executed within the GitHub 
- should the code not run, close the file and re-open <br><br>

---

## Running the notebook on your local PC environment:

After installing **Python** and **Jupyter** packages via **Anaconda**:


How to run the ipynb files:

- The key file is ipynb file.
- Once this is opened Jupyter starts off in web browser but is running on your machine
- Once opened click on the 'kernel' dropdown button on the taskbar at the top of the screen
- click on 'restart kernel and run all cells'
- Thus recreates the text and re-runs the code in each program cells from the beginning
- read the notebook from top to bottom
- read the text above each program cell for background as to the purpose of the python code 
- within each code are additional commments on the specific code  as non-executable commented out brief explanation  i.e. ***#asterisk followed by green text***

#### In summary once the required code is downloaded:
1. Download the required packages
2. open the ipynb file: 
3. restart the notebook
4. read the notebook from top to bottom

Troubleshooting:
- The code has been checked to ensure it runs end to end
- However if you get a warning then restart the kernel again as per above <br>

---
<br>

## Summary


 Open the simulation notebook in this repository in Jupyter and use the below notes as additional guidance <br> 


---

#### Plan:


My plan was to identify an area of interest for simulation. <br> Thereafter source a suitable dataset. <br>  Create a new dataset of simulated data from the original dataset using the pandas numpy.random functionality. <br> Analyse the simulated data for correlations/relationship.

Outline plan for the project:

1. Identify areas of interest
2. Source suitable data
3. Create a dataframe
4. Clean-up the dataset
5. Concatenate the relevant datasets (as required)
6. Check for correlations
7. Identify best data distribution
8. Generate simulated data
9. Merge simulated data into one dataframe
10. Plot data
11. Summarise the findings

A thorough assessment of potential databases online was completed. Based on area of interest, the focus was on global healthcare and where there could be interesting correlations and data simulation could be attempted. One area of interest is the impact of outcomes (life expectancy) based on national spend on healthcare.Two suitable databases were identified:

- Global Health Outcomes
- World Bank Databases
These two databases comntained suitable attributes to trend and simulate. <br> <br>

---
<br>

The Notebook `Simulation_Notebook.ipynb` describes the method to source suitable datasets, scrape the relevant data from the original datasets, create a dataframe containing the relevant data. <br>

As the original dataset did not contain GDP per country, this was located in another online database. <br>

As both databases did not fully match i.e. Global Health Outcomes contained some data for 'regions' which were not in the World Bank Database, a manual clean-up of each dataset to ensure each had the exact same entries (per country) before conmcatenating. <br>
Once the combined dataset was ready numpy random was used to determine what statistical function deascribes the data best <br>  
It was found that for 2 of 4 attributes these followed a normal distribution.  Hence the decision was made to simulate (create new data) from statisitical parameters (mu and sigma) of the original dataset. <br>
For the remaining two (Physicians per 10K population and GDP), these did not follow a normal distribution. <br>
Attempts to use alternative distributions in the numpy.random package did not adequately match the original data distributions. <br>
Therefore the random.choice function was used to randonly extract data from the orioginal datasets <br>
<br>

---
<br>

### Plotting the original datasets and looking for correlations
When the original dataset was plotted using histogram and correlations plots (seaborn Pairgrid) correlations were apparent between all attributes. <br>
Review the comments under each pair plot in the 'Simulation_Notebook' for more information.

<br>

---
<br>

### Plotting the simulated datasets and looking for correlations
When the simulated datasets were plotted using histogram and correlations plots (seaborn Pairgrid) weaker correlations were apparent between all attributes. <br>
Review the comments under each pair plot in the 'Simulation_Notebook' for more information. <br>

---

<br>


### Conclusion:

The project allowed me to improve my working knowledge of the python PANDAS and Matplotlib  functionality to extract and concatenate data from different online data <br>  The project allowed me put forward ways to scrape and engineer online data into a dataframe. <br>  Therafter the functionality of numpy.random can be used to create a new dastaset using the original dataset functionality for individual attributes.<br> 
However simulation of data using numpy.random will create new data to whatver parameters are inputted <br>
For instance creating simulated data from 200 data points of measured mean and standard deviation will create a new dataset with randomized data with the same mean and standard deviation. <br>
However based on my assessment this is insufficient to adequately preserve the correlations seen with the original data. <br>

---
<br>

### What I learned
<br>

I learned that there are many ways to capture data and transform it to trendable data using the functionality of PANDAS. <br> 
However the power of PANDAS does not avoid the need from time to time for the data analyst to manually inspect the raw data and clean it ready to be uploaded as a csv file/pandas dataframe. <br> 

I learned simulations using numpy.random data may be useful in creating randomized data that can be used for further work/model building. <br>
 
 However to ensure simulated data retains the same interdependencies to the original data i.e. retains correlations between the attributes as original data requires:
1. a strong and predictable correlation between each attribute i.e. y =mx +C
2. This function needs to be incorporated in the transformation of the data from parent to simulated dataset <br>

--- 

### Future work

<br>

To ensure simulated data reflects the same correlations to the original data requires:
a strong and predictable correlation between each attribute i.e. y =mx +C
This function needs to be incorporated in the transformation of the data from parent to simulated dataset <br>

---

## Contact: 

[doodymack@gmail.com](mailto:doodymack@gmail.com)
