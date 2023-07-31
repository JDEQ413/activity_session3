# Virtual Environments
Student: Julián Esquer


## Installation checklist
To validate the installation of tools, access the following file.

## Activity
In this activity, you will migrate and solve the package issues regarding a notebook that was created in a `Python 3.7.9` version.

Follow the instructions below to do the activity.
### Run the existing notebook
1. Clone the project `https://github.com/carloslme/itesm-mlops.git` on your local computer.
2. Create a virtual environment with `Python 3.7.9`
    * Create venv
        ```
        python3 -m venv venv37
        ```

    * Activate the virtual environment

        ```
        venv37/scripts/activate.bat
        ```

3. Install libraries
    Run the following command to install the other libraries.

    ```bash
    pip install -r module-2/session-3/activity/requirements-37.txt
    ```
    Verify the installation with this command:
    ```bash
    pip freeze
    ```
    Output:
    <details open>
    <summary>List of packages, click to collapse</summary>
  
        cycler==0.11.0
        joblib==1.0.1
        kiwisolver==1.4.4
        matplotlib==3.4.0
        numpy==1.21.6
        pandas==1.3.3
        Pillow==9.5.0
        pyparsing==3.1.0
        python-dateutil==2.8.2
        pytz==2023.3
        scikit-learn==0.20.0
        scipy==1.7.3
        seaborn==0.12.2
        six==1.16.0
        typing-extensions==4.7.1
        
    </details>
    

5. Open the `itesm-mlops/module-2/session-3/activity/end_to_end_machine_learning_project.ipynb` notebook and click on `Run All`. 
    > **IMPORTANT!**  
    Do not forget to select the Python 3.7.9 kernel you have already created.
    >
    > Install ipykernel as required by VSCode. Might take several minutes.

    If everything was ok, you should be able to see the last cell with this output:
    ```bash
    Predictions:	 [263527.   331884.02 221119.   ... 105722.   213199.   459125.66]
    ```
**Congrats, the notebook is running in a virtual environment with Python 3.7.9!**

### Migrating to Python 3.10.9
The goal of this activity is to migrate the libraries to a newer version of Python, for this exercise, `3.10.9`.

1. Create a virtual environment with `Python 3.10.9`.
2. Try to install the `requirements-37.txt`
3. You should get something like this:
    <details open>
    <summary>List of packages, click to collapse</summary>

    ```bash
    ...
    note: This error originates from a subprocess, and is likely not a problem with pip.
    error: subprocess-exited-with-error

    × pip subprocess to install build dependencies did not run successfully.
    │ exit code: 1
    ╰─> See above for output.

    note: This error originates from a subprocess, and is likely not a problem with pip.

    [notice] A new release of pip is available: 23.0.1 -> 23.2
    [notice] To update, run: pip install --upgrade pip
    ```
    </details>
    
    This means that the package installation was not successful.

    > **NOTE**  
    If you want to verify what packages were installed, run this code in your terminal, do not forget to activate your `python310` environment: `pip freeze`.

4. Find out how to upgrade the libraries in the `requirements-37.txt` file.
    > **HINT**  
    Look at the [Python Package Index (PyPI)](https://pypi.org/) for the compatible versions for every library.
    
    You have to create a new file called `requirements-310.txt` with the compatible versions. Do not forget to include the specific versions you used.

5. Change the notebook kernel to `python310` version, and `Run All` cells.  
    If everything was ok, you should see a similar output in the last cell as the kernel `python37`.


## Deliverable
The file is not going to be uploaded yet, so just keep it until the next session.
