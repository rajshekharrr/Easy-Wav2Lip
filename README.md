# Easy-Wav2Lip
Make Anime Movie Cartoon Speak Lip-Sync Characters in Any Language
### For the easiest and most compatible way to use this tool, use the Google Colab version:

## Google Colab:
[https://colab.research.google.com/github/anothermartz/Easy-Wav2Lip/blob/v8.3/Easy_Wav2Lip_v8.3.ipynb](https://colab.research.google.com/github/anothermartz/Easy-Wav2Lip/blob/v8.3/Easy_Wav2Lip_v8.3.ipynb)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/anothermartz/Easy-Wav2Lip/blob/v8.3/Easy_Wav2Lip_v8.3.ipynb)

# Credits:
* [The Original Wav2Lip](https://github.com/Rudrabha/Wav2Lip) of course.
* The huge speed increase and improved base quality comes from [cog-Wav2Lip](https://github.com/devxpy/cog-Wav2Lip).
* Code to upscale with [GFPGAN](https://github.com/TencentARC/GFPGAN) mainly came from [wav2lip-hq-updated-ESRGAN](https://github.com/GucciFlipFlops1917/wav2lip-hq-updated-ESRGAN).
* I couldn't have done this without AI assistance; Before making this I had very minimal python experience! LLM of choice: **Bing Chat** (now called 'Copilot').
* Thanks to [JustinJohn](https://github.com/justinjohn0306) for making the [Wav2Lip_simplified](https://colab.research.google.com/github/justinjohn0306/Wav2Lip/blob/master/Wav2Lip_simplified_v5.ipynb) colabs which inspired me to make my own, even simpler version.

## Support
If you're having issues running this, please look through the [issues tab](https://github.com/anothermartz/Easy-Wav2Lip/issues) to see if someone has written about it. If not, make a new thread but make sure you include the following:<br>
 <br> **If colab:**
 - Easy-Wav2Lip colab version number
 - Info about the files used.

For general chit chat about this and any other lipsync talk, I'll be in this discord:<br>
Invite link: https://discord.gg/FNZR9ETwKY<br>
Wav2Lip channel: https://discord.com/channels/667279414681272320/1076077584330280991

# Best practices:
* The best results come from lining up the speech to the actions and expressions of the speaker before you send it through wav2lip!

Video files:
* Must have a face in all frames or Wav2Lip will fail
* Crop or mask out faces you don't want to lipsync or it'll choose randomly.
* Use h264 .mp4 - other file types may be supported but this is what it outputs as
* Images are currently untested.
* Use a small file in every way (try <720p, <30 seconds, 30fps <b></b> etc. - Bigger files may work but are usually the reason it fails)
* For your first try, use a really tiny clip just to get used to the process, only once you're familiar should you try bigger files to see if they work.

Audio files:
* Save as .wav and the same length as your input video. If You didn't then I have to do it - I(colab) will convert .mp3 to .wav by processing, which will take little bit more time of Yours.
* NOTE: I've noticed that about 80ms gets cut from the processed video/audio and I'm not sure how to fix this, so make sure you have a little extra than what you actually need!

# Advanced Tweaking:
## wav2lip_version:
| Option | Pros | Cons |
|:-------|:-----|:-----|
| Wav2Lip | + More accurate lipsync <br> + Attempts to keep the mouth closed when there is no sound | - Sometimes produces missing teeth (uncommon) |
| Wav2Lip_GAN | + Looks nicer <br> + Keeps the original expressions of the speaker more | - Not as good at masking the original lip movements, especially when there is no sound |

I suggest trying Wav2Lip first and switching to the GAN version if you experience an effect where it looks like the speaker has big gaps in their teeth.
