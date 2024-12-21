### Qixelon Firmware Tools

Simple .img firmware flasher for ESP32-C6 based Qixelon 3D printers.

*only for Linux (TM)*

### How to Install
Script uses [pipx](https://command-not-found.com/pipx). Install it before use.

```bash
pipx install ampy
pipx ensurepath
git clone https://github.com/qixelon/qixelon-tools
cd qixelon-tools
chmod +x qx-*
cp qx-* ~/.local/bin
```

### How to Use

- **`qx-tools`**: Displays help and available commands.
  
- **`qx-flash <img> <config> <device>`**: Flash firmware image to a Qixelon printer.
  - `<img>`: Path to the `.img` firmware file.
  - `<config>`: Path to the printer's config file.
  - `<device>`: Path to the connected device (e.g., `/dev/ttyUSB0`).

- **`qx-backup <device>`**: Creates a backup of the printer's `/data`, `.env`, and `HISTORY` files.
  - `<device>`: Path to the connected device.

- **`qx-history <device>`**: Retrieve printer statistics from the `HISTORY` file.
  - `<device>`: Path to the connected device.

- **`qx-erase <device>`**: Erase the `/data` folder from the Qixelon printer.
  - `<device>`: Path to the connected device.
