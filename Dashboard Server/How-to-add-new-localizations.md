#Adding new localizations for Local Server

Create your own culture texts for the Syncfusion Dashboard Server and add it in the application anytime.

To make Syncfusion Dashboard Server use a different culture perform the following steps:

1. Open [Google Translator Kit](https://translate.google.com/toolkit). Click on Upload button.

    ![Open Google Translator Kit](images/add-localization-1.png)

    It will open a new window to upload the existing culture file en-us. Then click on `Add content to translate` link in the screen.
    
    ![Add content to translate](images/add-localization-2.png)
 
2. Select `Upload file` option in the dropdown.

    ![Upload](images/add-localization-3.png)
 
3. Upload [default.po](locale/default.po) file which contains the texts from the Dashboard Server application from `~Installed Drive~\Syncfusion\Dashboard Server\DashboardServer.Web\locale into google translator`.

    For example: `C:\Syncfusion\Dashboard Server\DashboardServer.Web\locale`

4. Make sure that the source language is in English and file name as `messages` as in the below image.

    ![Source Language](images/add-localization-4.png)
    
    Select your desire language in the listed language and click `Next`.
    
5. In the next screen, select `Start Order`, if you need paid service on translation; otherwise select `No, thanks`.

    ![Start Order or No thanks](images/add-localization-5.png)
 
6. The uploaded file will be listed in home page of translator kit. Click on the file to open it and make any corrections in the translation if needed.

    ![Translator Home page](images/add-localization-6.png)
 
7. Click on `Complete` on the right-top corner of the page to complete the translation.

    ![Complete](images/add-localization-7.png)
 
8. Download your translated `messages.po` file.

    ![Download Messages.po](images/add-localization-8.png)
 
9. Create a folder in `~Installed Drive~\Syncfusion\Dashboard Server\DashboardServer.Web\locale` with {language code}-{country code} and paste the downloaded messages.po file inside the newly created folder.

    For example, if you are translating to Italian, create a folder named `it-it` and paste the messages.po like the below.
    
    `C:\Syncfusion\Dashboard Server\DashboardServer.Web\locale\it-it\messages.po`
    
    Newly added language will be listed in language list in Dashboard Server after refreshing the page in the Dashboard Server.
    
    ![Locale-Folder](images/locale-folder.png)

#Adding new localizations for Azure Web App

Create your own culture texts for the Syncfusion Dashboard Server and add it in an application at anytime.

To use different cultures of Syncfusion Dashboard Server, follow the given steps:

1. Open the [Google Translator Kit](https://translate.google.com/toolkit) and click the upload.

    ![Open Google Translator Kit](images/add-localization-1.png)

    It will open a new window to upload the existing culture file en-us. Then, click the `Add content to translate` link in the screen.
    
    ![Add content to translate](images/add-localization-2.png)
 
2. Select `Upload file` option in the drop-down.

    ![Upload](images/add-localization-3.png)


   The [default.po](locale/default.po) file that contains the texts from the Dashboard Server application is needed from the Azure portal.

    To download the `default.po` file, follow the given steps:

    ### Stop the Dashboard Server App Service

    `Step 1:` Login to Azure portal: https://portal.azure.com.

    `Step 2:` Select App Services in Microsoft Azure Services.

    `Step 3:` Choose the Dashboard Server Azure App Service.

    `Step 4:` In the overview section, click the stop.

    ![Azure-Site-Stop](images/azure-stop.png)

    ### Get existing Azure blob storage details

    Follow the given steps and get the existing Azure blob storage details:

    `Step 1:` Login to Azure portal: https://portal.azure.com.

    `Step 2:` Select App Services in Microsoft Azure Services.

    `Step 3:` Choose the existing Syncfusion Dashboard Server Site, and then, click the get publish profile.

    ![Azure-Get-Publish-Profile](images/azure-publish-profile.png)

    `Step 4:` Save the <App service name>.PublishSettings file and open it. The file contains 2 <publishProfile> sections for web deploy and FTP.

    `Step 5:` From the FTP <publishProfile> section, copy the following values:
    * publishUrl
    * userName
    * userPWD

    ![FTP-Credential](images/ftp-credential.png)

    `Step 6:` Apply the copied credentials to the host, username, and password fields in the FTP client FileZilla as shown here and click the quickconnect.

    ![FileZilla](images/filezilla.png)

    `Step 7:` Download the `default.po` file from the `/site/wwwroot/locale` folder in the existing Azure App Service through FileZilla.

4. Upload the downloaded file and make sure that the source language is in English and the file name as `messages` like in the following image.

    ![Source Language](images/add-localization-4.png)
    
    Select the desired language in the listed languages and click `Next`.
    
5. In the next screen, select `Start Order`, if you need paid service on translation; otherwise select `No, thanks`.

    ![Start Order or No thanks](images/add-localization-5.png)
 
6. The uploaded file will be listed in the home page of translator kit. Click the file to open it and make corrections in the translation if needed.

    ![Translator Home page](images/add-localization-6.png)
 
7. Click `Complete` at the top-right corner of the page to complete the translation.

    ![Complete](images/add-localization-7.png)
 
8. Download the translated `messages.po` file.

    ![Download Messages.po](images/add-localization-8.png)

9. Create a folder with {language code}-{country code} and paste the downloaded messages.po file inside the `locale` folder in the local machine.

    Move the entire `locale` folder to Azure portal using FileZilla.

    For example, if you are translating to Italian, create a folder named `it-it` and paste the messages.po as follows.

    \site\wwwroot\locale\it-it\messages.po

10. In the **Overview** section of the Dashboard Server Azure App Service, click **Start**.

    ![Azure-Start](images/azure-start.png)

    Newly added language will be listed in the language list after refreshing the page in the Dashboard Server.

    ![Locale-Folder](images/locale-folder.png)
