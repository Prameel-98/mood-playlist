# Mood-Based Music Picker: Emotion-Driven Music Experience

Introduction
The Mood-Based Music Picker project uses AWS's serverless architecture to detect users' moods from audio recordings and deliver a curated Spotify playlist based on their emotional tone. The app features a responsive web interface where users can record their voice, have it transcribed and analyzed, and receive personalized music recommendations.

Objectives
Frontend: Create a React-based interface that records audio and connects with backend APIs.

Backend: Implement a serverless backend using AWS Lambda for mood detection and playlist curation.

Mood Detection: Use Amazon Transcribe and Comprehend for audio transcription and mood analysis.

Spotify Integration: Map moods to curated playlists from Spotify.

Hosting: Deploy the frontend on Amazon S3 and use CloudFront for global access.

Tools & Services Used
Amazon S3: Hosts the frontend and audio files.

AWS Lambda: Serverless backend logic for transcription, mood detection, and playlist mapping.

Amazon API Gateway: Exposes Lambda functions via REST APIs.

Amazon DynamoDB: Stores mood logs and user history.

Amazon Transcribe: Converts audio into text.

Amazon Comprehend: Analyzes text for emotional tone.

Spotify Web API: Provides mood-based playlists.

CloudFront: Delivers the frontend globally with caching.

React + TailwindCSS: For a dynamic and responsive UI.

Project Structure
Frontend (React):

Components: AudioRecorder.jsx, MoodRing.jsx, PlaylistPlayer.jsx, MoodHistory.jsx, App.jsx

api.js: Manages API calls to backend.

Backend (AWS Serverless):

S3 Bucket: Hosts frontend and audio files.

DynamoDB Table: Stores mood logs with attributes like text, mood, and playlist URL.

Lambda Functions:

getUploadUrl: Provides presigned URL for audio upload.

transcribeAudio: Transcribes audio.

analyzeMood: Analyzes text for mood.

mapPlaylist: Maps mood to playlist.

getMoodHistory: Retrieves mood history.

API Gateway Endpoints:

POST /upload-url, POST /transcribe, POST /analyze, POST /map, GET /history.

Workflow
Start Recording: User records audio and uploads it to S3.

Transcription: Audio is transcribed via /transcribe.

Mood Detection: Text is analyzed for mood using /analyze.

Playlist Mapping: Mood is mapped to a Spotify playlist via /map.

Display: Playlist and mood emoji are shown to the user.

Mood History: User's mood and playlist are stored and can be viewed under /history.

User Experience
Intuitive UI: Simple and clear interface for recording and mood detection.

Mood Visuals: Emojis represent detected moods.

Spotify Playlists: Curated music playlists are embedded and played.

Mood History: Users can view previous mood logs and playlists.

