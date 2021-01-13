# Amanita
Fork of the Adwaita with a few tweaks to make it less harsh on eyes.

# How to build?
1. Clone GTK from upstream: https://gitlab.gnome.org/GNOME/gtk
2. Checkout tag corresponding to your distribution. To find the version:
    ```
    dpkg -l libgtk-3-0
    Desired=Unknown/Install/Remove/Purge/Hold
    | Status=Not/Inst/Conf-files/Unpacked/halF-conf/Half-inst/trig-aWait/Trig-pend
    |/ Err?=(none)/Reinst-required (Status,Err: uppercase=bad)
    ||/ Name             Version      Architecture Description
    +++-================-============-============-====================================
    ii  libgtk-3-0:amd64 3.24.24-1    amd64        GTK graphical user interface library
    ```
3. Replace Adwaita files with ones provided in this repository.
4. Compile:
    ```sh
    $ meson _build .
    $ cd _build
    $ ninja
    ```
5. Alternatively &mdash; download compiled .CSS files from the "Releases" section. These are built on Debian Bullseye using v3.24.24.
