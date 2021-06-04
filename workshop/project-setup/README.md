# Workshop Setup

Before we get started with the workshop, you will need to download some assets and setup your environment. 

This section is broken up into the following steps:

1. [Download Assets](#1-download-assets)
1. [Create IBM Cloud Account and IBM Cloud Pak for Data services](#2-create-ibm-cloud-account-and-service)
1. [Create a Project](#3-create-a-project)
1. [Upload the data](#4-upload-the-data)
1. [Associate a Watson Machine Learning Service instance to the project](#5-associate-a-watson-machine-learning-service-instance-to-the-project)
1. [Conclusion](#6-conclusion)

>**Note:** You can click on any image in the instructions below to zoom in and see more details. When you do that just click on your browser's back button to return to the previous page.

## 1. Download Assets

Various parts of this workshop will require the attendee to upload files or run scripts. These artifacts have been collected in the following two zip files which you can download using the links below. For each line below, click on the `[Download]` link to get the file. If the link isn't working for you, try clicking the `[Mirror]` to get it from a backup server. You'll need these files in the next sections.

* Jumpstart your Journey with Cloud Pak for Data Project - [[Download]](http://ibm.biz/DDC2021-jumpstart-your-journey) | [[Mirror]](https://github.com/IBM/ddc-2021-jumpstart-your-journey/raw/main/projects/jumpstart-your-journey.zip)

## 2. Create IBM Cloud account and service

We need to provision our Cloud Pak for Data as a Service instance. Cloud Pak for Data provides you with an integrated set of capabilities for collecting and organizing your data into a trusted, unified view, and then creating and scaling AI models across your business.

* Launch a web browser and navigate to IBM Cloud Pak for Data using the region closest to your location from the list below:

    * [US, Dallas](https://dataplatform.cloud.ibm.com/registration/stepone?context=cpdaas&apps=all&regions=us-south&preselect_region=true)
    * [EU, Frankfurt](https://eu-de.dataplatform.cloud.ibm.com/registration/stepone?context=cpdaas&apps=all&regions=eu-de&preselect_region=true)
    * [Japan, Tokyo](https://jp-tok.dataplatform.cloud.ibm.com/registration/stepone?context=cpdaas&apps=all&regions=jp-tok&preselect_region=true)

* You can then log in using your IBMid if you have one or create a new IBMid.

  * If you do not have an IBMid, enter your email address and accept the terms checkbox in the `Create a new IBM Cloud Account` section. Then click the `Next` button to complete the process of creating a new account.
  * If you are a returning user, click on the `Log in with your IBMid` link.
    > **Note:** If you are a returning user and you have watson services in a different region than the pre-selected one, you will see an error message telling you to select that region instead. See the [FAQ](#faq) section for help.

[![CPDaaS login](../assets/images/setup/new-signup-page.png)](../assets/images/setup/new-signup-page.png)

* The services required for IBM Cloud Pak for Data will be automatically provisioned for you. Once you see a message that says that the apps are ready to use, click on `Go to IBM Cloud Pak for Data`.

[![CPDaaS ready](../assets/images/setup/cpdaas-ready.png)](../assets/images/setup/cpdaas-ready.png)

## 3. Create a project

### Import the Project

In Cloud Pak for Data, we use the concept of a project to collect / organize the resources used to achieve a particular goal (resources to build a solution to a problem). Your project resources can include data, collaborators, and analytic assets like notebooks and models, etc.

* Once you are on [Cloud Pak for Data as a Service](https://dataplatform.cloud.ibm.com). Click on the (☰) navigation menu on the top left, expand *Projects* and click on the *View all projects* link.

[![(☰) Menu -> Projects](../assets/images/setup/menu-projects.png)](../assets/images/setup/menu-projects.png)

* Click on the `New project` button on the top. *Note: If you already have existing projects, your screen will look different from the screenshot below. In that case, click on the `New project +` button on the top right.*

[![Start a new project](../assets/images/setup/cpd-new-project.png)](../assets/images/setup/cpd-new-project.png)

* Click on `Create a project from a sample or file`.

[![Create project from a file](../assets/images/setup/cpd-create-project-from-file.png)](../assets/images/setup/cpd-create-project-from-file.png)

* Click on the **browse** link and in the file browser popup, navigate to where you downloaded the files for this lab. Then select the `DDC2021-jumpstart-your-journey.zip`.

[![Browse for project files](../assets/images/setup/browse-project-zip.png)](../assets/images/setup/browse-project-zip.png)

* Give the project a name and optional description. You also need to provide an object storage instance for this project. If you have not previously created a Cloud Object Storage instance in your IBM Cloud account, you can create one now by clicking `Add`. *Note: If you do have an existing storage service, select it from the drop down list and click the `Create` button.*

[![Project name](../assets/images/setup/cpd-project-name.png)](../assets/images/setup/cpd-project-name.png)

* A new tab opens up, where you can create the Cloud Object Service. By default, a `Lite` (Free) plan will be selected. Scroll down and update the name of your Cloud Object Storage service if you wish, and click `Create`.

[![Create COS instance](../assets/images/setup/create-cos-instance.png)](../assets/images/setup/create-cos-instance.png)

* The browser tab will automatically close when the Cloud Object Storage instance has been created. Back on IBM Cloud Pak for Data as a Service, click `Refresh`.

[![Refresh COS](../assets/images/setup/refresh-cos.png)](../assets/images/setup/refresh-cos.png)

* The newly created Cloud Object Storage instance will now be displayed under "Storage". Click `Create` to finish creating the project.

[![Create project](../assets/images/setup/create-project.png)](../assets/images/setup/create-project.png)

* Once the project is succesfully created you will be brought to the project overview page (*Note:You may be presented with a project tour pop up window, go ahead and close it*)

[![Import project success](../assets/images/setup/project-create-success.png)](../assets/images/setup/project-create-success.png)

## 4. Upload the data

We'll use a data set from [Kaggle](https://www.kaggle.com/) for this workshop. You'll need to download it to your local machine, then upload to your project running in Cloud Pak for Data as a Service.

* Download the data to your laptop or PC by [clicking this link](https://www.kaggle.com/noordeen/insurance-premium-prediction/download).

* In your project, click on `Add to project +` and then choose the tile for `Data`. Alternately, under *Data assets* click `New data asset +`.

[![Upload data](../assets/images/setup/cpd-upload-data.png)](../assets/images/setup/cpd-upload-data.png)

* Wait on this page until the upload completes. You should see the file `insurance.csv` under your *Data assets*.

[![Data upload completed](../assets/images/setup/cpd-data-upload-completed.png)](../assets/images/setup/cpd-data-upload-completed.png)

## 5. Associate a Watson Machine Learning Service instance to the project

You will need to associate a Watson Machine Learning service instance to your project in order to run Machine Learning experiments.

* Go to the *Settings* tab of your project and look for the *Associated services* section. Click on `Add service` and in the menu that opens up, click on `Watson`.

[![Add Watson service](../assets/images/setup/add-watson-service.png)](../assets/images/setup/add-watson-service.png)

* Click the checkbox next to the Watson Machine Learning service instance that was created for you when you signed up for Cloud Pak for Data as a Service or the one you created in section 2. Click `Associate service`.

  > **Note:** If you have multiple WatsonMachineLearning services, make sure you select the one that is in the same regions as is your Cloud Pak for Data as a service.

[![Choose WML instance](../assets/images/setup/choose-wml-instance.png)](../assets/images/setup/choose-wml-instance.png)

* You willsee a notification that the WatsonMachineLearning service was successfully associated with your project. Click on the `X` in the right top corner to close the pop up modal and go back to your project.

[![WML Service added successfully](../assets/images/setup/wml-service-added-successfully.png)](../assets/images/setup/wml-service-added-successfully.png)

You are now ready to move on to the next module of this course.

## FAQ
 
**Q1: I don't have all the services needed.**

A: In some rare cases, the services may not automatically provision for you. You can do that manually by following these instructions:

* Go the (☰) navigation menu on the top left corner of the Cloud Pak for Data UI. Expand *Services* and then click on `Service instances`.

* If you do not have an instance of *Watson Machine Learning*, or any service that you need, click on the `Add service +` button.

* Search or scroll until you find the tile for *Machine Learning*,or whichever service you need, and click on it.

* Choose the same region as you chose for your Cloud Pak for Data as a Service platform, select the *Free* tier unless your organization has already used their 1 free tier, change the name and add tags if you like. The *Default* resource group should be correct, and then click `Create`.

**Q2: I get the `That email address is already registered to an IBM Cloud account.` messsage.**

A: You must already have an IBMid account. Follow the login link provided in the error message to login to your existing account. 

**Q3: I get the `Your Watson Studio, Watson Knowledge Catalog, and Watson Machine Learning Lite services must be created in the same service region.` error.**

A: This means you have previously created some Watson services in a different region. To resolve this, go to the [CP4DaaS Login](https://dataplatform.cloud.ibm.com/registration/stepone?context=cpdaas&apps=all) page, select the region you had previously used and then login using the login link at the bottom right. Alternatively, you can create a new account and proceed as a new user to follow along.

## 6. Conclusion

At this point we are done with this section. We have completed creating an IBM Cloud account, a Cloud Pak for Data as a Service instance, and the project that we will use in the rest of this workshop.
