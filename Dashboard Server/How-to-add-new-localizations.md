#Adding new localizations

Create your own culture texts for the Syncfusion Dashboard Server and add it in an application at anytime.

To use different cultures of Syncfusion Dashboard Server, follow the given steps:

1. Open the [Google Translator Kit](https://translate.google.com/toolkit), and click the Upload.

    ![Open Google Translator Kit](images/add-localization-1.png)

    It will open a new window to upload the existing culture file en-us. Then, click the `Add content to translate` link in the screen.
    
    ![Add content to translate](images/add-localization-2.png)
 
2. Select the `Upload file` option in the drop-down.

    ![Upload](images/add-localization-3.png)
 
3. Upload the [default.po](locale/default.po) file which contains the texts from the Dashboard Server application, `~Installed Drive~\Syncfusion\Dashboard Server\DashboardServer.Web\locale into google translator`.

    For example: `C:\Syncfusion\Dashboard Server\DashboardServer.Web\locale`

4. Make sure that the source language is in English and file name as `messages` as shown in the following image.

    ![Source Language](images/add-localization-4.png)
    
    Select the desired language in the listed languages and click `Next`.
    
5. In the next screen, select `Start Order`, if you need paid service on translation; otherwise select `No, thanks`.

    ![Start Order or No thanks](images/add-localization-5.png)
 
6. The uploaded file will be listed in the home page of translator kit. Click the file to open it and make any corrections in the translation if needed.

    ![Translator Home page](images/add-localization-6.png)
 
7. Click `Complete` at the top-right corner of the page to complete the translation.

    ![Complete](images/add-localization-7.png)
 
8. Download the translated `messages.po` file.

    ![Download Messages.po](images/add-localization-8.png)
 
9. Create a folder in `~Installed Drive~\Syncfusion\Dashboard Server\DashboardServer.Web\locale` with {language code}-{country code} and paste the downloaded messages.po file inside the newly created folder.

    For example, if you are translating to Italian, create a folder named `it-it` and paste the messages.po as follows.
    
    `C:\Syncfusion\Dashboard Server\DashboardServer.Web\locale\it-it\messages.po`
    
    Newly added language will be listed in the language list after refreshing the page in the Dashboard Server.
    
    ![New Languages](images/add-localization-9.png)
