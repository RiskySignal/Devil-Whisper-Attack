# Devil-Whisper-Attack

&emsp;&emsp;We present Devil’s Whisper, a general adversarial attack on commercial ASR systems. Our idea is to enhance a simple local model roughly approximating the target model of an ASR system with a white-box model that is more advanced yet unrelated to the target. We find that these two models can effectively complement each other in predicting the target’s behavior, which enables highly transferable and generic attacks on the target. The adversarial examples (AEs) can effectively exploit the commercial devices (Google Home, Amazon Echo, Microsoft Cortana, etc) with 96% of the target commands successful on average.

Our AEs are trained against a specific target IVC service. An AE against one service may not work well on the other, since it is generated by the substitute model (together with the base model), which is trained specifically to simulate the target service. Below the target details of AEs are given:

Target IVC service: Google Assistant
01.wav - Okay Google, take a picture.
02.wav - Okay Google, navigate to my home.
Target IVC service: Google Home
03.wav - Okay Google, turn off the light.
04.wav - Okay Google, play music.
Target IVC service: Microsoft Cortana
05.wav - Hey Cortana, open the website.
06.wav - Hey Cortana, make it warmer.
Target IVC service: Amazon Echo
07.wav - Echo, call my wife.
08.wav - Echo, turn off the computer.

The success of an AE depends on the quality of the speaker (to play the AEs) and the microphone of a target device (to receive the AEs on the device), also effeted by many other factors like volume, distance between speaker and target device, the angle between the speaker and IVC device.
