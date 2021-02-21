# WhatSoup 🍲
A web scraper that exports your entire WhatsApp chat history.

## Overview
### Problem
1) Exports are limited up to a maximum of 40,000 messages
2) Exports skip the text portion of media-messages by replacing the entire message with ```<Media omitted>``` instead of for example ```<Media omitted> My favorite selfie of us 😻🐶🤳```
3) Exports are limited to a ```.txt``` file format

### Solution
*WhatSoup* solves these problems by loading the entire chat history in a browser, scraping the chat messages (only text, no media), and exporting it to ```.txt```, ```.csv```, or ```.html``` file formats.

**Example output**: 

*WhatsApp Chat with Bob Ross.txt*
```
02/14/2021, 02:04 PM - Eddy Harrington: Hey Bob 👋 Let's move to Signal!
02/14/2021, 02:05 PM - Bob Ross: You can do anything you want. This is your world.
02/15/2021, 08:30 AM - Eddy Harrington: So I'm thinking of making a tool to help us backup our cherished chats, called WhatSoup 🍲 Thoughts?
02/15/2021, 08:30 AM - Bob Ross: However you think it should be, that’s exactly how it should be.
02/15/2021, 08:31 AM - Eddy Harrington: You're the best, Bob ❤
02/19/2021, 11:24 AM - Bob Ross: <Media omitted> My latest happy 🌲 painting for you.
```
## Demo
[![Watch the video on YouTube](https://raw.githubusercontent.com/eddyharrington/WhatSoup/master/docs/demo.gif)](https://www.youtube.com/watch?v=F3lNYk8pPeQ)

## Prerequisites
1) You have a WhatsApp account
2) You have Chrome browser installed
3) You have some familiarity with setting up and running Python scripts
4) Your terminal supports unicode (UTF-8) characters (for chat emoji's)

## Instructions
1) Clone the repo:
    ```
    git clone https://github.com/eddyharrington/WhatSoup.git
    ```
2) Create a virtual environment:
    ```
    # Windows
    python -m venv env

    # Linux
    python3 -m venv env

    # Mac
    TODO
    ```
3) Activate the virtual environment:
    ```
    # Windows
    env/Scripts/activate

    # Linux
    source env/bin/activate

    # Mac
    TODO
    ```
4) Install the dependencies:
    ```
    pip install -r requirements.txt
    ```
5) Setup your environment
- Download [ChromeDriver](https://chromedriver.chromium.org/downloads) and extract it to a local folder (such as the ```env``` folder)
- Get your Chrome browser ```Profile Path``` by opening Chrome and entering ```chrome://version``` into the URL bar
- Create an ```.env``` file with an entry for ```DRIVER_PATH``` and ```CHROME_PROFILE``` that specify the directory paths for your ChromeDriver and your Chrome Profile:
    ```
    # .env file contents
    DRIVER_PATH = 'C:\path-to-your-driver\chromedriver.exe'
    CHROME_PROFILE = 'C:\Users\your-username\AppData\Local\Google\Chrome\User Data'
    ```
5) Run the script
    ```
    # Windows
    python whatsoup.py

    # Linux
    python3 whatsoup.py

    # Mac
    TODO
    ```

## Contributing
TODO