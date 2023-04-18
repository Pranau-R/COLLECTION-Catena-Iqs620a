# COLLECTION-Catena-Iqs620a

This repo is intended to be built on Linux (Ubuntu 18 or later). The build script might work with Ubuntu for Windows, but has not been tested.

To build:

1. Clone this repository:

    ```bash
    git clone --recursive git@gitlab-x.mcci.com:client/woodfern/wakefield/sketches/COLLECTION-Catena-Iqs620a.git
    ```

2. If building with a project secure key, get a copy of that key and put it someplace handy; please make sure it's password protected, at least.

3. Build with the following commands:

    - to build with the test-signing key:

      ```bash
      ./build-with-cli --test
      ```

    - to build with a project-specific key:

      ```bash
      ./build-with-cli --key={path-to-file}.pem
      ```

    - to build for 2 MHz clock and hardware serial, for Europe, with the test-signing key:

      ```bash
      ./build-with-cli.sh --clock=2 --serial=hw --region=eu868 --test
      ```

    - to build for multiple regions and multiple networks:

      ```bash
      ./build-with-cli.sh --test --verbose && ./build-with-cli.sh --test --verbose --region=au915 --network=ttn && ./build-with-cli.sh --test --verbose --region=eu868 --network=ttn
      ```

   The output shows up in `{slug}/build/ide`.
