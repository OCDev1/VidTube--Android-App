# VidTube-Android app
<img src="/Android-app-screenshots/logo_vidtube.png" alt="Example Image" width="300">

The VidTube app is a video sharing app, made for allowing users across the world to upload and share their video content, comment their thoughts and interact with each other.
This Readme file contains an overview of the Android app and its features, along with a guide on how to run it on your machine.

## How To Run
In order to run the Android app, start by cloning the repository to Android Studio, you can do this by opening the terminal and entering this command:
`git clone https://github.com/eyalg43/project_android.git`.

After cloning the repository, open the project in Android Studio.
(Note: if you are using a physical device, make sure to change the code, such that in every place that it says "10.0.2.2", change it to your IP address)

Now clone the server using your IDE of choice, you can do this by opening the terminal and entering this command: `git clone https://github.com/OCDev1/VidTube-server.git` Or download the repository to your computer.

If you downloaded the repo-change the directory in your terminal to the downloaded repo directory. (if you cloned to your IDE then ignore this)

While in the project directory run:
### `npm install`

and wait for it to finish installing.

### Setting up config and .env.local
In the project directory go to the "config" folder (its in the main project directory) and inside it you will find a file called ".env.local", inside
".env.local" change the conncetion string to the connection string of your MongoDB, and set PORT to 12345.
it should look something like this:

`CONNECTION_STRING=mongodb://localhost:27017/vidtube` (change to the connection string of your MongoDB)
<br>`PORT=12345` (NOTE: you must use 12345 for it to work)
<br>there is also `JWT_SECRET=your_secret_key` (you can ignore this)

* Open MongoDB on your computer.

### insertData.js script

* Included in the project is a script called "insertData.js" which will initialize the database with users, videos and comments. we highly reccomend you run this script in order to get the best experience and see all the features (and also to save you some time (: )

* You can run the script by typing `node insertData.js` wait for the script to finish and your database should be initialized with videos, users and comments, hooray!

* NOTE: in order for the DB to be initialized with the users, videos and comments of the script, make sure you dont already have a database called "vidtube" (or else the script won't add it's data), if you do then delete the database and run the script again.

Now you can run

### `npm start`

Because this is for the 4th part, you should also ensure that the CPP server of the 4th part runs.

Now go back to Android studio and run the app, now you should be able to use the app!
Now you are all set up, enjoy!

## Our work process:
As usual, we started off by watching Hemi's videos, we set up the android to be in an MVVM architecture. Each group member had his responsibility, Eyal was responsible for the comments, Omri was responsible for the users and Max was responsible for the videos. We modified our code to work with the server we made in part 2, so the videos, comments and users are being kept in the database. We also added features that take advantage of the server like: users can edit and delete their own videos and comments, likes and dislikes are being saved and more.

### NEW!
* You can now delete your account or edit your user details in your profile page, you can reach it by clicking on the "You" option in the side menu.

* In the watch video screen, clicking the uploaders image or name will take you to his profile page where you can see more videos that he uploaded.

* Clicking your profile picture in the side menu will take you your videos page, in which you can edit and delete your videos.

* Users can now edit and delete only their own comments and videos.


## Android App Features:
* After running the app, the emulator (or device if ran on a physical device) will open and you will be brought to the **Home Activity**

* The **Home Activity** contains many exciting features such as:
    * A video list displaying some of the videos on the platform
    * A search bar where you can filter videos by title
    * A side menu where you have the ability to sign in (or sign up and then sign in) which unlocks more features such as:
        * Upload video - share your videos and content with the world (note: videos must contain a title, description, thumbnail etc.).
        * Edit video - allows you to change video title, description, thumbnail, or the video itself.
        * Delete video - don't want your video to appear on VidTube? you can easily delete it.
        * Commenting on a video (in the watch-video Activity).
    * Dark mode, which works across the entire app, this can be accessed and toggled via the side menu.

* The **Watch-Video** Activity contains even more great functionality:
    * The video itself with Pause, Play and a time line to jump ahead or back.
    * Interesting details about the video such as the author, author image, views, how long ago the video was uploaded, the description etc.
    * A list under the video with lots of recommended videos for you to watch and enjoy, each better than the last.
    * The ability to share your thoughts with buttons such as 'Like', 'Dislike', and 'Subscribe'.
    * You can also share your thoughts via the comment section (note: you must be logged in to comment, and comment must contain text)
      where you can like or dislike other peoples' comments, post a comment on your behalf with your Display name and profile picture,
      and also delete and edit comments (again, you must be logged in to edit and delete).

* The **Upload-Video** Activity:
    * Here you can share your video content with the world!
    * Choose a catchy title, informative description, an eye catching thumbnail and then select the video you want to share.
      click 'Upload To Vidtube' and your video can be seen on VidTube!
    * Your new video will be posted under your Display name and your profile picture.
    * Having second thoughts? don't worry, just click the 'cancel' button and you will be brought back to the Home Activity!

* The **Edit-Video** Activity:
    * We believe in second chances! Here you can edit videos, and change their title, description, thumbnail or the video itself.
    * Having second thoughts? don't worry, just click the 'cancel' button and you will be brought back to the Home Activity!

* The **Sign-in** Activity:
    * Sign in with your Username and password (make sure your account exists first) to unlock features such as commenting, editing, deleting and uploading videos and many more!
    * Don't have an account? No worries! click the "Don't have an account? Sign up here." text and you will be brought to the Sign-up Activity, where you can create an account.

* The **Sign-up** Activity:
    * Sign up by choosing your own Username, Display name, profile picture and password (and Verifying your password) to create your very own VidTube account and unlock features such as commenting, editing, deleting and uploading videos and many more!
    * You can upload a profile picture from your phone, or take a picture using your phone camera using the "Take photo" button.
    * Make sure your password fits the criteria and that your password and verification password match, or else you wont be allowed to sign up.


# 📷 Screenshots from the Android app:
## Home Activity (and switching to dark mode):
<img src="/Android-app-screenshots/Screenshot_1.png" alt="Example Image">
<img src="/Android-app-screenshots/Screenshot_2.png" alt="Example Image">
<img src="/Android-app-screenshots/Screenshot_3.png" alt="Example Image">
<img src="/Android-app-screenshots/Screenshot_4.png" alt="Example Image">

## Log in Activity (and signing up):
<img src="/Android-app-screenshots/Screenshot_5.png" alt="Example Image">

## Sign-up Activity (and uploading image from camera):
<img src="/Android-app-screenshots/Screenshot_6.png" alt="Example Image">
<img src="/Android-app-screenshots/Screenshot_7.png" alt="Example Image">
<img src="/Android-app-screenshots/Screenshot_8.png" alt="Example Image">
<img src="/Android-app-screenshots/Screenshot_9.png" alt="Example Image">
<img src="/Android-app-screenshots/Screenshot_10.png" alt="Example Image">
<img src="/Android-app-screenshots/Screenshot_11.png" alt="Example Image">

## Watch-Video Activity:
<img src="/Android-app-screenshots/Screenshot_37.png" alt="Example Image">

## Watch-Video Activity (Like, Dislike, Comments-post, edit, delete, like, dislike):
<img src="/Android-app-screenshots/Screenshot_19.png" alt="Example Image">
<img src="/Android-app-screenshots/Screenshot_20.png" alt="Example Image">
<img src="/Android-app-screenshots/Screenshot_21.png" alt="Example Image">
<img src="/Android-app-screenshots/Screenshot_22.png" alt="Example Image">
<img src="/Android-app-screenshots/Screenshot_23.png" alt="Example Image">
<img src="/Android-app-screenshots/Screenshot_24.png" alt="Example Image">
<img src="/Android-app-screenshots/Screenshot_25.png" alt="Example Image">
<img src="/Android-app-screenshots/Screenshot_26.png" alt="Example Image">
<img src="/Android-app-screenshots/Screenshot_27.png" alt="Example Image">
<img src="/Android-app-screenshots/Screenshot_28.png" alt="Example Image">
<img src="/Android-app-screenshots/Screenshot_30.png" alt="Example Image">
<img src="/Android-app-screenshots/Screenshot_29.png" alt="Example Image">

## Watch-Video Activity - Dark Mode:
<img src="/Android-app-screenshots/Screenshot_18.png" alt="Example Image">
<img src="/Android-app-screenshots/Screenshot_36.png" alt="Example Image">

## Upload-Video Activity:
<img src="/Android-app-screenshots/Screenshot_12.png" alt="Example Image">
<img src="/Android-app-screenshots/Screenshot_13.png" alt="Example Image">
<img src="/Android-app-screenshots/Screenshot_14.png" alt="Example Image">
<img src="/Android-app-screenshots/Screenshot_145.png" alt="Example Image">
<img src="/Android-app-screenshots/Screenshot_15.png" alt="Example Image">
<img src="/Android-app-screenshots/Screenshot_16.png" alt="Example Image">

## Edit-Video Activity (and editing a video):
<img src="/Android-app-screenshots/Screenshot_31.png" alt="Example Image">
<img src="/Android-app-screenshots/Screenshot_32.png" alt="Example Image">
<img src="/Android-app-screenshots/Screenshot_33.png" alt="Example Image">
<img src="/Android-app-screenshots/Screenshot_34.png" alt="Example Image">
<img src="/Android-app-screenshots/Screenshot_345.png" alt="Example Image">

## Edit-Video Activity - Dark Mode:
<img src="/Android-app-screenshots/Screenshot_35.png" alt="Example Image">

## Edit-User Activity:
<img src="/Android-app-screenshots/Screenshot_50.png" alt="Example Image">
<img src="/Android-app-screenshots/Screenshot_51.png" alt="Example Image">
<img src="/Android-app-screenshots/Screenshot_52.png" alt="Example Image">
<img src="/Android-app-screenshots/Screenshot_53.png" alt="Example Image">
<img src="/Android-app-screenshots/Screenshot_54.png" alt="Example Image">
<img src="/Android-app-screenshots/Screenshot_55.png" alt="Example Image">

## User-Videos Activity:
<img src="/Android-app-screenshots/Screenshot_60.png" alt="Example Image">
<img src="/Android-app-screenshots/Screenshot_61.png" alt="Example Image">
<img src="/Android-app-screenshots/Screenshot_62.png" alt="Example Image">
<img src="/Android-app-screenshots/Screenshot_63.png" alt="Example Image">

## Swipe to refresh:
<img src="/Android-app-screenshots/Screenshot_70.png" alt="Example Image">
<img src="/Android-app-screenshots/Screenshot_71.png" alt="Example Image">
