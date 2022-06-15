# Setup for Angular Course

###### Version 12.2.0.2

1.  A recent version of Windows (10 or later) or macOS, with current system updates and:
    - at least 4 GB of RAM
    - 8 GB is great
    - 16 GB is ideal
2.  Modern web browser:

    - Google Chrome (http://www.google.com/chrome/) – any recent version
      - Students should be able to use the Chrome Developer Tools. This overview explains how to access them:
        - https://developers.google.com/web/tools/chrome-devtools/#open
    - Please also install the following Chrome extension ( Note: this are NOT required for the course but nice to have):
      - Angular DevTools
        - https://chrome.google.com/webstore/detail/angular-devtools/ienfalfjdbdpebioblfackkekamfmbnh
      - Redux DevTools Extension
        - https://chrome.google.com/webstore/detail/redux-devtools/lmhkpmbekcpmknklioeibfkpmmfibljd
          > This extension is only used in the advanced and comprehensive courses
    - Also, any other browsers that you plan to support

3.  An IDE (Integrated Development Environment) or code editor of your choice – **Visual Studio Code OR WebStorm recommended**.

    > Visual Studio Code and WebStorm are both excellent editors for JavaScript, TypeScript, and Angular. **If you do not already have a preference, we recommend Visual Studio Code**.

    - Visual Studio Code is a free download from

      - https://code.visualstudio.com/download
        - Windows users, please select the **System Installer** if you are running as an Administrator.

      > Note that Visual Studio Code is NOT the same application as Visual Studio. It is a free open-source lightweight text editor similar to Sublime Text, Atom, or Brackets. It is a small quick install and is now [the most popular development environment](https://insights.stackoverflow.com/survey/2019#development-environments-and-tools) according to the Stack Overflow Developer Survey Results. It was created by the same guy who created the Eclipse IDE.

      - Please install the Angular Essentials - Extension Pack for VS Code by clicking the install button on this page
        - https://marketplace.visualstudio.com/items?itemName=johnpapa.angular-essentials
      - After the Angular Essentials is finished:
        - [Configure Visual Studio Code as outlined in this document](./visualstudiocode/configuration.md)

    - WebStorm is available (as an alternative to Visual Studio Code) from

      - https://www.jetbrains.com/webstorm/download
      - It comes with a free 30-day trial

      * >

    - IntelliJ IDEA Ultimate (is another alternative to Visual Studio Code) and is available from
      - https://www.jetbrains.com/idea/download/
      - WebStorm is made by the company Jetbrains who also makes IntelliJ IDEA.
      - It also contains the same editing features as WebStorm, and it has a similar free 30-day trial, so that is another possible option for class.
      - However, please note that the free IntelliJ IDEA Community Edition does NOT have the same level of support for JavaScript, TypeScript, and Angular, so anyone who plans to use IntelliJ in this class should have the Ultimate edition.

4.  Node.js installed, **Version 14.x or 16.x**

    - Any Node version 14 or later is fine for this class, but Long-Term Support (LTS) versions are preferred, so we recommend using a 16.x LTS version.
    - Please visit https://nodejs.org/ , and click the “16.15.1 LTS” (or similar) button below the “Download for [your operating system]” heading to download the installer file.

      - Run the installer, accepting all default settings.

        > Angular version 14 does not support Node versions earlier than `14.15.4`. For more information see the [Angular CLI, Angular, Node.js, TypeScript, and RxJS compatibility matrix](https://gist.github.com/LayZeeDK/c822cc812f75bb07b7c55d07ba2719b3#gistcomment-3879034.)

    - After installation, please confirm that the Path environment variable on your computer has been modified to include the path for node and npm:
    - In a Mac Terminal prompt or a Windows command prompt (in Windows 7, click the Start button and type `cmd`), run the commands:
      ```
      node -v
      npm -v
      ```
      Which should return the version number of each program.
      >     NOTE:  If you already have another version of Node.js on your machine that you use to support an existing application and you do not want to overwrite/uninstall it, please see the article below about how to run multiple versions of Node.js using nvm for Windows or nvm on a Mac.
      - https://www.sitepoint.com/quick-tip-multiple-versions-node-nvm/
    - Next, please confirm that you are able to install npm packages by running this command:
      - `npm install chalk -g`
      - On Windows, this installation may produce some warnings. If you receive an ERROR (different from a warning) that begins `Error: ENOENT, stat...`, this error usually means that npm is expecting a directory named “npm”, and you just need to create an empty “npm” directory at the location indicated in the error message. Then you should be able to rerun the install command.
        >     Note: if you receive warnings but not an error, this is fine, and you do not need to rerun anything.
      - CERT or certificate issues sometimes result from corporate firewalls particularly if they use a self-signed certificate. This post discusses various approaches to getting npm to work behind a corporate firewall.
        https://stackoverflow.com/questions/13913941/how-to-fix-ssl-certificate-error-when-running-npm-on-windows

5)  Install the Angular CLI (as an Administrator if permitted) and confirm the installation:

    >     Note: depending on your security settings, you may or may not be able to run the command prompt as Administrator for this installation.  If you run into any difficulty, please let us know.

    >     If you are permitted, please start a Command prompt as Administrator.  In most versions of Windows, you can do this by navigating to `C:\Windows\System32` in Windows Explorer, then right-click on `cmd.exe`, and select `Run as administrator`.

    In a Mac Terminal prompt or a Windows command prompt, please run this command:

    ```
    npm install -g @angular/cli@14
    ```

    - The installation may produce some warnings, but it should not have any errors. After running the install command, you can confirm a successful installation by running the command “ng v” (this should report the version of Angular CLI that’s installed).
      - You should have version `12.x.x` of the Angular CLI for the course. Note that older versions of the Angular CLI work with older versions of Angular but not Angular 12 used in this course.
      - If you have a previous version of the Angular CLI use the following command to update it:
      ```shell
      npm update -g @angular/cli@14
      ```

6)  Create a new project with the Angular CLI

    - Create an empty directory named ngverify on your machine in a location where you have permissions to create and edit files (for example, `c:\ngverify` OR `c:\users\[username]\Documents\ngverify`)
    - In the Administrator command prompt from the previous step, change the current directory to ngverify
    - Run the command:
      ```shell
          ng new demoproject --defaults=true
      ```
      - This command will take some time as it is downloading several libraries from npmjs.com.
      - When the command is finished, verify the output.
        > Note that if you receive warnings but not an error, this is fine, and you do not need to rerun anything.
    - Run the command:
      ```
      cd demoproject
      ```
    - Run the command:

      ```
      ng serve -o
      ```

      - The Angular application will build and open your default web browser and display the message ‘demoproject app is running!’
        > Note: If Internet Explorer is your default browser, you may receive a blank page. If this is the case:
        >
        > - copy the current URL: http://localhost:4200 from IE into another browser such as Chrome, Edge or Firefox
        > - In the new browser you should see the message ‘demoproject app is running!’ We will review how to configure Angular to work with Internet Explorer in class.

    - Close your browser tab and the command prompt.

7)  Internet access for all attendees and the instructor is required.
8)  You will need to have a **Git client** installed. To verify it is installed open a terminal or command-prompt and run the command:
    ```
    git --version
    ```
    - Any version should work.
    - Here is a link to a [page describing the process for installing the git client](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) if you need to install it.

8.  Your computer is now ready for class – you may exit from the Terminal / command prompt and any other programs that you were using in the setup.
