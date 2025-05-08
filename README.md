#EDUCATIONAL PURPOSES ONLY

# Telegram Group Manager

A Python script for managing Telegram groups using the Telethon library. Perform member management tasks like exporting group members to CSV, adding members from CSV files, and viewing CSV contents.

## Features

- **Export Group Members**: List all members of a Telegram group/channel and save to CSV
- **Add Members from CSV**: Bulk add users to a group from a CSV file 
- **CSV Viewer**: Quickly display contents of member CSV files
- **Safe Interval Handling**: Built-in delays to help avoid Telegram flood limits
- **Multiple Auth Methods**: Supports adding users by username or Telegram ID

## Prerequisites

- Python 3.7+
- [Telethon](https://docs.telethon.dev/) library
- Telegram API ID and Hash (from [my.telegram.org](https://my.telegram.org))
- Active Telegram account with phone number

## Installation

1. Clone repository:

git clone https://github.com/yourusername/telegram-group-manager.git
cd telegram-group-manager

2.Install dependencies

pip install telethon csv


## Configure credentials:

api_id = YOUR_API_ID
api_hash = 'YOUR_API_HASH'
phone = '+YOUR_PHONE_NUMBER'



## Usage

1. Export Group Members to CSV

python3 telegram_manager.py
Choose option 1 and select a group from the list. Members will be saved to members-[groupname].csv.

2. Add Members from CSV

python3 telegram_manager.py members.csv
Choose option 2 and select:

Target group

Add method (username or ID)
CSV format required:

username,user_id,access_hash

user1,12345678,1234567890123456789

3. View CSV Contents

python3 telegram_manager.py members.csv
Choose option 3 to display CSV file contents in terminal

CSV Format
Sample CSV structure for adding members:

csv
username,user_id,access_hash
sample_name,123456789,1234567890123456789
samplename,987654321,9876543210987654321



## Security Notes


🔐 Keep your API credentials private

⚠️ Never share generated CSV files containing user hashes

⏳ Respect Telegram's rate limits read more at("https://limits.tginfo.me/en")

👥 Only add users who have agreed to join groups


## Common Errors

PeerFloodError: Too many requests - wait several hours

UserPrivacyRestrictedError: User has privacy settings enabled

PhoneNumberInvalidError: Verify country code in phone number

SessionPasswordNeededError: 2FA enabled - provide password

## Disclaimer

Use this tool responsibly. The developers are not responsible for:

Account bans due to aggressive API use

Privacy violations or spam complaints

Any misuse of the provided functionality

Always comply with Telegram's Terms of Service and respect user privacy.



