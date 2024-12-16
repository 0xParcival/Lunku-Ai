# Lunku AI Bot </PYTHON/>

## Description

   Lunku AI Bot is used in Discord for Image Generation using Pordia AI'

## Requirmemts

- Docker
- VS code *any IDE can use but should be install in your system*
- WSL(Windows Subsystem For Linux) [Intall WSL](learn.microsoft.com/en-us/windows/wsl/install) *only for Windows users*

## Techstack

   Python

## ✨ Features  

List of Features

- Realtime bot app
- standardized development environment with devcontainers
- Image Gentration AI

## 🚀 Getting Started  

### Create Discord Bot

1. **Enable Discord Developer Mode**

   1. User Settings -> Advanced -> Enable Developer Mode

      <img width="500" alt="image" src="https://github.com/user-attachments/assets/04b8f2c2-02ac-43d6-b159-03ae7dfd94c5" />

2. **Get Discord API** [Dicord](https://discord.com/developers/applications)

   <img width="500" alt="Screenshot 2024-12-10 160136" src="https://github.com/user-attachments/assets/54065f77-d453-4b59-a930-3a3a5dc02d24">

3. **Give Name To APP**

4. **Go To Bot Tab**

   1. Give All Access To Bot

      <img width="500" alt="image" src="https://github.com/user-attachments/assets/7238a786-d8e7-44df-bcb0-e7d04c943990">

   2. Click To Reset Token and Paste in .Env File

      <img width="564" alt="image" src="https://github.com/user-attachments/assets/09ac192e-9a68-43f4-86f6-d094c93d3eb5">

5. **Invite the Bot To Server**
    1. Create a Test Server
       1. Open Discord.
       2. On the left sidebar, click the **"+"** button to create a new server.
       3. Choose **Create My Own** (for personal use).
       4. Give your server a name (e.g., "Test Server") and click **Create**.

    2. Invite the Bot to Your Server

       1. Obtain the bot's invite link (usually provided by the bot’s developer or through a specific URL).
       2. Open the invite link in your browser.
       3. Select the test server you just created from the dropdown list of servers you can add the bot to.
       4. Click **Authorize** and ensure you check the necessary permissions for the bot to function properly (such as sending messages, reading channels, etc.).
       5. Complete any CAPTCHA verification if required.

    3. Using the Bot Commands in Your Test Server
         Once the bot is added to your server, you can use the following commands in any text channel:
         <video width="500" src="https://github.com/user-attachments/assets/8c10153c-9c53-4350-ae75-eb14f637af63">

### Open Using Daytona  

1. **Install Daytona**: Follow the [Daytona installation guide](https://www.daytona.io/docs/installation/installation/)
               *Note: Docker should Installed in your system and widows system for linux (wsl)*

2. **Open Terminal Run Daytona**: *Note This Terminal Session not close until full devoplement completed*

   ```bash
   daytona serve
   ```

3. **Create the Workspace**: *Note any IDE must installed in system my fav is Vscode*
   1. Open another Terminal

      ```bash  
      daytona create https://github.com/0xParcival/Lunku-AI.git
      ```

   2. It will Open automatically in VScode

4. **Add Prodia AI (API KEY) To .Env File**:

   1. Follow the Prodia AI Sign up [Prodia](https://app.prodia.com/login)

   2. Get API

      <img width="500" alt="Screenshot 2024-12-12 232719" src="https://github.com/user-attachments/assets/370e669e-f26a-4ff2-b478-258913a56709" />

   3. Add To The .env file

    ```env
    DISCORD="YOUR_DISCORD_BOT_TOKEN"
    PRODIA="YOUR_PRODIA_API"
    ```

5. **Start the Application in vscode Teminal**:  

   ```bash  
   python main.py
   ```

# Usage
   In The Discord Server That You Invite the Bot And Start The Chat using this command

### Available Commands

   1. **`/help`**  
      Displays a list of available commands and how to use them.

   2. **`/generate`**  
      Generates an image based on the provided text description.  
      Example: `/generate "A futuristic cityscape at sunset"`

   3. **`/upscale`**  
      Upscales an image. Simply upload an image file and use this command to enhance it.  
      Example: `/upscale [image file]`

   4. **`/swapface`**  
      Swaps faces between two uploaded images: one from the source image and one from the target image.  
      Example: `/swapface [source image] [target image]`

   5. **`/transform`**  
      Transforms an image based on a text description.  
      Example: `/transform [upload image file] "Turn the image into a cartoon version"`

## ERROR

### Error 1

   1.AttributeError: 'Bot' object has no attribute 'sync_commands'. Did you mean: 'all_commands'?

   ```python
   Traceback (most recent call last):
     File "/usr/local/lib/python3.13/site-packages/discord/client.py", line 449, in _run_event
        await coro(*args, **kwargs)
      File "/workspaces/Lunku-AI/main.py", line 27, in on_ready
         await bot.sync_commands()
           ^^^^^^^^^^^^^^^^^
   AttributeError: 'Bot' object has no attribute 'sync_commands'. Did you mean: 'all_commands'?
   ```

   1.Solution

   Change The *py-cord* package verson (downgrade/upgrade) (2.6.0/2.6.1) in requirment.txt

   *Default The Py-cord Package version is 2.6.0*

   ```txt
   py-cord=2.6.1
   ```

   Then run This Command:

   ```bash
   pip install -r requirements.txt
   python main.py
   ```
