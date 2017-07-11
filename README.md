## About the project

This project provides a step-by-step walkthrough to help you build a **hands-free** [Alexa Voice Service](https://developer.amazon.com/avs) (AVS) prototype in 60 minutes, using wake word engines from [Sensory](https://github.com/Sensory/alexa-rpi) or [KITT.AI](https://github.com/Kitt-AI/snowboy). Now, in addition to pushing a button to "start listening", you can now also just say the wake word "Alexa", much like the [Amazon Echo](https://amazon.com/echo). You can find step-by-step instructions to set up the hands-free prototype on [Raspberry Pi](../../wiki/Raspberry-Pi), or follow the instructions to set up the push-to-talk only prototype on [Linux](../../wiki/Linux), [Mac](../../wiki/Mac), or [Windows](../../wiki/Windows).

---

## What is AVS?

[Alexa Voice Service](https://developer.amazon.com/avs) (AVS) is Amazon’s intelligent voice recognition and natural language understanding service that allows you as a developer to voice-enable any connected device that has a microphone and speaker.

---

## Get started
refs: https://blog.sparrows.co.jp/

* [Raspberry Pi](../../wiki/Raspberry-Pi), or
* [Mac](../../wiki/Mac)

Or you can prototype with these third-party dev kits -

* *New!* [Raspberry Pi + Microsemi AcuEdge Development Kit for Amazon AVS](https://github.com/MicrosemiVoiceProcessing/ZLK38AVS/wiki/howto)    
* [Raspberry Pi + Conexant 4-mic Development Kit for Amazon AVS](https://github.com/conexant/alexa-avs-sample-app/wiki/Conexant4Mic-Raspberry-Pi)
* [Raspberry Pi + Conexant 2-Mic Development Kit for Amazon AVS](../../wiki/Conexant2Mic-Raspberry-Pi)  

## Start
refs: https://github.com/alexa/alexa-avs-sample-app/wiki/Raspberry-Pi

Terminal Window 1

Open a new terminal window and type the following commands to bring up the web service which is used to authorize your sample app with AVS:

```sh
cd ~/alexa-avs-sample-app/samples
cd companionService && npm start
```
Terminal Window 2

Open a new terminal window and type the following commands to run the sample app, which communicates with AVS:

```sh
cd ~/alexa-avs-sample-app/samples
cd javaclient && mvn exec:exec
```

Terminal Window 3

Open a new terminal window and use the following commands to bring up a wake word engine from Sensory or KITT.AI. The wake word engine will allow you to initiate interactions using the phrase "Alexa".

```sh
# To use the Sensory wake word engine, type -
cd ~/alexa-avs-sample-app/samples
cd wakeWordAgent/src && ./wakeWordAgent -e sensory
# OR
# type this to use KITT.AI's wake word engine -
cd ~/alexa-avs-sample-app/samples
cd wakeWordAgent/src && ./wakeWordAgent -e kitt_ai
```

call Alexa!!!
