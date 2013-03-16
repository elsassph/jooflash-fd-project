Jangaroo Flash Application Project Template for FlashDevelop
============================================================

For Jangaroo background information, please visit the [Jangaroo Home Page](http://www.jangaroo.net).

You need to have installed the usual Jangaroo prerequisites

1. [Java 6](http://java.sun.com/javase/downloads/) and
2. [Maven 3](http://maven.apache.org/download.html).

Note that you do not have to download and / or install Jangaroo itself!

**Checkpoint:** opening a command prompt and entering `mvn -v` should output something like

    Apache Maven 3.0.2 (r1056850; 2011-01-09 01:58:10+0100)
    Java version: 1.6.0_21, vendor: Sun Microsystems Inc.
    Java home: C:\Program Files\Java\jdk1.6.0_21\jre
    Default locale: de_DE, platform encoding: Cp1252
    OS name: "windows 7", version: "6.1", arch: "amd64", family: "windows"

Now, install [FlashDevelop](http://www.flashdevelop.org).

To set up the Jangaroo Flash Project template for FlashDevelop

1. Download this project as a [`ZIP`](https://github.com/elsassph/jooflash-fd-project/archive/master.zip),
2. unzip the subfolders `10 Jangaroo - JooFlash Project` and `11 Jangaroo - Web Project` contained in the archive into the `Projects` directory of your FlashDevelop installation. (You may have to unzip to a temporary directory and copy over to the program directory to be asked for admin rights.)

Then, you can create Jangaroo HTML5 Flash Applications from FlashDevelop using

1. `Project | New Project...`
2. Select `Jangaroo | JooFlash Project` from the list.
3. Fill in desired `Name`, `Location` and `Package` of your new project.

   You usually want to check `Create directory for project`.

![screenshot](https://github.com/elsassph/jooflash-fd-project/raw/master/FlashDevelop-Jangaroo-Flash-Project-Screenshot.png "Dialog for creating a Jangaroo project in FlashDevelop")

Now you can build the project using the `Test Project` toolbar button (or press F5 or Ctrl+Enter). Maven is invoked and compiles and builds your Web application.
Then, your default browser opens your Jangaroo application.
Now you can edit source code, click `Build Project` again (or press F8), and watch the result in the browser window. If changes do not appear, try clearing the browser cache.

For debugging, please have a look at the [Jangaroo debugging tutorial](http://www.jangaroo.net/tutorial/debugging).

**Optional Setup**

Loading the application from the local filesystem has some disadvantages. IE keeps on asking whether you want local scripts to execute. Debugging is not as nice, as Firebug's Network tab stays empty. Ajax requests (which jooflash uses for [Embed(...)] of text files) do not work.

To improve the situation, Maven allows starting a local Web server serving your Web app:
- Execute `start-server.bat` to start the server (keep this command window running),
- Navigate to `http://localhost:8080`

To always open the server page, you can change the url in `Project Properties | Test Project | Open Document | Edit...`.
