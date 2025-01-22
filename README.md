# YouTube Comment Scraper

A Python script to scrape comments from a YouTube video using the YouTube Data API v3. This project retrieves comments from a specified video and saves them in a CSV file for further analysis.

---

## Features
- Fetches top-level comments from a YouTube video.
- Handles pagination to retrieve all comments.
- Saves comments in a user-friendly CSV format.
- Includes error handling for API and connection issues.

---

## Prerequisites

### 1. **Python Environment**
Ensure you have Python 3.7 or higher installed. You can download it from [python.org](https://www.python.org/downloads/).

### 2. **YouTube Data API Key**
1. Visit the [Google Cloud Console](https://console.cloud.google.com/).
2. Create a new project or use an existing one.
3. Enable the **YouTube Data API v3**.
4. Create an API key from **APIs & Services > Credentials**.

---

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/youtube-comment-scraper.git
   cd youtube-comment-scraper
   ```

2. Install required dependencies:
   ```bash
   pip install google-api-python-client
   ```

---

## Usage

### 1. Prepare the Script
Open `youtube_comment_scraper.py` and replace `YOUR_API_KEY` with your YouTube Data API key:

```python
yt_client = build(
    "youtube", "v3", developerKey="YOUR_API_KEY"
)
```

### 2. Run the Script
Run the script using the terminal:
```bash
python youtube_comment_scraper.py <video_id> <output_file.csv>
```

- Replace `<video_id>` with the ID of the YouTube video (e.g., `M7lc1UVf-VE`).
- Replace `<output_file.csv>` with the desired filename for storing comments (e.g., `comments.csv`).

### Example:
```bash
python youtube_comment_scraper.py M7lc1UVf-VE comments.csv
```

---

## Error Handling

### Common Issues
1. **Invalid API Key**
   - Ensure your API key is valid and has access to the YouTube Data API.

2. **Video Not Found**
   - Verify the `video_id` is correct and the video is public.

3. **Quota Exceeded**
   - Check your API quota in the [Google Cloud Console](https://console.cloud.google.com/).

---




