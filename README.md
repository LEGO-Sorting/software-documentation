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

1. Clone [Source Code](https://github.com/LEGO-Sorting/lego-mobile-client)
2. Use `expo install` command to install or update libraries
3. Use `expo start` command to run app locally
4. Scan QR code using expo app on your mobile device (remember to have allowed port displayed in terminal)
5. Setup api URL to API from [ngrok](https://ngrok.com/download)

#### Deployed

1. Download Expo app from Google store
2. Scan [QR code](https://expo.io/@maskam/projects/lego-mobile-client) from downloaded earlier app
3. Setup api URL to API from [ngrok](https://ngrok.com/download)


## API

The API has been written in .NET Core 5. The aim of that microservice is receive recorded videos and split it into frames and send them into recognition service. 

### Requirements

- Installed .NET Core 5 SDK
- Installed .NET Core Runtime
- Installed FMPEG library. For Windows you can get it from [gyan.dev](https://www.gyan.dev/ffmpeg/builds/), you'll have to have dll's
- Downloaded Ngrok

### Install

1. Clone the [Source Code](https://github.com/LEGO-Sorting/Lego.Server)
2. If you are on Windows, setup path to FMPEG library in Startup. It is done by changing variable `currentDirectory`. By default it is output directory for `Lego.Server.WebAPI`
2. Run app with environment variable `ASPNETCORE_URLS=http://localhost:5001`
3. Run Ngrok using command `ngrok http 5001`. The URI generated with https protocol will be URI recognized by mobile app


## Recognition Service

The microservice wirtten in Python and Flask for client. Aim of that service is use trained model and display results in web client.

### Required
- Python 3.8
- Anaconda (Recomended)
- PyCharm (Recommended)

### Install

1. Clone the [Source Code](https://github.com/LEGO-Sorting/lego-recognition-service)
2. Use `pip install -r requirements.txt` to install all needed libraries to run app
3. Run app

