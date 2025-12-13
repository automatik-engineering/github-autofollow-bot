# github-autofollow-bot 

This Python script automates the process of following or unfollowing users on GitHub. Designed for educational purposes, the script facilitates automated interactions with GitHub users and stargazers on repository pages, offering configurable options for a customizable experience. During the 2FA authentication process, you can manually enter the OTP code in Microsoft Edge to ensure seamless automation.
E
| Author's Note                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------|
| Sorry for the late update. Please disregard the "YES" option in the 2FA verification, as it requires multiple processes, especially with device passkeys. I will focus on automating the bypass of 2FA verification using GitHub recovery codes only, allowing you to manually enter the OTP code from your email. Thanks! 👀 |

## bugs i encountered
```
Traceback (most recent call last):
  File "D:\Users\********\AppData\Local\Programs\Python\Python311\Lib\site-packages\selenium\webdriver\common\service.py", line 95, in start
    path = SeleniumManager().driver_location(browser)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "D:\Users\********\AppData\Local\Programs\Python\Python311\Lib\site-packages\selenium\webdriver\common\selenium_manager.py", line 74, in driver_location
    result = self.run((binary, flag, browser))
             ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "D:\Users\********\AppData\Local\Programs\Python\Python311\Lib\site-packages\selenium\webdriver\common\selenium_manager.py", line 93, in run
    raise SeleniumManagerException(f"Selenium manager failed for: {command}.\n{stdout}{stderr}")
selenium.common.exceptions.SeleniumManagerException: Message: Selenium manager failed for: D:\Users\*********\AppData\Local\Programs\Python\Python311\Lib\site-packages\selenium\webdriver\common\windows\selenium-manager.exe --browser edge.
ERROR   error sending request for url (https://msedgedriver.azureedge.net/LATEST_RELEASE_143_WINDOWS): error trying to connect: dns error: No such host is known. (os error 11001)
```
- [DOWNLOAD Microsoft Edge WebDriver](https://developer.microsoft.com/en-us/microsoft-edge/tools/webdriver/), file name: edgedriver_win64.zip
- Check your Edge version, `CTRL + E` paste `edge://settings/help `
- extract downloaded file: `edgedriver_win64.zip`, copy this file named `msedgedriver.exe`, paste it here `D:\Users\********\Downloads\github-autofollow-bot-main\msedgedriver.exe`


## Features

- **Follow or Unfollow:** Choose to follow or unfollow users based on your preference.
- **Target Options:**
  - **Stargazers:** Automatically follow or unfollow stargazers of a specified repository.
  - **GitHub Users:** Follow or unfollow the followers of a specific GitHub user.
- **Default Targets:**
  - **GitHub User:** https://github.com/lamarry69
  - **GitHub Repository:** https://github.com/gradle/gradle
- **Configurable Settings:**
  - **Starting Page Number:** Specify the page number to start following or unfollowing users.
  - **Speed Mode:** Choose a speed mode for the automation process to manage anti-detection.
- **2FA Authentication:**
  - **Verification Option:** Manually enter the OTP code to bypass 2FA authentication. (during automation process)
    - **IMPORTANT:** Please select "NO" if you have already completed your 2FA authentication. In case you miss this, the script will display a warning for you to check.


## Logging

The script provides detailed logs of the actions performed, helping you track the status and results of the automation process.

## Disclaimer

Please use this script responsibly and abide by all relevant terms and conditions while using GitHub.

## Setup

1. **Clone the repository:** 
   ```sh
   git clone https://github.com/VIRUZ801/github-autofollow-bot.git
   cd github-autofollow-bot
   ```
   
2. **Create a virtual environment and activate it:**
   ```sh
   # Linux
   python -m venv venv
   source venv/bin/activate 
   ```
   ```sh
   # Windows
   python -m venv venv
   venv\Scripts\activate
   ```
   
   
3. **Install the dependencies:**
   ```sh
   pip install -r requirements.txt
   ```
   
4. **Create a .env file and add your GitHub credentials:**
   ```sh
   GITHUB_USERNAME=your_github_username
   GITHUB_PASSWORD=your_github_password
   ```
   
5. **Run the script:**
   ```sh
   python autofollow.py # use ms_edge browser 
   ```

## License

This project is licensed under *The Unlicense*.

## Credits
This project is based on the template provided using [GitHub-Auto-Follow](https://github.com/ZigaoWang/github-auto-follow/blob/master/main.py).

I have made modifications and improvements to suit the needs of my specific use case. Please refer to the original repository for further details.


