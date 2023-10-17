# Deepgram Relay POC
<img width="438" alt="Screenshot 2023-10-17 at 7 17 21 AM" src="https://github.com/jongray00/Relay-DeepGram/assets/78746011/381cf288-6f59-47c7-a8c7-8db24e35390c">


## Getting Started

Follow these steps to set up and run the application.
This application demonstrates the use of a relay consumer to answer a call and transcribe the audio using Deepgram.


### Prerequisites

- Node.js and npm (Node Package Manager)
- Deepgram API key
- SignalWire project key and token
- ngrok or websocket tunnel

# Installation

###1. Clone the repository:

   ```
   git clone <repository-url>
   cd deepgram-relay-poc
   ```
   
###2. Create an .env file by renaming env.sample and fill out the required environment variables:
```
SIGNALWIRE_PROJECT_KEY=YOUR_SIGNALWIRE_PROJECT_KEY
SIGNALWIRE_TOKEN=YOUR_SIGNALWIRE_TOKEN
DEEPGRAM_SECRET=YOUR_DEEPGRAM_SECRET
TAP_ADDRESS=ws://<your-ngrok-subdomain>.ngrok.io/asr
PORT=4040
```
Make sure to replace YOUR_SIGNALWIRE_PROJECT_KEY, YOUR_SIGNALWIRE_TOKEN, YOUR_DEEPGRAM_SECRET, and <your-ngrok-subdomain> with your actual credentials and ngrok subdomain.


###3. Install dependencies by running the following command:
```
npm install
```

###4. Run Application
```
npm run start
```
Start the SignalWire client to answer inbound calls and stream audio via 'tap':


###5. Set up your SignalWire number
Use the 'asr' Topic declared with the Relay client. You can add this route in your SignalWire dashboard.
<img width="1265" alt="Screenshot 2023-10-17 at 6 35 13 AM" src="https://github.com/jongray00/Relay-DeepGram/assets/78746011/10f67a59-5b55-4e1a-b22f-2e07582192c1">

Overview
This application sets up a relay consumer to answer inbound calls and transcribe the audio using Deepgram. When a call is received, it answers the call, establishes a WebSocket connection, streams audio for transcription, and prints it to the console.
