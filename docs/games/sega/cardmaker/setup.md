<img class="header-logo" src="/img/sega/cardmaker/logo.webp">
# Game Setup

--8<-- "docs/snippets/common/data_warning.md"

--8<-- "docs/snippets/sega/common/data_old.md"

!!! info "Info"

    The setup process should be mostly the same regardless of the game version. However, some things may change, so proceed with caution. Feel free to ask for help on our Discord server!

## Preparing data

--8<-- "docs/snippets/sega/common/data_driveletter.md"

--8<-- "docs/snippets/common/data_readonly.md"

--8<-- "docs/snippets/sega/common/data_preparation.md"

    ```
    📂license
    📂package
    📄firewall.cfg
    ▶️game.bat
    ▶️pxGetHwinfo.exe
    📝pxGetHwInfo.ini
    ▶️RotateDisplay.exe
    📄system_config.json
    ```

--8<-- "docs/snippets/sega/common/data_bad.md"

## Installing unprotected executables

!!! tip ""

    Card Maker executables are protected and will not run on a regular computer.

    - Obtain unprotected (also called "unpacked" or "decrypted" by the community) copies of of the following folders and files:

    ```
    ▶️amdaemon.exe
    ▶️CardMaker.exe
    📂CardMaker_Data
    ┣━📂Plugins
    ┃  ┣━⚙️amdaemon_api.dll
    ┃  ┣━⚙️chiffre.dll
    ┃  ┣━⚙️libhttp.dll
    ┃  ┣━⚙️PrintDLL.dll
    ┃  ┗━⚙️QR_Image.dll
    ┗━📂Managed
       ┣━⚙️AMDaemon.NET.dll
       ┗━⚙️Assembly-CSharp.dll
    ```

    - Copy all of the above to your data's `App\package` folder
    - Agree to overwrite when asked

!!! warning "Assembly-CSharp Notes"

    `Assembly-CSharp.dll` **must** match your game version.  
    All other files can be reused between game versions.

## Installing ICFs

--8<-- "docs/snippets/sega/common/data_icfs.md"

## Installing segatools

--8<-- "docs/snippets/sega/common/segatools_install.md"
    - Find `cm.zip` and extract it to your data's `App\package` folder

    You should now have these files added to your `App\package` directory:

    ```
    📂DEVICE
    ⚙️cmhook.dll
    📄config_hook.json
    ▶️inject.exe
    📝segatools.ini
    ▶️start.bat
    ```

## Configuring segatools

--8<-- "docs/snippets/sega/common/segatools_preamble_package.md"

=== "[vfs]"

--8<-- "docs/snippets/sega/common/segatools_relativepaths.md"

--8<-- "docs/snippets/sega/common/segatools_vfs.md"

## Configuring audio

--8<-- "docs/snippets/common/audio_48khz.md"

## Connecting to a network

--8<-- "docs/snippets/sega/common/network_preamble.md"

--8<-- "docs/snippets/sega/common/network_remote.md"

--8<-- "docs/snippets/sega/common/network_local.md"

## Installing VCRedist & DirectX

--8<-- "docs/snippets/common/setup_vcredist_directx.md"

## Before playing

--8<-- "docs/snippets/common/before_playing.md"

## First launch

!!! tip ""

    If you've followed all instructions correctly, you're now finally ready to launch the game!

    Start the game by running `App\package\start.bat`.

    Press your `Test` button (default `F1`) to enter the service menu. Use the arrow buttons on the screen to navigate the menu, and the `決定` button to select an option.

    Navigate to **閉店設定** (`CLOSE SETTING`, the 11th option).

    <img src="/img/sega/cardmaker/setup/close_setting.webp">

    Navigate to **時** (`HOUR`, the 2nd option) and use the `決定` button to toggle the setting until it says **全時刻** (`ALL TIME`).

    <img src="/img/sega/cardmaker/setup/all_time.webp">

    Select **終了** (`EXIT`, the last option) to exit to the main service menu, then select **終了** (also the last option) in the main menu to exit the service menu.

--8<-- "docs/snippets/sega/common/success.md"

!!! info "By default, "printed" cards will be saved in the `App\package\DEVICE\print` folder"

## Help

--8<-- "docs/snippets/common/help.md"
