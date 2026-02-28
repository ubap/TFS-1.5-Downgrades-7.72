# Nekiro's 7.72 Downgrade Updated to 2023 to compile with vcpkg and latest FMT libraries 

This downgrade is a download and run distribution, monsters and spells are probably not 100% correct.
You are welcome to submit a pull request though.

This downgrade is up to Dec 21, 2021, commit: https://github.com/otland/forgottenserver/commit/17bf638815fa7c04d5b723baa8e0bfbdaad341f2

## Other distributions:
## How to compile

`docker build -t tfs-builder .`

# How to debug in Clion

`docker build -t tfs-dev -f Dockerfile.dev .`

Step 2: Configure Toolchain in CLion
Now, we will configure CLion to use the Docker container as the development environment instead of your local system.

Open Settings (Cmd + ,) -> Build, Execution, Deployment -> Toolchains.

Click the + icon and select Docker.

In the Server field, ensure Docker is selected. For the Image, choose tfs-dev:latest.

Wait a moment for CLion to detect the tools (C++ compiler, CMake, and GDB). Success indicators should appear next to each item once detected.

Step 3: CMake Settings
Finally, assign the Docker Toolchain to your project to enable building and debugging:

Go to Settings -> Build, Execution, Deployment -> CMake.

In the Toolchain field, select your newly created Docker profile.


Click OK. CLion will now reload the project. You can now build or debug by clicking the Build (Hammer) or Debug (Bug) icons.

## Start DB

`docker-compose up -d`

## Contributing
