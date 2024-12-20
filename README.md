# appium-expandtesting_UI

UI testing in [expandtesting](https://practice.expandtesting.com/notes/app/) note app. This project contains basic examples on how to use Appium and Robot Framework to test UI tests. Good practices such as hooks, custom commands and tags, among others, are used. All the necessary support documentation to develop this project is placed here. 

# Pre-requirements:

| Requirement                     | Version        | Note                                                            |
| :------------------------------ |:---------------| :-------------------------------------------------------------- |
| Visual Studio Code              | 1.89.1         | -                                                               |
| Node.js                         | 22.11.0        | -                                                               |
| Python                          | 3.13.1         | -                                                               |
| JDK                             | 23             | -                                                               |
| Anroid Studio                   | 2024.2.1.11    | -                                                               |
| Appium                          | 2.13.1         | -                                                               |
| Appium Doctor                   | 1.16.2         | -                                                               |
| Appium Inspector                | 2024.12.1      | -                                                               |
| uiautomator2 driver             | 3.9.2          |                                                                 |
| Virtual device                  | Pixel 4        |                                                                 |
| API                             | 29             |                                                                 |
| uiautomator2 driver             | 3.9.2          |                                                                 |
| Robot Framework                 | 7.1.1          | -                                                               | 
| robotframework-appiumlibrary    | 2.1.0          | -                                                               | 
| Robot Framework Language Server | 1.13.0         | -                                                               | 

# Installation:

- See [Visual Studio Code page](https://code.visualstudio.com/) and install the latest VSC stable version. Keep all the prefereced options as they are until you reach the possibility to check the checkboxes below: 
  - :white_check_mark: **Add "Open with code" action to Windows Explorer file context menu**; 
  - :white_check_mark: **Add "Open with code" action to Windows Explorer directory context menu**.
Check then both to add both options in context menu.
- See [Node.js page](https://nodejs.org/en) and install the aforementioned Node.js version. Keep all the preferenced options as they are.
- See [python page](https://www.python.org/downloads/) and download the latest Python stable version. Start the installation and check the checkboxes below: 
  - :white_check_mark: **Use admin privileges when installing py.exe**, :white_check_mark: **Add python.exe to PATH** and :point_right:**Customize installation**;
  - :point_right:**Next**; 
  - :white_check_mark:**Install Python 3.13 for all users**, set **Customize install location** as **C:\Python313**, click :point_right:**Install**;
  - :point_right:**Yes** to accept changes in the system;
  - :point_right:**Close** after installation is done.
- See [JDK Development Kit 23 downloads](https://www.oracle.com/in/java/technologies/downloads/#jdk23-windows), download the proper version for your OS and install it by keeping the preferenced options. 
- See [Anroid Studio download page](https://developer.android.com/), download the last version and install it by keeping the preferenced options. Open Virtual Device Manager and create an image as simple as possible. 
- Open your terminal in your project directory and execute ```npm init``` to initiate a project.
- Open your terminal in your project directory and execute ```npm i appium``` to install Appium.
- Open your terminal in your project directory and execute ```npm i appium-doctor``` to install Appium Doctor.
- Right click :point_right:**My Computer** and select :point_right:**Properties**. On the :point_right:**Advanced** tab, select :point_right:**Environment Variables**, and then edit JAVA_HOME to point to where the JDK software is located, for example, C:\Program Files\Java\jdk-23.
- Right click :point_right:**My Computer** and select :point_right:**Properties**. On the :point_right:**Advanced** tab, select :point_right:**Environment Variables**, and then edit ANDROID_HOME to point to where the sdk software is located, for example, C:\Users\user\AppData\Local\Android\Sdk.
- Right click :point_right:**My Computer** and select :point_right:**Properties**. On the :point_right:**Advanced** tab, select :point_right:**Environment Variables**, and then edit Path system variable with the new %JAVA_HOME%\bin and %ANDROID_HOME%\platform-tools entries.
- Open your terminal in your project directory and execute ```npx appium-doctor --android``` to run Appium Doctor and check Appium instalation status.
- Open your terminal in your project directory and execute ```npx appium driver install uiautomator2``` to install drivers for automationName and platformName capabilities.
- See [Appium Inspector download page](https://github.com/appium/appium-inspector/releases), download and install it. Configure capabilities as below and save it:

  ```
  {
    "platformName": "Android",
    "appium:deviceName": "Android Emulator",
    "appium:automationName": "UIAutomator2",
    "appium:app": "C:\\appium-expandtesting_UI\\apps\\apiClient.apk",
    "adbExecTimeout": 60000,
    "appium:autoGrantPermissions": true
  }
  ```  
- Open windows propmpt as admin and execute ```pip install robotframework``` to install Robot Framework.
- Open windows propmpt as admin and execute ```pip install robotframework-appiumlibrary``` to install Appium Library for Robot Framework.
- Look for Robot Framework Language Server in the extensions marketplace and install the one from Robocorp.
- Open your terminal in your project directory and execute ```npx appium``` to start appium session.
- Execute Virtual Device Manager on Android Studio.
- Open Appium Inspector and start the appium session. 

# Tests:

- Execute ```robot -d ./results tests``` to run all tests in headless mode and store results in separated folder.
- Hit :point_right:**Testing** button on left side bar in VSC and choose the tests you want to execute.

# Support:

- [expandtesting API documentation page](https://practice.expandtesting.com/notes/api/api-docs/)
- [expandtesting API demonstration page](https://www.youtube.com/watch?v=bQYvS6EEBZc)
- [AppiumLibrary](https://serhatbolsu.github.io/robotframework-appiumlibrary/AppiumLibrary.html)
- [Quickstart Intro](https://appium.io/docs/en/latest/quickstart/)
- [Download ApiClient : REST API Client APK](https://apiclient-rest-api-client.en.softonic.com/android/download)
- [ChatGPT](https://chatgpt.com/)

# Tips:

- UI and API tests to send password reset link to user's email and API tests to verify a password reset token and reset a user's password must be tested manually as they rely on e-mail verification.  
- ChatGPT helped a lot when dealing with github actions.  
