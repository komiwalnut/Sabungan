# Sabungan-sales
A script that tracks Sabong Saga Genesis NFT sales on Mavis Market and posts real-time updates to the "💰｜sales" channel.

<image src=./images/sample.png/>

# Prerequisites
Ensure you have the following installed on your Linux system:
- Python 3 (Recommended: Python 3.8+)
- pip (Python package manager)
- virtualenv (Install using `pip install virtualenv` if not installed)
- pm2 (Process manager for Node.js, install using `npm install -g pm2`)

# Setting Up the Virtual Environment
1. Open a terminal and navigate to the project directory:
   ```bash
   cd Sabungan-sales
   ```
3. Create a virtual environment named sabungan-venv:
   ```bash
   python3 -m venv sabungan-venv
   ```
5. Activate the virtual environment:
   ```bash
   source sabungan-venv/bin/activate
   ```

# Setting Up Environment Variables
Create a .env file in the project directory and add the following:
```bash
DISCORD_WEBHOOK_URL=your_webhook_url_here
```

# Installing Dependencies
Once the virtual environment is activated, install the required dependencies from requirements.txt:
   ```bash
   pip install -r requirements.txt
   ```

# Running the Application with PM2
1. Ensure pm2 is installed globally:
   ```bash
   npm install -g pm2
   ```
2. Start the application using pm2:
   ```bash
   pm2 start ecosystem.config.js
   ```
3. To check the status of the application:
   ```bash
   pm2 list
   ```
4. To restart the application if needed:
   ```bash
   pm2 restart sabong-saga-genesis-sales-tracker
   ```
5. To stop the application:
    ```bash
   pm2 stop sabong-saga-genesis-sales-tracker
   ```
6. To remove the application from pm2:
   ```bash
   pm2 delete sabong-saga-genesis-sales-tracker
   ```
   
# Keeping PM2 Running After Reboot
To ensure pm2 restarts the application after a system reboot:
   ```bash
   pm2 startup
   pm2 save
   ```
