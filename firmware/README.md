
## Build

### Fetch Dependencies

```bash
python3 ./fetch_repos.py
```

### Tool Chains

[ESP-IDF v5.5.4](https://docs.espressif.com/projects/esp-idf/en/v5.5.4/esp32s3/index.html)

### Build

```bash
idf.py build
```

### Flash

```bash
idf.py flash
```

## Troubleshooting

### ESP-IDF version

*StackChan Firmware v1.2.4* can be built using only ESP-IDF v5.5.4. Although the ESP-IDF installer recommends installing ESP-IDF v6.0.0, you need to actually install the v5.5.4.

### Build target device

*StackChan firmware* is designed for the ESP32S3. If you encounter an error related to `bootloader_check_size`, please verify the target device for the build.

For instance, you can set the target with:

```bash
idf.py set-target esp32s3   
```

### ESP-IDF Version selection in VSCode Extension

If you are using ESP-IDF via the VSCode Extension and cannot find `idf.py`, the version of ESP-IDF recognized by the extension may be incorrect.
You need to set the current ESP-IDF version in the VSCode IDE.

> In Visual Studio Code, navigate to View > Command Palette and type select current esp-idf version and select ESP-IDF: Select Current ESP-IDF Version from the list. by [ESP-IDF Extension for VS Code](https://github.com/espressif/vscode-esp-idf-extension/blob/master/README.md)
