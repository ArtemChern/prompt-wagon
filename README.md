# Prompt Wagon

## Summary

This app is designed for organizations seeking to seamlessly integrate AI technologies, with features catering to beginners and administrators. 

![Screenshot](assets/PromptWagonScreenshot.png)

## Applies to

![Power Apps](https://img.shields.io/badge/Power%20Apps-Yes-green "Yes")
![Dataverse](https://img.shields.io/badge/Dataverse-Yes-green "Yes")
![Custom Connectors](https://img.shields.io/badge/Custom%20Connectors-Yes-green "Yes")
![Power Fx](https://img.shields.io/badge/Power%20Fx-Yes-green "Yes")

## Compatibility

![Premium License](https://img.shields.io/badge/Premium%20License-Required-green.svg "Premium license required")
![Azure OpenAI](https://img.shields.io/badge/Azure%20OpenAI-Required-green.svg "Use Azure OpenAI GPT-4 model")

## Contributors

* [Artem Chernevskiy](https://github.com/ArtemChern)

## Version history

Version|Date|Comments
-------|----|--------
1.0|September 24, 2023|Initial release

## Prerequisites

* Azure OpenAI resource
* GPT-4 model deployed in the Azure OpenAI resource
* Save the following information from your GPT-4 model deployment (this will be needed during the solution import process):
1) AzureOpenAI Host
2) AzureOpenAI Key
3) AzureOpenAI URL
![Prerequisites](assets/prerequisites.png)

## Minimal path to awesome

### Using the solution zip

* [Download](./solution/solution.zip) the `.zip` from the `solution` folder.

* Navigate to [https://make.powerapps.com](https://make.powerapps.com).

* Open **Solutions** from the left-hand panel, select **Import solution**. Select **Brows** to choose downloaded Zip file, and select **Next**.
![1](assets/1.png)

* Select **Next** on the **Details** screen.
![2](assets/2.png)

* On the **Environment Variables** screen enter values for all environment variables. Once you are ready, seelct **Import**
![3](assets/3.png)

* Wait till the end of the import process.
![4](assets/4.png)

* Open the imported solution, Select **Apps**, click on three dots next to the app name, select **Play**.
![11](assets/11.png)

* Select **Sign in**.
![12](assets/12.png)

* Enter Azure OpenAI API key, and select **Create**.
![13](assets/13.png)

* Select **Allow**.
![14](assets/14.png)

* Navigate to **Connections**, click three dots next to connection name, select **Share**.
![15](assets/15.png)

* Select **Add everyone in my org** (or select your colleagues with whom you want to share the app).
![16](assets/16.png)

* Select **Save**.
![17](assets/17.png)

* Go back to the solution, click three dots next to the app name, select **Share**.
![18](assets/18.png)

* Add security roles **Prompt Wagon User** and **Basic User**, select **Share**.
![19](assets/19.png)

On the initial launch, users will encounter a pop-up prompting them to grant permission for connections to Azure OpenAI. Once authorized, this pop-up will not appear in subsequent launches.
![20](assets/20.png)


### Import sample data

This step is optional. You have the option to populate the Dataverse tables with your content, such as interface text, images, prompts, and translations into two other languages. If you'd prefer to begin with sample data, follow the steps outlined below.

* [Download](./sample-data/PromptWagonSampleData.zip) the `.zip` from the `sample-data` folder.

* Make sure that you have version 1.19.3 (or newer) of [Power Platform CLI](https://learn.microsoft.com/en-us/power-platform/developer/cli/introduction).
To install the latest version:
  ```bash
  pac install latest
  ```

* Now get help on the tools.

  ```bash
  pac tool help
  ```

* See what tools are installed.

  ```bash
  pac tool list
  ```

* Download and launch the Configuration Migration Tool

  ```bash
  pac tool CMT
  ```

![5](assets/5.png)

* Select **Import data* and **Continue**
![6](assets/6.png)

* Select **Office 365**, check **Display list of available organizations** and select **Login**
![7](assets/7.png)

* Select your target environment and select **Login**
![8](assets/8.png)

* In the fiels **Zip File** select **PromptWagonSampleData.zip** downloaded earlier, and select **Import Data**.
![9](assets/9.png)

* Once the import process will be completed, select **Exit**.
![10](assets/10.png)


## Features

* The app's responsive design ensures compatibility with both PC and mobile devices.
* With Sample Data, users receive 103 preset prompts spread across three categories: Business, Data, and Education. This facilitates interaction with GPT-4, even for those unfamiliar with prompt engineering.
* The interface supports multiple languages: English, German, and French.
* Administrative features empower admins to adjust prompts directly within the app. They can edit text for both system and user roles, modify the super prompt, and tweak request parameters like temperature, top p, and more.
* A super prompt enables the provision of overarching instructions to GPT-4, which apply to all prompts. This can include company style guidelines, restrictions, and more.

