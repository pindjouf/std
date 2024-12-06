# Simple Timer Daemon (STD)

A lightweight and configurable timer daemon that helps you manage work and break periods. STD is designed to run as a background service and can be easily controlled through a command-line interface.

## Features

- Customizable work and break periods via a config file.
- Plays a sound to signal transitions between work and break.
- Runs as a daemon with systemd or standalone.
- Easy CLI interaction for starting, stopping, and configuring the timer.

---

## Installation

### Prerequisites

- Python 3.8+
- Linux with systemd (optional for running as a service)

### Clone the Repository

```bash
git clone https://github.com/yourusername/std.git
cd std
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Configure the Timer

Edit the `config.toml` file to set your desired work and break periods and the path to the sound file:

```toml
work_period = 25
break_period = 5
sound_file = "/absolute/path/to/sound.wav"
```

---

## Usage

### Running Without Systemd

Run the daemon manually:

```bash
python main.py
```

### Running With Systemd

1. Copy the provided systemd service file to your user systemd directory:

   ```bash
   cp std.service ~/.config/systemd/user/
   ```

2. Enable and start the service:

   ```bash
   systemctl --user enable std
   systemctl --user start std
   ```

### CLI Commands

- Start a work period:

  ```bash
  std start
  ```

- Stop the timer:

  ```bash
  std stop
  ```

- Check status:

  ```bash
  std status
  ```

---

## Contributing

Contributions are welcome! Please fork the repository and create a pull request.

## License

This project is licensed under the WTFPL License - see the [LICENSE](LICENSE) file for details.
