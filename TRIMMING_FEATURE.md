# Video Trimming Feature

## Overview
The YTVidDownloader now supports trimming videos to specific start and end times. You can download only the portion of the video you need instead of the entire video.

## How to Use

### Step 1: Enter YouTube URL
Enter the YouTube video URL as usual in the URL field.

### Step 2: Enable Trimming
Check the "Enable video trimming" checkbox in the Trim Video section.

### Step 3: Fetch Video Duration
Click the "Fetch Video Duration" button. This will:
- Query the video's total length
- Display the duration (e.g., "Total Duration: 00:05:30")
- Enable the start and end time sliders

### Step 4: Adjust Time Range
Use the two sliders to select your desired video segment:
- **Start Time slider**: Move to where you want the video to begin
- **End Time slider**: Move to where you want the video to end
- Watch the time labels update in real-time (HH:MM:SS format)
- The "Selected Duration" shows how long your trimmed video will be

### Step 5: Download
- Select your video quality (or audio-only mode)
- Choose your download location
- Click "Download"

The downloaded file will contain ONLY the selected time range.

## Technical Details

### For Video Downloads
- Uses `--download-sections *HH:MM:SS-HH:MM:SS` flag
- Includes `--force-keyframes-at-cuts` for better accuracy
- Efficient: only downloads the selected segment

### For Audio Downloads
- Uses ffmpeg postprocessor with `-ss` (start) and `-to` (end) parameters
- Works with M4A audio extraction

## Example Use Cases

1. **Extract a specific song from a concert video**
   - Video duration: 01:30:00
   - Want song from: 00:15:30 to 00:19:45
   - Result: 4 minute 15 second clip

2. **Download just the intro of a tutorial**
   - Video duration: 00:45:00
   - Want intro: 00:00:00 to 00:02:30
   - Result: 2 minute 30 second clip

3. **Get audio clip from podcast**
   - Enable "Extract audio only"
   - Enable trimming
   - Select time range
   - Result: M4A audio file of just that segment

## Validation
- Start time must be before end time
- Duration must be fetched before downloading with trimming enabled
- Minimum selection: 1 second

## Notes
- Trimming may not be frame-perfect due to video keyframe locations
- For most accurate cuts, video is re-encoded
- Live streams may not support trimming
- The total video duration is fetched quickly without downloading the entire video
