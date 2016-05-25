# google-search-api-to-pentaho

- **Install CPython Script Executer**
- **The Code**
- **For more info**

## Install CPython Script Executer

1. Go to http://www.pentaho.com/marketplace/ and download the plugin.
2. Close the pdi
3. Unzip all the files in pdi-path/plugins.
4. Install Python.
```
sudo apt-get install python
```
5. Install the following packages to Python.
```
sudo apt-get install python-numpy python-scipy python-matplotlib ipython ipython-notebook python-pandas python-sympy python-nose
```
```
apt-get -y install python-pip
```
```
sudo pip install -U scikit-learn
```
6. Open the pdi.
7. Create a new transformation and go to *Statistics* you will see the CPython step.

## How to execute?

To correct execute the process, go to the main.ktr and run the transformation. Don't forget to use yours Google API Keys on Python code.

## Why its three files and not just one?

If you try to execute all the steps in just one Transformation, the PDI will execute the Python Step and the Json Input step together. This will give you a error. Thats why we need to use jobs, to mantain the steps orders.

## How to show the result in biserver?

1. Create a new dashboard.
2. Create a new table component.
3. Go to Datasource Panel and select KETTLE Queries.
4. 