from moviepy.editor import *

# 비디오 클립 로드
clip = VideoFileClip("input_video.mp4")

# 비디오 클립에 텍스트 추가
txt_clip = TextClip("Hello, Replit!", fontsize=70, color='white')
txt_clip = txt_clip.set_pos('center').set_duration(10)

# 비디오와 텍스트 합치기
video = CompositeVideoClip([clip, txt_clip])

# 결과 비디오 저장
video.write_videofile("output_video.mp4", fps=24)
