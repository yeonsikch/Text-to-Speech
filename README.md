# Text-to-Speech
TTS (Glow-TTS + HiFi-GAN)
# 음성 녹음
- [여기](https://drive.google.com/file/d/1qWWBVerugPedNvaUbqYqwPhbIvWXnFxN/view?usp=sharing)에서 프로그램 설치<br>
- 대략 1시간 ~ 2시간 분량 녹음하면 되고, 이는 약 1000 ~ 2000문장이 됨
## 에러 해결
1. 2번째 녹음부터 저장이 되지 않는 에러 발생
  - 원인 : 저장되는 `metadata.txt` 파일이 중복되어 발생
  - 해결방법 : 실시간으로 생성되는 `metadata.txt`를 `metadata_1.txt`와 같이 변경해주면 됨
  - (Python Code)[]로 이를 해결
  - 후에 위 코드를 통해 모든 텍스트 파일을 하나로 합치는 작업을 진행
2. 녹음이 잘 되지 않는 에러 발생
  - 해결방법 : 5번 녹음할때마다 페이지 새로고침
# 모델 학습
- (Glow-TTS)[]를 통해 `Text`를 `MelSpectrogram`으로 인코딩하는 부분을 학습함
- (HiFi-GAN)[]을 통해 `MelSpectrogram`을 `Audio`로 보코딩하는 부분을 학습함
* 각 모델의 본 코드는 위 코드 내에서 `git clone`을 통해 설치하도록 되어있음
* 학습 시간 대략 각각 2~4시간이면 가능함(GPU 2080Ti * 1 기준)
