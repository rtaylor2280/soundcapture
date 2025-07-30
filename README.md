# soundcapture

YouTube Audio Extractor
The YouTube Audio Extractor is a single-page web application built with React and Tailwind CSS, designed to simulate extracting audio from YouTube videos. Users can input a YouTube URL, select an audio format (MP3 or WAV), and optionally specify a time range for trimming the audio. The app includes a "Saber Font" option for WAV files, producing high-quality audio (PCM, 16-bit, 44.1 kHz, mono) suitable for applications like lightsaber sound effects. The app is deployed on Vercel and can be accessed at https://jedimastertech.com/soundcapture.
Note: This app currently simulates audio extraction and downloading due to client-side limitations. Actual audio processing requires a server-side backend (e.g., using yt-dlp and ffmpeg) or a third-party API (e.g., Listnr AI).
Features

YouTube URL Input: Paste a YouTube video URL to initiate audio extraction.
Audio Formats: Choose between MP3 (compressed) or WAV (uncompressed).
Saber Font Option: When selecting WAV, enable "Saber Font" for PCM, 16-bit, 44.1 kHz, mono output (stereo supported).
Time Trimming: Specify start and end times (MM:SS or HH:MM:SS) to extract a specific audio segment.
Responsive Design: Styled with Tailwind CSS for a clean, mobile-friendly UI.
Simulated Download: Generates a mock download link (to be replaced with actual backend processing).

Technologies Used

React: Client-side rendering and state management.
Tailwind CSS: Styling for a responsive and modern UI.
CDNs: React, ReactDOM, Babel, and Tailwind CSS loaded via jsDelivr.
Vercel: Hosting platform for deployment.
GitHub: Version control and continuous deployment.

Prerequisites

Git: For cloning and managing the repository.
Vercel Account: For deployment (free tier).
GitHub Account: To host the repository.
Custom Domain (optional): To serve the app at jedimastertech.com/soundcapture.

Installation and Setup
1. Clone the Repository
git clone https://github.com/your-username/soundcapture.git
cd soundcapture

Replace your-username with your GitHub username.
2. Project Structure
soundcapture/
├── index.html      # Main app file with React and Tailwind CSS
├── vercel.json     # Vercel configuration for routing
├── README.md       # This file

3. Deploy to Vercel

Sign Up/Login to Vercel: Go to vercel.com and sign up with GitHub.
Import Repository:
In the Vercel Dashboard, click Add New > Project.
Select the soundcapture repository and click Import.
Use default settings (no build command or output directory needed).
Click Deploy.


Custom Domain (optional):
In Vercel Dashboard, go to Settings > Domains.
Add jedimastertech.com.
In your domain registrar (e.g., Hostinger), set a CNAME record:
Name: @
Value: cname.vercel-dns.com


The app will be accessible at https://jedimastertech.com/soundcapture.



4. Local Development
To test locally:
python -m http.server 8000

Open http://localhost:8000 in a browser (requires internet for CDNs).
Usage

Access the App: Visit https://jedimastertech.com/soundcapture or your Vercel URL (e.g., soundcapture.vercel.app).
Input YouTube URL: Paste a valid YouTube URL (e.g., https://www.youtube.com/watch?v=VIDEO_ID).
Select Format: Choose MP3 or WAV. For WAV, optionally check "Saber Font" for PCM, 16-bit, 44.1 kHz, mono output.
Specify Time Range (optional): Enter start and end times (e.g., 01:30 to 02:15) for trimming.
Extract Audio: Click "Extract Audio" to simulate processing (2-second delay).
Download: Click "Download MP3/WAV" to simulate downloading a mock file.

Note: Actual audio extraction requires a backend. See "Future Improvements" below.
Future Improvements

Backend Integration: Add a Vercel serverless function with yt-dlp and ffmpeg to process YouTube audio. Example:yt-dlp --extract-audio --audio-format wav --postprocessor-args "-ss 01:30 -to 02:15 -ac 1 -ar 44100 -acodec pcm_s16le" <URL>


Third-Party API: Integrate services like Listnr AI or Media.io for audio extraction.
Audio Preview: Add a player to preview the extracted audio before download.
Error Handling: Enhance validation for YouTube video duration and availability.

Legal Considerations
Ensure the YouTube audio is copyright-free or you have permission to extract it, as per YouTube’s terms and services like Listnr AI.
Contributing

Fork the repository.
Create a branch: git checkout -b feature-name.
Commit changes: git commit -m "Add feature".
Push to the branch: git push origin feature-name.
Open a pull request.

License
MIT License - feel free to use and modify this project.
Contact
For issues or suggestions, open a GitHub issue or contact the repository owner.
