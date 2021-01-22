# Amanita
GTK3+ theme based on the Adwaita:
- Focus on content rather than decoration
- Utilitarian and calm
- Easy on eyes

# How to install pre-compiled version?
Download from the "Releases" section; built on Debian Bullseye using `libgtk v3.24.24-1`.

# How to build?
1. Clone GTK from upstream: https://gitlab.gnome.org/GNOME/gtk
2. Checkout tag corresponding to your distribution. To find the version:
    ```
    $ dpkg -l libgtk-3-0
    Desired=Unknown/Install/Remove/Purge/Hold
    | Status=Not/Inst/Conf-files/Unpacked/halF-conf/Half-inst/trig-aWait/Trig-pend
    |/ Err?=(none)/Reinst-required (Status,Err: uppercase=bad)
    ||/ Name             Version      Architecture Description
    +++-================-============-============-====================================
    ii  libgtk-3-0:amd64 3.24.24-1    amd64        GTK graphical user interface library
    ```
3. Replace Adwaita files with ones provided in this repository.
4. Switch Meson to the release build:
    ```yml
    project('gtk+-3.0', 'c',
        version: '3.24.24',
        default_options: [
          'buildtype=release',
          'warning_level=1'
        ],
        meson_version : '>= 0.48.0',
        license: 'LGPLv2.1+')
    ````
4. Compile:
    ```sh
    $ meson _build .
    $ cd _build
    $ ninja
    ```

# Screenshots

![image](https://user-images.githubusercontent.com/300146/105485759-4b048200-5cfd-11eb-8159-065ab54998bd.png)

![image](https://user-images.githubusercontent.com/300146/105485820-61124280-5cfd-11eb-9ab2-637729f475b4.png)

![image](https://user-images.githubusercontent.com/300146/105485828-653e6000-5cfd-11eb-907c-020a0c5d6d5e.png)

