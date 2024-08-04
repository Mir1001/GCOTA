# Flash ESP32 with initial firmware (test)

- Install [esptool](https://github.com/espressif/esptool) or mac `brew install esptool`
- Download bin files from this repro
- Run cmd comman one line (replace YOURPATH), select correct com port (currenty selected "COM8")

```cmd
esptool.py  --chip esp32 --port "/dev/cu.usbserial-210" --baud 1000000 --before default_reset --after hard_reset write_flash -z --flash_mode dio --flash_freq 80m --flash_size 8MB 0x1000 bootloader.bin 0x8000 partitions.bin 0xe000 boot_app0.bin 0x10000 fw.bin
```

# Install Android app

- Remove/uninstall the old version (if exists)
- Download latest [apk](https://github.com/Mir1001/GCOTA/raw/main/app-release.apk)
- In some browse files app, click on downloaded file. The install will start. Alow permisions. This is an unofficial version.

# Windows command

```cmd
"c:\YOURPATH\python.exe" "YOURPATH\esptool.py" --chip esp32 --port "COM8" --baud 1000000 --before default_reset --after hard_reset write_flash -z --flash_mode dio --flash_freq 80m --flash_size 8MB 0x1000 bootloader.bin 0x8000 partitions.bin 0xe000 boot_app0.bin 0x10000 fw.bin
```
