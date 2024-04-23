# Streaming Video with RTSP and RTP

## Programming Task 
In this task, you will implement a streaming video server and client that communicate using the Real-Time Streaming Protocol (RTSP) and send data using the Real-time Transfer Protocol (RTP). Your task is to implement the RTSP protocol in the client and implement the RTP packetization in the server.

We will provide you with source codes that implement the RTSP protocol in the server, the RTP de-packetization in the client, and takes care of displaying the transmitted video.

## Classes / Methods

### Client, ClientLauncher
The ClientLauncher starts the Client and the user interface which you use to send RTSP commands and which is used to display the video. In the Client class, you will need to implement the actions that are taken when the buttons are pressed. You do not need to modify the ClientLauncher module.

### Server, ServerWorker
These two modules implement the server which responds to the RTSP requests and streams back the video. The RTSP interaction is already implemented and the ServerWorker calls methods from the RtpPacket class to packetize the video data. You do not need to modify these modules.

### RtpPacket
This class is used to handle the RTP packets. It has separate methods for handling the received packets at the client side and you do not need to modify them. The Client also de-packetizes (decodes) the data and you do not need to modify this method. You will need to complete the implementation of video data RTPpacketization (which is used by the server).

### VideoStream
This class is used to read video data from the file on disk. You do not need to modify this class.

## Running the program

Setup Python virtual environment.
```
python -m venv .
```

Change the source to the virtual environment
```
Scripts\activate
```

Install required Python libraries
```
pip install -r requirements.txt
```

Run the program
```
run.bat
```