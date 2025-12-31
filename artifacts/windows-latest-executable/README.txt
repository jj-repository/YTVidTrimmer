===================================================================
  YoutubeDownloader v3.0.0 - Windows Edition
===================================================================

Thank you for downloading YoutubeDownloader!

A professional YouTube video downloader with advanced trimming
capabilities, clipboard monitoring, and catbox.moe upload integration.


QUICK START
===========

Just double-click "YoutubeDownloader.exe" - that's it!

All dependencies (ffmpeg, ffprobe, yt-dlp) are bundled inside.
No additional software installation required.

Note: If Windows Defender blocks it, click "More info" then "Run anyway"


FEATURES
========

Core Functionality:
- Multiple quality options (240p - 1440p)
- Audio-only extraction (M4A, 128kbps AAC)
- Video trimming with visual frame previews
- Real-time progress with speed and ETA
- Smart frame caching (10-50x faster)

Clipboard Mode:
- Auto-detect YouTube URLs from clipboard
- Auto-download option for detected URLs
- URL queue with batch download

Uploader Tab:
- Upload files to catbox.moe for sharing
- Multi-file upload queue
- Upload history tracking

Advanced Features:
- URL validation for all YouTube formats
- Auto-retry with exponential backoff (80%+ recovery)
- Download timeout protection
- Multi-language support (English, German, Polish)
- Volume control for audio processing


HOW TO USE
==========

Basic Download:
1. Paste a YouTube URL
2. Select quality (480p is default)
3. Click "Download"

Video Trimming:
1. Paste a YouTube URL
2. Check "Enable video trimming"
3. Click "Fetch Video Duration"
4. Adjust start/end times with sliders
5. Click "Download"

Clipboard Mode:
1. Switch to "Clipboard Mode" tab
2. Copy any YouTube URL (Ctrl+C)
3. URL is automatically detected
4. Click "Download All" to process queue

Downloads are saved to your Downloads folder by default.


SYSTEM REQUIREMENTS
===================

- Windows 10/11 (64-bit)
- ~200 MB disk space
- ~100 MB RAM during operation
- Internet connection


TROUBLESHOOTING
===============

App won't start:
  - Windows Defender: Click "More info" -> "Run anyway"
  - Check logs: %USERPROFILE%\.youtubedownloader\youtubedownloader.log

Preview frames not loading:
  - Check internet connection
  - Video may be age-restricted or private

Download stalling:
  - App auto-detects stalls after 5 minutes
  - Try a different quality


DEBUG LOGS
==========

Logs are saved to:
  %USERPROFILE%\.youtubedownloader\youtubedownloader.log


SUPPORT
=======

GitHub: https://github.com/jj-repository/YoutubeDownloader
Issues: https://github.com/jj-repository/YoutubeDownloader/issues


LICENSE
=======

This software is released under the MIT License.


CREDITS
=======

- yt-dlp: https://github.com/yt-dlp/yt-dlp
- FFmpeg: https://ffmpeg.org/
- Pillow: https://python-pillow.org/


===================================================================
Made with love for the community
https://github.com/jj-repository/YoutubeDownloader
===================================================================
