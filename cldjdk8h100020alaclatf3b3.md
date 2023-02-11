# Your First ReactNative App - Windows

## What is covered in this article?

1. Prerequisites for running your first react-native app.
    
2. Setting environment variables.
    
3. Running your first app.
    
4. Bonus tips to save you from headaches.
    

## 1\. Prerequisites:

* [VS Code(love it)](https://code.visualstudio.com/download)
    
* [Node.Js version 14 or higher](https://nodejs.org/en/)
    
* [JAVA](https://www.oracle.com/in/java/technologies/downloads/)
    
* [Android Studio](https://developer.android.com/studio)
    
* **Android device(To actually test the apps physically)**
    
* **Data Cable**
    

---

## 2\. Environment Variables:

In order to utilize the installed packages or libraries, in general, we need to make our computer learn and remember the places where it can find these packages whenever required, where environment variables come into play.

Now that we installed the required executables, we will set the environment variable for the same.

1. Go to the search bar in your computer and type <mark>environment variables</mark> and select the option shown below.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675113815214/f1ea7119-cf82-4ae6-b3f2-e1ac2b5ae4de.png align="center")
    
2. Click on the <mark>environment variables</mark>.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675113946305/e42237cd-7a98-4cc2-8ea4-610c044515e5.png align="center")
    
3. Under *<mark>system variables</mark>* click on *<mark>Path -&gt; Edit -&gt; New</mark>*
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675114088770/8d8b40fc-28a3-42d0-83c9-59b268eea05b.png align="center")
    
4. Paste the path to <mark>SDK TOOLS</mark> and press <mark>ok</mark> e.g.,
    
    *C:\\Users\\moeen\\AppData\\Local\\Android\\Sdk\\platform-tools*
    
    note: change your *user according to your own machine.*
    
    Now repeat the same process for the *JAVA* <mark>bin </mark> folder and you are done.
    

---

## 3.Let's run our first app:

Now that we have set up an environment for development, let's build our first react-native app.

create a folder named e.g., react-native and open it in *vscode and enter the below command to initialize the project*

1. ```plaintext
          npx react-native init ProjectName
    ```
    

This command will install all the required dependencies into the project directory and will look something like this.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675115160768/0869cb4e-9996-4625-b708-d994b0a72c70.png align="center")

1. Type the below command in the terminal, it will start building the application so that it is executable on the android device.
    
    ```plaintext
    npx react-native run-android
    ```
    
    You will get a prompt like the one below, press the character *'a'*
    
    meaning *android*
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675115809612/7ad1def8-deb3-46ac-8cf2-d17b71a051a3.png align="center")
    
2. Now for the first time, it may take a bit of time for bundling all the things together, and may run into some potential issues which I will cover in the next section. Once done, VIOLA! you can see the app up and running on your android device.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675116122436/9f358737-3e1e-4a7c-9cd9-7fbb457e3c84.jpeg align="center")
    

---

## 4\. Potential issues & Solutions:

Now, I have written everything in order so that it will be seamless for you to set up the environment and run your first app but you may get issues related to a *variable* that may hinder the process of execution while trying to run the app on the device and to solve that, please follow the below few steps.

1. navigate into the <mark>project folder -&gt; android</mark> and create a file named `local.properties` and create the below variable (note: mention the path according to your own user)
    
2. Save the below variable in the file(note: mention the path according to your own user)
    
    ```plaintext
    sdk.dir=C:\\Users\\moeen\\AppData\\Local\\Android\\Sdk
    ```
    

---

## Connect with the author

[LinkedIn](https://www.linkedin.com/in/moeenulislam/)  
[Twitter](https://twitter.com/moeenulislam_)  
[Hashnode](https://moeen.hasnode.dev)