# LiveWave

LiveWave is a real-time streaming application that allows users to capture and stream video content directly to platforms like YouTube Live. Built with Node.js, Express, Socket.IO, and FFmpeg, it provides a simple interface for live broadcasting.

## Features

- Real-time video streaming
- WebRTC-based media capture
- RTMP output compatible with YouTube Live and similar platforms
- Low-latency streaming with optimized FFmpeg settings

## Prerequisites

- Node.js (v18 recommended)
- FFmpeg installed on your system
- A YouTube account with live streaming enabled (for streaming to YouTube)

## Installation

### Local Setup

1. Clone this repository
2. Install dependencies:

```bash
npm install
```

3. Start the development server:

```bash
npm run dev
```

4. Open your browser and navigate to `http://localhost:3000`

### Docker Setup

This project includes Docker configuration for easy deployment:

1. Build and start the container:

```bash
docker-compose up
```

2. Access the application at `http://localhost:3000`

## Usage

1. Open the application in your browser
2. Grant camera and microphone permissions when prompted
3. Click the "Start" button to begin streaming
4. To stream to YouTube, update the RTMP URL in the `index.js` file with your YouTube stream key

## Configuration

The FFmpeg settings in `index.js` are optimized for YouTube Live streaming. You can modify these settings based on your specific requirements:

- Video codec: libx264 with ultrafast preset
- Frame rate: 25 fps
- Audio: AAC 128k

## Dependencies

- Express: Web server framework
- Socket.IO: Real-time bidirectional event-based communication
- FFmpeg: Media processing library (used for transcoding)
- Nodemon: Development utility for auto-restarting the server

## License

MIT