# Ecobotix---Locating-Stresses-Of-Plants-From-A-UAV
For the 4th semester master thesis of the Robotics MSc in Engineering at University of Southern Denmark (SDU) And in collaboration with Ecootix an algorithm was developed to help detect stress in plants more effectively.

## Setting up environment
Assuming Linux. To setup the environment we first need to install either [Anaconda](https://www.anaconda.com/) or [Conda](https://docs.conda.io/en/latest/).

We will then create a new environment with `conda env create -f environment.yml`.


## Usage
If you chose not to add the Conda hook to your .bashrc, you can add it with `eval "$(/home/$USER/miniconda3/bin/conda shell.bash hook)"`. Now activate the Conda environment with `conda activate msth` and start the Jupyter notebook with `jupyter notebook ./'` assuming that your terminal is currently inside the this git repository.

You can now use the 'Orthomosaic_to_dataset' script to turn the included 6-channel image into smaller images using the the included mask. A RGB image will also be plit in the same way as to give better insight into the workings of the output.

After this, the 'Build_dataset' script in the 'CNN' directory can be used to create training, valiation, and test datasets for the CNN. 

At last, one can run the 'CNN' script to actually train the AI.