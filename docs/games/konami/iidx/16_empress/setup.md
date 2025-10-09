<img class="header-logo" src="/img/konami/iidx/16_empress/logo.webp">
# Game Setup

--8<-- "docs/snippets/common/data_warning.md"

## Preparing data

--8<-- "docs/snippets/common/data_readonly.md"

    The **complete game data** should be approximately **26 GB or larger**.  
    If your data is significantly smaller, you likely have an update archive instead of the full game data.

    Here's what the expected data structure should look like: 

    ```
    📂yyyymmddrr (revision folder, y = year digit, m = month digit, d = day digit, r = revision digit)
    📂data
    📄sidcode.txt
    ```

## Installing Bemanitools

!!! tip ""

    - Download the latest Bemanitools release zip [here](https://github.com/djhackersdev/bemanitools/releases/latest)

    - Inside `bemanitools-x.xx.zip` locate `iidx-14-to-17.zip`

    - Extract all files from `iidx-14-to-17.zip` into your revision folder (yyyymmddrr)
        - (Hint: you only need one of the `gamestart-**.bat` and `iidxhook-**.bat` files, specific to your game version number)
    
--8<-- "docs/snippets/konami/iidx/btools_d3d8to9.md"

--8<-- "docs/snippets/konami/iidx/clvsd.md"

!!! tip ""

    - After all this, here's what the expected data structure should look like:
    ``` hl_lines="2 3 4 7 8 10 11 12 13 14 18 19"
    📄bm2dx.exe
    📄config.bat
    📄config.exe
    📄d3d8.dll
    📄d3dx9_24.dll
    📄dbghelp.dll
    📄eamio.dll
    📄gamestart-16.bat
    📄gcidata.nsd
    📄geninput.dll
    📄iidxhook3.dll
    📄iidxhook-16.conf
    📄iidxio.dll
    📄inject.exe
    📄libacio.dll
    📄libavs-win32.dll
    📄libavs-win32-ea3.dll
    📄vefx.txt
    📄vefxio.dll
    ```

## Configuring Bemanitools

!!! info "Open the `config.bat` file. The following tabs correspond to the ones in the configuration window."

=== "Buttons"

--8<-- "docs/snippets/konami/iidx/btools_buttons.md"

--8<-- "docs/snippets/konami/common/spicecfg_buttons_additionalinfo.md"

=== "Lights"

--8<-- "docs/snippets/konami/common/btools_lights.md"

=== "Analogs"

--8<-- "docs/snippets/konami/iidx/btools_analogs.md"

=== "Network"
    
--8<-- "docs/snippets/konami/common/btools_cards.md"

## Connecting to a network

--8<-- "docs/snippets/konami/iidx/btools_connecting_network.md"

## Game resolution and locking FPS

!!! tip ""
    We'd like to mention that there are two options when it comes to how the game renders. You can choose between `Linear` and `Point`.

    Below is an example of how both look like.

    ??? info "Linear"
        <img src="/img/konami/iidx/14_gold/iidx14_linear.webp">

    ??? info "Point"
        <img src="/img/konami/iidx/14_gold/iidx14_point.webp">
        
    It comes down to your own prefrence what you decide on, `Linear` is less sharp but doesn't have pixel perfect edges. `Point` is sharp and is pixel perfect.

--8<-- "docs/snippets/konami/iidx/btools_resolution_fps.md"

## Before playing

--8<-- "docs/snippets/common/before_playing.md"

## First launch

!!! tip ""

    If you've followed all instructions correctly, you're now finally ready to launch the game!

    **First plug your controller if you have one** and run `gamestart.bat` **as Administrator**.

    If it's your first time running the game, you'll soon be greeted with this screen.

    <img src="/img/konami/iidx/14_gold/firstlaunch/2.webp">
    
    Press your `Test` key to initialize the backup data, a message will pop up stating it's been initialized.

    !!! warning ""
        If right here you get `USB I/O ERROR ERROR(FM TRNS-OUT)` or `USB I/O ERROR ERROR(FM-DL TIMEOUT)` instead of the `BACKUP DATA ERROR`, reboot the game and it should get fixed.
    
    Next, you'll get another error.
    
    <img src="/img/konami/iidx/14_gold/firstlaunch/3.webp">

    Press your `Test` key again and let the game run for a bit until the monitor check is complete.

    You will now be taken to the service menu.

    <img src="/img/konami/iidx/14_gold/firstlaunch/5.webp">

    Instructions on how to navigate the menu are shown at the bottom of the screen:

    - Press `1` and `2` to go up and down
    - Press `6` to select/execute
  
    Start by going up to `CLOCK`.

    <img src="/img/konami/iidx/14_gold/firstlaunch/6.webp">

    Here, simply select `SAVE AND EXIT` and the clock will be set.

    You'll be back in the service menu.

    Go to `NETWORK OPTIONS` then `e-AMUSEMENT SETTINGS`.

    <img src="/img/konami/iidx/14_gold/firstlaunch/9.webp">
    <img src="/img/konami/iidx/14_gold/firstlaunch/10.webp">

    You will need to set a shop name.
    
    - Name your shop to whatever you'd like. Again, navigation instructions are at the bottom of the screen
    - Go to `EXIT` then `SAVE AND EXIT`

    Select `GAME OPTIONS`.
    
    <img src="/img/konami/iidx/16_empress/11.webp">
    Here, you need to select a display type.
    !!! tip "This setting affects timing offset in the song."
    - For lower offset, select `TYPE B`. If your monitor has high latency, select `TYPE A`. If you're not sure what to pick, remember that you can always change this setting later depending on how the game feels
    - Go to `SAVE AND EXIT`

    Select `GAME MODE`.
    
!!! success "You're all done! The game should load up properly now. Make sure to insert credits by pressing your `SERVICE` key!"

## Help

--8<-- "docs/snippets/common/help.md"