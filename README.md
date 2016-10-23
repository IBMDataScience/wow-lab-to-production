#Hands on Lab - World of Watson, October 2016

Session Name: From Lab to Production: Scale Up Your Data Science with IBM Data Science Experience

Date: October 25, 2016, 4:00pm - 6:30pm

Place: Las Vegas, Mandalay Bay - Bayside F - 13

Description: Learn how IBM Data Science Experience can be used in early the stages of a data science project to create models that can then be scaled. By making it easy to change Spark instances with Jupyter notebooks or RStudio, Data Science Experience makes it easy to scale up when you are ready.

Speakers:   
 - Brandon MacKenzie, IBM
 - Greg Filla, IBM

# Contents 
- [Account Set-up](#set-up)
- [Create a project](#create-project)
- [Load data](#load-data)
- [Import Notebook from GitHub](#importing-notebooks)
- [Load Object Storage Data in a Notebook](#object-data)
- [Create decision tree in R](#decision-tree-r)
- ### Additional Activities 
 - [Create & Visualize Decision Tree with SPSS in Scala](#spss-tree) 
 
# Instructions:

#Step 1. Get on IBM Data Science Experience (DSX).
## <a name="set-up"></a>Create an account.

1.  Go to [http://datascience.ibm.com/](http://datascience.ibm.com/)

2.  Click the signup button on the top right

 > <img src="https://github.com/ibmdataworks/datafirst/raw/master/datascientist/media/DSX Sign On.png">

3. If you have a Bluemix account you can click continue with Bluemix credentials, otherwise click create your Bluemix account and enter your email.

4. You should get an email from "ibmacct" with your IBMid Confirmation code

 >  <img src="https://github.com/IBMDataScience/wow-lab-to-production/blob/master/images/confirmation-code.png?raw=true"/>

5. Then, on the next page fill in the corresponding fields and click CREATE ACCOUNT

 > <img src="https://github.com/ibmdataworks/datafirst/blob/master/appdeveloper/media/image3.png?raw=true" width="624" height="300" />

6. In the new page, write your email and click CONTINUE

 >  <img src="https://github.com/IBMDataScience/wow-lab-to-production/blob/master/images/enter-email.png?raw=true"/>

7. Write your recently generated password and click on SIGN IN

 >  <img src="https://github.com/IBMDataScience/wow-lab-to-production/blob/master/images/enter-password.png?raw=true"/>

8. It will take a minute to create your account. When ready, click on Get Started.

 > You are now in the Data Science Experience landing page. Your environment is automatically set up with one Apache Spark instance and 5 GB of object storage. From here you can explore any of the tutorials, videos, sample notebooks, totorials or articles in the community.

>  <img src="https://github.com/IBMDataScience/wow-lab-to-production/blob/master/images/landing.png?raw=true"/>

# <a name="create-project"></a>Step 2. Create a project

1. Click on the left hand side "hamburger" icon and then click on My Projects to see a list of your projects. You should only see a default project.

 >  <img src="https://github.com/IBMDataScience/wow-lab-to-production/blob/master/images/my-projects.png?raw=true"/>

2. Click on the create project icon on the top right of the project list.

 >  <img src="https://github.com/IBMDataScience/wow-lab-to-production/blob/master/images/
 new-project.png?raw=true" />

3. Type a name for your project. For instance, "DSX Lab". A Spark service and an object storage will be automatically selected as well as a container with a default name. A container is a directory on the object storage. Click on Create.

 > You are now in your new project where you can create notebooks and data assets as well as add collaborators.

 >  <img src="https://github.com/IBMDataScience/wow-lab-to-production/blob/master/images/create-project.png?raw=true" width="512" height="499" />


# <a name="load-data"></a>Step 3. Get the data into DSX


1. [Click here to download this repository](https://github.com/IBMDataScience/wow-lab-to-production/archive/master.zip) to your computer to access the data stored in the data directory.

2. Unzip this zip file on your computer so you have a directory with all the assets in the repository.  We will be using the data from the data directory.

2. Go to your recently created project on DSX and click on the add data assets + icon

 >  <img src="https://github.com/IBMDataScience/wow-lab-to-production/blob/master/images/add-data-asset.png"/>

3. Click on the Add file and select the transactions.csv file from your computer and click on open

 >  <img src="https://github.com/IBMDataScience/wow-lab-to-production/blob/master/images/add-file.png" width="450" height="275"/>

5. Once the file is loaded, click on Apply to add this file to your project.

 >  <img src="https://github.com/IBMDataScience/wow-lab-to-production/blob/master/images/apply-file.png" width="450" height="275"/>
 
 > Click Apply on the pop-up:
 
 >  <img src="https://github.com/IBMDataScience/wow-lab-to-production/blob/master/images/apply-changes.png" width="500" height="225"/>

  > You should see transactions.csv under the data assets list of your project. Your data is  now loaded in your object storage in the container associated to your project. If your project name is "DSX Lab", the default container name is DSXLab (unless you change to a different name on Step 2, part 3).
 >  <img src="https://github.com/IBMDataScience/wow-lab-to-production/blob/master/images/project-view.png"/>


# <a name="importing-notebooks"></a>Step 4. Importing Notebooks for Machine Learning Lab


1. From the your project page, on the "Overview" tab click "add notebook"
 >  <img src="https://github.com/IBMDataScience/wow-lab-to-production/blob/master/images/add-notebook.png" />
2. In the next screen named “Create Notebook”, switch to “From File” tab, name the notebook “ML Lab Installation”, and choose the notebook file on your disk from the archive: notebooks/ml-lab-installation.ipynb; alternatively you can switch to “From  URL” tab and use the following “Notebook URL”:
 > https://raw.githubusercontent.com/IBMDataScience/wow-lab-to-production/master/notebooks/ml-lab-installation.ipynb
 
 >  <img src="https://github.com/IBMDataScience/wow-lab-to-production/blob/master/images/notebook-from-url.png" width="512" height="499"/>
3. Click Create Notebook at the bottom of the page to add the notebook
4. Run all the cells in the notebook clicking on the Run All option under Cells
  >  <img src="https://github.com/IBMDataScience/wow-lab-to-production/blob/master/images/run-all.png" width="435" height="207"/>
5. Once the libraries have been installed, all the cells will have a number present on the left side of the notebook between square brackets.
   >  
   <img src="https://github.com/IBMDataScience/wow-lab-to-production/blob/master/images/complete-notebook.png"  width="435" height="207"/>
6. Click File -> Save or the Floppy disk icon to save the notebook 
7. Return back to the project overview page by clicking on "DSX Lab" or the name you gave your project
 >NOTE: the software packages installation may take a few minutes, but it
 >needs to be done only once per account
8.  Load the second notebook “Machine Learning with DSX - Lab” (from the file machine-learning-with-DSX-lab.ipynb, or from URL https://raw.githubusercontent.com/IBMDataScience/wow-lab-to-production/master/notebooks/machine-learning-with-DSX-lab.ipynb ) by following the same steps 1-3 as above


# <a name="object-data"></a>Step 5. Adding data from Object Storage in the Notebook

1.  From the loaded notebook “Machine Learning with DSX Lab” click on "Find and add data": 
<img src="https://github.com/IBMDataScience/wow-lab-to-production/blob/master/images/Selecting-Data-Sources.jpg"  width="230" height="189"/>   
2.  The expanded "Find and add data" would show transaction.csv under “Files” section

3.  Follow the instructions in the cell of the notebook shown below:

<img src="https://github.com/IBMDataScience/wow-lab-to-production/blob/master/images/adding-data-in-notebook.png"/> 
4.  After inserting the code, at then end you will see something that looks like this:
     
     ```R
     df.data.1 <-  read.csv(file = getObjectStorageFileWithCredentials_92c679820c6ebdd53("DSXLab", "transactions.csv"))
     head(df.data.1)    
     ```
   > Replace df.data.1 with df
   
     ```R
     df <-  read.csv(file = getObjectStorageFileWithCredentials_92c679820c6ebdd53("DSXLab", "transactions.csv"))
     head(df)    
     ```     
### Check point: 
 After the modifications, the section code should define a data frame variable df which is used in the notebook; the modifications should be done only for replacing  the variable in the last 2 lines of code shown above.

# <a name="decision-tree-r"></a>Step 6. Generate a decision tree model with visualizations in R
1.  Begin execution of every code section in the order in which the sections appear by clicking on the button ![](https://github.com/IBMDataScience/wow-lab-to-production/blob/master/images/Execute-section.png) or by using the menu Cell&gt; Run Cells. The lab covers the following actions:

     a.  Declaring the libraries used in the lab

     b.  Loading the data from the Object Storage into a data frame

     c.  Transforming the data for using with C5.0

     d.  Training the classification model (C5.0)

     e.  Transforming the classification model to visualize it in Brunel

     f.  Using a tree map for visualizing and exploring the decision tree in Brunel

     g.  Using a tree for exploring the decision tree in Brunel

     h.  Showing the native R visualization of the decision tree for comparison

2.  Stop the kernel (File &gt; Stop Kernel) and go back to the project overview page or DSX home page

---
# Additional Activity
## <a name="spss-tree"></a>Create and Visualize SPSS CHAID Decision Tree in Scala



