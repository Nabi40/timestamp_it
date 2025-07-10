# timestamp_it
🕒 Timestamp Finder for Video Using Whisper ASR  
This project provides a simple method to find when a specific sentence or phrase is spoken in a video by transcribing the audio using OpenAI's Whisper model.  

It allows users to pass in a search phrase (query), and it will return the timestamp (in seconds) when that phrase first appears in the audio.  


**How It Works📌**  
Video Upload:  
User uploads a .mp4 video (in the /content/video/ folder on Colab).  

Model Loading:  
The whisper model (base) is loaded.  

Transcription:  
Full audio is transcribed and segmented.  

Query Search:  
The query string is matched against each segment.  
If found, the corresponding start time (in seconds) of that segment is returned.  

Video Display:  
The video is embedded in the notebook using HTML5 video.  


**Example output📌**   
query = "You said he wants to erode the very fabric of civilization"  
get_timestamp_for_query(video_path, query)  

output:  
Timestamp: 104.2 seconds  



**Strengths📌**  
Extremely easy to use with minimal code.  
Uses state-of-the-art Whisper ASR model.  
No external dependencies apart from openai-whisper.  





**Limitations📌**  
Whisper might not detect exact matches due to:  
  Word contractions (e.g., “he’s” vs “he is”)  
  Accents, noise, or audio quality  
  Slight text mismatches (consider fuzzy matching) 

Only returns the first matching timestamp.  
Can be slow on longer videos or lower-spec machines.  
