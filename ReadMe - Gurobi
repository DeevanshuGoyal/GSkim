Running Gurobi using conda environments

Here is a short and useful guide on how to install Gurobi and run it anywhere in your machine, irrespective of the location of the license installation.

1. Install [Miniconda](https://docs.conda.io/en/latest/miniconda.html) (you can skip this if you already have either of Miniconda or Anaconda installed).
2. Create a conda environment by running the following command ;
```conda create --name myenv```
Replace myenv with the name of your environment.
4. Now, enter the created environment by running the following command ;
```conda activate myenv```
Alternatively, you can enter any of your older environments as well.
4. Once the conda environment has been activated, you can move to the directory wherein you wish to install the Gurobi executables
5. Once you are in the desired directory, your first steps would be to visit the [download page](https://www.gurobi.com/downloads/gurobi-software/), find your platform, and choose the corresponding file to download. 
6. Please note that you might have to create an account on Gurobi for access to the desired software. This would also be required to create and use licenses later on.
7. To download the .tar file for the Gurobi executable from the online database into the destination directory where you are currently, use this command ; `curl -O https://packages.gurobi.com/9.5/gurobi9.5.2_linux64.tar.gz` (We are assuming Linux as your platform for this example)
8. Unpack the downloaded file into the destination directory by running; 
`tar xvfz gurobi9.1.2_linux64.tar.gz` 
This command will create a sub-directory `/opt/gurobi912/linux64` that contains the complete Gurobi distribution (here `/opt` refers to your destination directory). Your `<installdir>` will be `/opt/gurobi912/linux64` then.
9. After this, users of the bash shell should add the following lines to their .bashrc files:
`export GUROBI_HOME=“/opt/gurobi912/linux64”`
`export PATH=“${PATH}:${GUROBI_HOME}/bin”`
`export LD_LIBRARY_PATH=“${LD_LIBRARY_PATH}:${GUROBI_HOME}/lib”`
Where; GUROBI_HOME should point to your`<installdir>`.
PATH should be extended to include `<installdir>/bin`.
LD_LIBRARY_PATH should be extended to include `<installdir>/lib`.
10. You'll need to close your current terminal window and open a new one after you have made these changes in order to pick up the new settings.
11. Your next step is to install the Gurobi license on your machine. You do this by obtaining a license key file by creating a license under your registered profile.
12. There are various types of licenses available. Based on your requirement, identify the relevant type [here](https://www.gurobi.com/documentation/9.1/quickstart_linux/retrieving_and_setting_up_.html#section:RetrieveLicense) and proceed to generate the required license.
13. We will discuss the next steps for the Academic license. Before proceeding for the academic license, please ensure that you are connected to your university network. If you are validating a home machine and the university provides a VPN, please connect to it before retrieving your license. If the reported host name is a valid university address, please visit the [support site](https://support.gurobi.com/hc/en-us) for assistance.
14. Once you have generated the license, you can find the exact grbgetkey command to run for a specific license at the bottom of the License Details page (e.g., `grbgetkey 253e22f3-...`). Copy and paste the entire grbgetkey command from our website and paste it into a shell window. Make sure that your machine has an active Internet connection.
15. Once you run the command, grbgetkey will ask for the name of the directory in which to store your license key file (gurobi.lic). We recommend accepting the default location (either your home directory or `/opt/gurobi`) by hitting Enter.
16. Now, you are ready to test your license in the terminal window. To do this, type `gurobi_cl`. The shell should produce the following output;
```
Set parameter LogFile to value "gurobi.log"
Restricted license - for non-production use only - expires 2023-10-25

Usage: gurobi_cl [--command]* [param=value]* filename
Type 'gurobi_cl --help' for more information.
```
17. Congratulations, your license is functioning correctly! Now, you can use the solver in any directory by simply activating the environment (`myenv` in this case) in the desired directory. To check this, go to any other directort, activate the relevant conda environment and repeat step 16.
