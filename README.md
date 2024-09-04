## Features:

* Configuration for the M200 3D printer.
  - It can be restored to its original state even if the user makes arbitrary corrections by mistake.
  - Users comply with the laws and regulations of the country and region in which 3D printers are located (used), comply with work ethics, and pay attention to safety obligations. Users should strictly prohibit the use of our products or equipment for illegal purposes. Moment Co., Ltd. will not be held liable for the legal liability of the violator under any circumstances.
  - Free support is not available if the user arbitrarily changes or modifies the printer.
  - If the manufacturer updates you, you can receive the service remotely.
 
## Requirements:

* You have to define it in moonracker.cfg.
* You will also need to make sure the following is defined in `moonraker.conf`:
  
    ```yaml
    [update_manager M200_configuration]
    type: git_repo
    channel: dev
    path: ~/M200_configuration
    origin: https://github.com/MOMENT3D/M200_configuration.git
    managed_services: klipper
    primary_branch: main

    ```

## Installation:

Moonraker's Update Manager utility. This will allow you to easily install and helps to provide future updates when more features are rolled out!

* `ssh` into your Klipper device and execute the following commands:
   ```bash
    cd
    
    git clone https://github.com/MOMENT3D/M200_configuration.git
    
    ln -s ~/M200_configuration printer_data/config/M200

    ```    
