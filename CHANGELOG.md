# Changelog

## v0.2.23

* Updates
  * Several networking notebook additions and improvements. Thanks to Jon
    Carstens for these.
  * Pull in a subtle mDNS/DNS issue lookup issue that affected using .local
    addresses on some networks
  * Pull in Bluetooth support fixes. BLE works on Raspberry Pi Zeros and
    Raspberry Pi 3s now, but it's not convenient and there aren't any sample
    notebooks. We hope to change that soon.
  * You can transfer files using `scp` in addition to `sftp` from Nerves
    Livebook devices now.

## v0.2.22

* Updates
  * Upgrade to `nerves_system_br` `1.17.0`-based systems. These include Erlang
    24.1 and Buildroot 2021.08.

## v0.2.21

* Updates
  * Update all URLs to point to the `nerves_livebook` home on the `livebook-dev`
    GitHub repository

## v0.2.20

* Updates
  * The Raspberry Pi 4 USB-C port can now be used for power and data. This is
    similar to the Raspberry Pi Zero, 3A and BBB.
  * Minor updates to a variety of packages

## v0.2.19

* Updates
  * Use new Nerves MOTD for ssh logins

## v0.2.18

* Updates
  * Livebook 0.2.3
  * Update to MdnsLite 0.8.0 and enable support for using mDNS (.local)
    addresses with Erlang distribution and more
  * Update various other Nerves dependencies

## v0.2.17

* Updates
  * Make Erlang distribution predictable. It's now
    `livebook@nerves-<device id>.local`. From within Livebook, you can see the
    name by going to the settings tab. This is an mDNS name and will work even
    if the IP address to the device changes. It only requires an mDNS client on
    your computer which is included by default on MacOS and usually on Linux.

## v0.2.16

* Updates
  * Support provisioning WiFi when creating the MicroSD card. See `README.md`
    for how to pass parameters when calling `fwup`.
  * Check that dependencies passed to `Mix.install/1` are compatible with what's
    included in Nerves Livebook. Installation isn't supported yet, but this
    update makes it possible to include `Mix.install/1` calls in your livebooks
    for when it does work.

## v0.2.15

* Updates
  * Minor version bumps on many dependencies - no new features

## v0.2.14

* Updates
  * Update to OTP 24-based Nerves systems
  * Livebook 0.2.2

## v0.2.13

* Updates
  * Update Livebook to 0.1.2
  * The `vega_lite` and `kino` packages are available so it's now possible to
    experiment with plotting sensor data. Note that `Mix.install` doesn't work
    yet so if you're trying out a notebook that uses `vega_lite`, just uncomment
    the `Mix.install` parts for now.

## v0.2.12

* Updates
  * Organize sample livebooks into directories so that they're easier to find.
    More changes are coming. Thanks to DJ Carpenter for spearheading the effort
    better organize this project.
  * Add a delta firmware update livebook. This livebook can't be used just yet.
    It needs a release to update to. Once v0.2.13 is available, it will work.

## v0.2.11

* Updates
  * Add NervesKey (ATECC508A/608) provisioning example. Thanks to Alex McLain
    for contributing this.
  * Building delta firmware updates on CI. This lays the groundwork for future
    livebooks.

## v0.2.10

* Updates
  * Update to Livebook 0.1.1
  * Add PWM example using Pigpiox for Raspberry Pis. Thanks to DJ Carpenter for
    contributing this.

## v0.2.9

* Updates
  * Update to Elixir 1.12.0 and Livebook 0.1.0
  * Various BMP280 Livebook and library updates

## v0.2.8

Community update release!

* Updates
  * Thanks to Jonatan Klosko, upstream Livebook now supports embedded mode so we
    can use it on Nerves without patching it. This release has zero custom
    Livebook patches for Nerves.
  * DJ Carpenter has started reorganizing the samples directory to make it
    easier to find examples. He also added a GPIO button example.
  * Masatoshi Nishiguchi has updates to the BMP280
    temperature/humidity/barometric sensor example too

## v0.2.7

* Updates
  * Add Circuits.GPIO example from DJ Carpenter
  * Add BMP280 example from Masatoshi Nishiguchi

## v0.2.6

* Updates
  * Use Elixir 1.12.0-rc.1. This enables some Livebook features that I haven't
    tested yet, but look cool.
  * Update Livebook to the latest to pull in user profiles

## v0.2.5

* Updates
  * Verify firmware signatures in `firmware_update.livemd`

## v0.2.4

* Updates
  * Start signing firmware updates and add info on how. This doesn't check
    firmware signatures yet. That will be the next release.

## v0.2.3

* Updates
  * Minor firmware update livebook improvements

## v0.2.2

* Updates
  * Add welcome
  * Update Livebook to latest

## v0.2.1

* Bug fixes
  * Clean up /data/livebooks. This may be worth a complete re-flash to clean up
    the MicroSD card.

* Updates
  * Update Livebook to try import feature

## v0.2.0

This release no longer copies the built-in Livebooks to the data partition.
They're no symlinked so that they remain read-only and update on firmware
updates. You now have to fork them to run them.

* New features
  * A firmware update example

## v0.1.1

Initial CI-built release

## v0.1.0

Initial release
