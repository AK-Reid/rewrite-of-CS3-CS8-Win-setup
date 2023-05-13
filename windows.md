# Windows Instructions

- ## [Installing `git`](#win_installing_git)
- ## [Installing `cmake`](#win_installing_cmake)
- ## [Installing `MinGW`](#win_installing_mingw)

---


# ![#f03c15](https://via.placeholder.com/15/f03c15/000000?text=+) Installing git ![#f03c15](https://via.placeholder.com/15/f03c15/000000?text=+)



## Download `git`

Grab the latest 64 bit git setup from [here](https://git-scm.com/download/win).

> <img src="images/win_images/dl-git.png" alt="vscode_after_cloning" width="600"/>

<br>

## Install `git`

Double click the executable, i.e `Git-2.40.0.1-64-bit.exe`, just keep clicking next and install. The **default options** for everything is perfectly fine.<br>


> <img src="images/win_images/git-01-download_git_12.png" alt="vscode_after_cloning" width="600"/>

#### Ensure that `git` was succesfully installed
<br>

Run `git --version` in your command prompt:<br>

> <img src="images/win_images/git-02-git_version.png" alt="vscode_after_cloning" width="500"/>
<br>

If you see the above output, you're good to go, otherwise reinstall `git`.

## Configure git:

The steps in this section are very important.

First, let git know who you are, set your global name and email address in your command prompt, this only needs to be done once.
You can paste commands into your Command Prompt by right clicking.

```
git config --global user.name "John Doe"
git config --global user.email johndoe@example.com
```
This is important because every git commit you make will have this information baked into it. This is your identity.

If you like you may also check that your name and email were set correctly with `git config --get user.name` and `git config --get user.email`

#### Personal access tokens:
**Very important:** You will not be able to clone your repositories without first setting up a GitHub Personal Access Token. This is key that grants access to all your repositories, so be very careful with it.

Go to `github.com`, click your profile picture on the top right, click on `settings`. On the sidebar of the next page click `Developer settings` at the very bottom. At the bottom of the sidebar on the next page, click `personal access tokens`

Go to your profile settings   |  Go to `Developer Settings` | Create a `classic` token
:-------------------------:|:-------------------------:|:-------------------------:
<img src="images/win_images/github-settings.png" alt="vscode_after_cloning" width="230" height="600"/>  |  <img src="images/win_images/dev-settings-github.png" alt="vscode_after_cloning" width="200" height="600"/> |  <img src="images/win_images/create-token.png" alt="vscode_after_cloning" width="320" height="600"/>



| <img src="images/win_images/generate-new-token.png" alt="vscode_after_cloning" width="810" />  |
| :----------------------------------------: |
|      **Generate a new token**     |

| <img src="images/win_images/token-access.png" alt="vscode_after_cloning" width="810"/>   |
| :----------------------------------------: |
|      **Set an expiration date, check the `repo` box, leave all the boxes below unchecked, scroll down and click `Generate token`**   |

**Set an expiration date for your tokens! I highly recommend setting a custom expiration date that's just after finals week. Around Dec 20th for Fall and June 20th for Spring should be good. In the unfortunate event your token is ever compromised months or years down the line, you wont have to worry about the tokens you generated during your studies being the reason you got fired.**

#### Finally, here is your token, this is the first and last time GitHub is going to show it to you, so put it in a secure folder or write it down on paper for future access.
<img src="images/win_images/generated-token.png" alt="vscode_after_cloning" width="800">

## Cloning a repository


The first time you attempt to clone one of your own repos you will be met with this prompt  |  Go to the `Token` tab and paste in your token
:-------------------------:|:-------------------------:
<img src="images/win_images/token-prompt.png" alt="vscode_after_cloning" width="650" >  |  <img src="images/win_images/token-paste.png" alt="vscode_after_cloning" width="400">

**After doing this once you will have permissions to clone repos unprompted.**

<br><br><br>

<a name="win_installing_cmake"></a>

# ![#f03c15](https://via.placeholder.com/15/f03c15/000000?text=+) Installing cmake ![#f03c15](https://via.placeholder.com/15/f03c15/000000?text=+)




### Download `cmake`

Download cmake from [here](https://cmake.org/download/). Choose the `Windows win64-x64 Installer`. You should get an msi with a name similar to this: `cmake-3.19.4-win64-x64.msi`<br>

> <img src="images/win_images/cm-00-download_site.png" alt="vscode_after_cloning" width="700"/>

<br>

You may blindly click through the setup wizard, except for setting the path  |  Important: Make sure to select `Add CMake PATH for all users`
:-------------------------:|:-------------------------:
<img src="images/win_images/cm-01-download_00.png" alt="vscode_after_cloning" width="500"/> |  <img src="images/win_images/cm-01-download_03.png" alt="vscode_after_cloning" width="510" />

### Check that cmake was installed succesfully:

To make sure `cmake` is intalled correctly, run `cmake --version`:
<br>

> <img src="images/win_images/cm-02-cmake_version.png" alt="vscode_after_cloning" width="600"/>

If you see something like this, you're good to go!

<br>

---


<a name="win_installing_mingw"></a>

# ![#f03c15](https://via.placeholder.com/15/f03c15/000000?text=+) Install MinGW ![#f03c15](https://via.placeholder.com/15/f03c15/000000?text=+)


## Download `MinGW`

Download MinGW from [here](https://github.com/niXman/mingw-builds-binaries/releases). Download the release in below screenshot
> <img src="images/win_images/mingw-64.png" alt="64 mingw release" width="800"/>

Once downloaded use your favorite archive manager(e.g WinRAR, 7-Zip) to extract the archive straight to your C:\ drive
> <img src="images/win_images/extract-mingw.png" alt="Extract the release, technically it can go anywhere you like, just set the path in the next step" width="700"/>



## Set your path environment variable for C++

Search for "path" in the task bar search box. Open Edit the system environment variables.

Edit `system  environment variables`   |  Click `Environment Variables` | Select `Path` variable and click `Edit`| Click 'New' and paste in your `MinGW` path `C:\mingw64\bin`
:-------------------------:|:-------------------------:|:-------------------------:|:-------------------------:
<img src="images/win_images/system-vars.png" alt="vscode_after_cloning" width="500">   |  <img src="images/win_images/enviro-vars.png" alt="vscode_after_cloning" width="500" /> |  <img src="images/win_images/edit-path.png" alt="vscode_after_cloning" width="500" > |  <img src="images/win_images/new-path.png" alt="vscode_after_cloning" width="500"/>


> <img src="images/win_images/g++-03-path_00.png" alt="vscode_after_cloning" width="600"/>

<br>

Click on "Environment Variables..."

> <img src="images/win_images/g++-03-path_01.png" alt="vscode_after_cloning" width="600"/>

<br>

Add the path to the gcc and g++ executables to environment variables as shown below and press OK.<br>

> <img src="images/win_images/g++-03-path_02.png" alt="vscode_after_cloning" width="600"/>

<br>

Next, double click on the **user variable** Path (in the top half of the window). A window like this should pop up:

> <img src="images/win_images/g++-03-path_before.png" alt="vscode_after_cloning" width="600"/>

<br>

Click New, and enter C:\MinGW\bin to the text box. Click OK.<br>

> <img src="images/win_images/g++-03-path_after.png" alt="vscode_after_cloning" width="400"/>

<br>

Your environment and user variables should look like this after you are done:<br>

> <img src="images/win_images/g++-03-path_03.png" alt="vscode_after_cloning" width="400"/>

<br><br><br>

## Check the version of the g++ again:

To make sure `MinGW`/`g++` is intalled correctly, run `g++ --version` again. If the version output doesn't show, reboot your machine and try again.<br><br>

> <img src="images/win_images/g++-00-g++_version.png" alt="vscode_after_cloning" width="1000"/>

<br>

---

## Once all software has been installed, continue to the [next step](start_project.md)
