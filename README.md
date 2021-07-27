# Flash ESP32 with initial firmware (test)
- Install [esptool](https://github.com/espressif/esptool)
- Download bin files from this repro
- Run cmd comman one line (replace YOURPATH), select correct com port (currenty selected "COM8")
```cmd
"c:\YOURPATH\python.exe" "YOURPATH\esptool.py" --chip esp32 --port "COM8" --baud 2000000 --before default_reset --after hard_reset write_flash -z --flash_mode dio --flash_freq 40m --flash_size detect 0x1000 bootloader_dio_40m.bin 0x8000 partitions.bin 0xe000 boot_app0.bin 0x10000 fw.bin
```
