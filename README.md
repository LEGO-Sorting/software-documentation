# Software for LEGO Sorting Machine

The software has been created in REST Architecture using following microservices:

- Mobile App - capture video real LEGO bricks. Written in React Native and deployed using Expo [Download](https://expo.io/@maskam/projects/lego-mobile-client). [Source Code](https://github.com/LEGO-Sorting/lego-mobile-client)
- API - receiving videos in mp4 format. Technology used: .NET Core 5.0 [Source Code](https://github.com/LEGO-Sorting/Lego.Server)
- Recognition Service - Microservice Written in Python 3.8 which is responsible for LEGO parts recognition and send it to client [Source Code](https://github.com/LEGO-Sorting/lego-mobile-client).

## Requirements
- [Expo](https://expo.io/) installed on PC and device
- Python 3.8
- Python libraries from requirements.txt in [recognition service](https://github.com/LEGO-Sorting/lego-mobile-client)
- .NET Core 5
- Android Device
- Ngrok [download](https://ngrok.com/download)
- Anaconda (recommended)

## Mobile App

The mobile app has been created only for android users. No possibillity to run it on iOS at the moment.

### Install

#### local

If you are interested in build app locally you will have installed:
- `expo-cli`
- `expo`
- `npm` or `yarn` (recommended)
- Expo app installed on your android device

1. Use `expo install` command to install or update libraries
2. Use `expo start` command to run app locally
3. Scan QR code using expo app on your mobile device (remember to have allowed port displayed in terminal)
4. Setup api URL to API from [ngrok](https://ngrok.com/download)

#### Deployed

1. Download Expo app from Google store
2. Scan [QR code](https://expo.io/@maskam/projects/lego-mobile-client) from downloaded earlier app
3. Setup api URL to API from [ngrok](https://ngrok.com/download)
