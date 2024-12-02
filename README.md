<div align="center">

# PIML4PDE: Physics-Informed Machine Learning for Solving Partial Differential Equations

</div>

The **PIML4PDE** framework is designed to solve Partial Differential Equations (PDEs) using Physics-Informed Machine Learning (PIML). This framework is intended for educational purposes, demonstrating steady-state and transient-state PDE problems. Example applications include water flow through homogeneous and heterogeneous porous media, contaminant tranport and heat conduction.  



### **Applications of PIML4PDE**
The PIML codes available here can also be directly applied to the following fields or adapted with modifications:  

#### **Multiphase Flow**
- Models the movement of multiple interacting fluid phases (e.g., water, oil, gas) in porous media.
- Crucial for applications in petroleum engineering, CO₂ sequestration, and groundwater management.

#### **Contaminant Transport**
- Simulates the transport and fate of contaminants in water and soil systems.
- Essential for environmental engineering, pollution control, and risk assessment.

#### **Heat Conduction**
- Models the steady-state temperature distribution in a medium with uniform thermal conductivity and no internal heat sources.
- Useful in thermal engineering and material science applications.

#### **Electrostatics**
- Describes the electric potential in regions without charges.
- Forms the foundation for studying electric fields and potentials, often applied in physics and electronics.

#### **Elasticity Problems**
- Simulates stress distributions in materials under equilibrium conditions.
- Commonly used in mechanical and structural engineering.

#### **Geophysics**
- Solves electrival resistivity, gravitational or magnetic potential field problems.
- Aids in subsurface exploration and resource management.

#### **Image Processing**
- Provides a mathematical basis for techniques such as, edge detection, image smoothing, and noise reduction.
- Useful in computer vision and digital image analysis.

#### **Other Fields**
- Appears in diverse applications such as:
  - Steady-state diffusion processes.
  - Financial modeling for steady-state behaviors.


The **PIML4PDE** framework provides a versatile platform for solving PDEs across various disciplines, demonstrating the broad applicability of physics-informed machine learning.


---

## Installation

This guide provides a step-by-step approach for cloning the **PIML4PDE** repository, creating a Conda environment named **ml4pde**, and installing the required dependencies on both **Windows** and **macOS** for seamless use of the **PIML4PDE** framework.


### A. Cloning the PIML4PDE Repository
#### 1. Git Installation: Prerequisites for Windows and Mac: If Git is not installed, do the following steps: 

##### For Windows:
1. Download Git for Windows from [Git's official website](https://git-scm.com/).
2. Run the installer and follow the setup instructions:
   - During installation, choose the default options unless you have specific preferences.

##### For Mac:
1. Open the Terminal and check if Git is already installed:
```
git --version
```

2. If not installed, you'll be prompted to install it, or download it from [Git's official website](https://git-scm.com/).


##### For Linux:
1. Open the Terminal and check if Git is already installed:
```
git --version
```

If Git is not installed, install it using:

```
sudo apt update
sudo apt install git
```

2. If Git is not installed, you'll be prompted to install it. Follow the on-screen instructions to complete the installation.
Alternatively, download Git from Git's official website and install it manually.



#### 2. Cloning the Repository

To clone the **PIML4PDE** repository, follow these steps:

1. Open a Terminal (Mac) or Command Git-Bash/Prompt/PowerShell (Windows).

2. Navigate to the directory where you want to clone the repository:

```
cd /path/to/your/desired/folder
```

3. Run the command on Terminal: 

```
git clone https://github.com/EMSL-Computing/PIML4PDE.git
```

4. Navigate into the cloned repository:

```
cd PIML4PDE
```



### B. Setting Up a Python Environment for **PIML4PDE** framework Using Conda

#### 1. Install Conda
If Conda is not installed, download and install either [Anaconda](https://www.anaconda.com/) or [Miniconda](https://docs.conda.io/en/latest/miniconda.html), depending on your preference.

##### For Windows:
- Download the Anaconda installer for Windows from [Anaconda's official website](https://www.anaconda.com/).
- Run the downloaded `.exe` file to begin the installation.
- Follow the setup instructions:
   - Choose the default options unless you have specific preferences.
   - Optionally, check "Add Anaconda to my PATH environment variable" during installation.
- After installation, open **Anaconda Prompt** and verify the installation:

```
conda --version
```

##### For Mac:
- Download the Anaconda installer for macOS from [Anaconda's official website](https://www.anaconda.com/).
- Open the downloaded `.pkg` file and follow the instructions to install Anaconda.
- Alternatively, for the command-line installer, open Terminal and run:

```
   bash ~/Downloads/Anaconda3-latest-MacOSX-x86_64.sh
```

- After installation, restart the terminal or run:

```
   source ~/.bash_profile
```

- Verify the installation:

```
   conda --version
```

##### For Linux:
- Open the Terminal and download the Anaconda installer:

```
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
```

- Run the installer:

```
bash Miniconda3-latest-Linux-x86_64.sh
```

- Follow the prompts to complete the installation:
   - Accept the license terms and choose the installation location (default is recommended).

- Restart the terminal or activate Conda:

```
source ~/.bashrc
```

- Verify the installation:

```
conda --version
```






#### 2. Create and activate the Conda Environment
Open an Anaconda Promt (Windows) or Terminal (Mac or Linux). Run the following command to create a new environment named **ml4pde** with Python 3.9:

```
conda create -n ml4pde python=3.9 -y
```


Activate the newly created environment:

```
conda activate ml4pde
```

#### 3. Install the Required Packages
To install all dependencies from the *requirements.txt* file:


```
pip install -r requirements.txt
```


#### 4. Verify the Installation
Type the on Anaconda Prompt (Windows) or Terminal (Mac or Linux) to lunch Jupyter Notebook: 
```
jupyter notebook
```

Navigate to the example directory in the browser interface. Open and run the testing script *testing_packages_for_pinn.ipynb*. 

You should see the following printout text after running the testing script and successful installation of all the packages:  
```
Testing imports and basic functionality...

NumPy: OK
JAX: OK
Optax: OK
Matplotlib: OK
Scikit-learn: OK

Testing complete!
```



In case of any errors, follow these steps:

```
pip uninstall <package-name>

pip install <package-name>

```

---


## Authors
* Lal Mamud (lead developer), Pacific Northwest National Laboratory, Richland, WA, USA (<lal.mamud@pnnl.gov>)
* Pratanu Roy, Lawrence Livermore National Laboratory, Livermore, CA, USA (<roy23@llnl.gov>)
* Maruti K. Mudunuru, Pacific Northwest National Laboratory, Richland, WA, USA (<maruti@pnnl.gov>)
* Md Golam Kibria, Morehead State University, Morehead, KY, USA (<m1235960@moreheadstate.edu>)
* Piyoosh Jaysaval, Pacific Northwest National Laboratory, Richland, WA, USA (<piyoosh.jaysaval@pnnl.gov>)
* Md Samrat Alam, Geological Survey of Canada, Quebec City, Canada (<samrat.alam@nrcan-rncan.gc.ca>)
* Habiba Akter, University of London, London, UK (<eex373@qmul.ac.uk>)
* Satish Karra, Environmental Molecular Sciences Laboratory, Richland, WA, USA (<karra@pnnl.gov>)




## Development, contribution, and questions
Contact Md Lal Mamud (lal.mamud@pnnl.gov) and/or Maruti Mudunuru (maruti@pnnl.gov): If you have questions or need help getting started.



## Acknowledgements
This work was performed on a project award (Award DOIs: 10.46936/lser.proj.2023.60720/60008914, 10.46936/lser.proj.2023.60723/60008915, 10.46936/intm.proj.2023.60904/60008965) from the Environmental Molecular Sciences Laboratory (EMSL), a DOE Office of Science User Facility spon-sored by the Biological and Environmental Research program under contract no. DE-AC05-76RL01830.

PNNL-SA-206348

## Disclaimer
This research work was prepared as an account of work sponsored by an agency of the United States Government. Neither the United States Government nor any agency thereof, nor any of their employees, makes any warranty, express or implied, or assumes any legal liability or responsibility for the accuracy, completeness, or usefulness of any information, apparatus, product, or process disclosed, or represents that its use would not infringe privately owned rights. Reference herein to any specific commercial product, process, or service by trade name, trademark, manufacturer, or otherwise does not necessarily constitute or imply its endorsement, recommendation, or favoring by the United States Government or any agency thereof. The views and opinions of authors expressed herein do not necessarily state or reflect those of the United States Government or any agency thereof.
