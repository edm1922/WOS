# WOS Discord Bot

A comprehensive Discord bot for Whiteout Survival game management, featuring alliance management, gift code distribution, user tracking, and automated operations.

## Features

- **Alliance Management**: Create and manage alliances with member operations
- **Gift Code System**: Distribute and track gift codes for users
- **User Tracking**: Monitor user progress, furnace levels, and nickname changes
- **Automated Operations**: Backup operations, bear trap management, and logging systems
- **Auto-update System**: Automatic file updates from GitHub and alternative sources
- **Database Management**: SQLite-based data storage with automatic table creation

## Requirements

- Python 3.7+
- Discord.py
- Required packages (automatically installed on first run):
  - discord.py
  - colorama
  - requests
  - aiohttp
  - python-dotenv
  - aiohttp-socks
  - pytz
  - pyzipper

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/edm1922/WOS.git
   cd WOS
   ```

2. Run the bot:
   ```bash
   python main.py
   ```

3. On first run, the bot will:
   - Install required dependencies automatically
   - Prompt for your Discord bot token
   - Create necessary database files and folders
   - Check for updates

## Configuration

### Bot Token
- Create a Discord application and bot at [Discord Developer Portal](https://discord.com/developers/applications)
- Copy your bot token
- The bot will prompt for the token on first run and save it to `bot_token.txt`

### Database
The bot automatically creates SQLite databases in the `db/` folder:
- `alliance.sqlite` - Alliance and member data
- `giftcode.sqlite` - Gift code management
- `changes.sqlite` - User change tracking
- `users.sqlite` - User information
- `settings.sqlite` - Bot settings and versions

## Usage

The bot uses slash commands (`/`) for interaction. Available commands depend on the loaded cogs:

- **Alliance Commands**: Manage alliances and members
- **Gift Code Commands**: Distribute and track gift codes
- **User Commands**: View user information and progress
- **Admin Commands**: Bot management and settings

## Auto-Update System

The bot includes an automatic update system that:
- Checks for updates from GitHub and alternative sources
- Downloads and applies file updates
- Restarts automatically when main.py is updated
- Maintains version tracking in the database

## Project Structure

```
WOS/
├── main.py                 # Main bot file with auto-update system
├── cogs/                  # Bot command modules
│   ├── alliance.py        # Alliance management
│   ├── gift_operations.py # Gift code system
│   ├── bot_operations.py  # Bot management
│   └── ...               # Additional modules
├── db/                    # Database files
├── log/                   # Log files
└── startmain.bat         # Windows startup script
```

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Support

For support and questions, please open an issue on GitHub or contact the development team.

## Disclaimer

This bot is designed for educational and entertainment purposes. Please ensure compliance with Discord's Terms of Service and your server's rules when using this bot. 