# Simple Timer Daemon (STD)

A lightweight and configurable timer daemon that helps you manage work and break periods. STD is designed to run as a background service and is perfect for study sessions, coding sprints, or any focused work that benefits from structured breaks.

## Features

- Configurable work/break periods
- Audio notifications when periods end
- Clean countdown display
- Automatic transitions between work and break periods
- Simple config file in TOML format

## Requirements

- Python 3.12+
- mpg123 (for audio notifications)
- Required Python packages:
  - click>=8.1.7
  - tomllib (included in Python 3.11+)

## Installation

1. Clone this repository:
```bash
git clone https://github.com/yourusername/std.git
cd std
```

2. Create and activate a virtual environment:
```bash
python -m venv env
source env/bin/activate  # On Windows use: env\Scripts\activate
```

3. Install requirements:
```bash
pip install -r requirements.txt
```

4. Install mpg123 for your system:
- Ubuntu/Debian: `sudo apt install mpg123`
- macOS: `brew install mpg123`
- Windows: Download from the official mpg123 website

## Usage

Start a study/work session:
```bash
python std.py start
```

## Configuration

On first run, you can choose to create a default configuration file Ghich will be created at `~/.config/std/config.toml` with these settings:

```toml
work_period = 90    # Work period in minutes
break_period = 20   # Break period in minutes
sound_file = "/path/to/sound.mp3"  # Notification sound
```

Edit these values to match your preferred study/break schedule.

## Current Status

This is version 0.1.0, an MVP release. Core functionality is working, but some features are still in development:

- ✅ Basic timer functionality
- ✅ Work/break cycles
- ✅ Audio notifications
- ❌ Pause/resume (coming soon)
- ❌ Session statistics (planned)
- ❌ Status command (planned)

## Contributing

This is a personal project in active development. Feel free to open issues for bugs or feature suggestions!

## License

This project is licensed under the WTFPL License - see the [LICENSE](LICENSE) file for details.
