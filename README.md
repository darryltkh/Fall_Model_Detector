# SafeSteps - Elderly fall? We catch!

---

This is the project we have done for iNTUition 2023 Hackathon organised by IEEE NTU Student Branch.
You can check out our [DevPost writeup](https://devpost.com/software/safesteps-kcevrm) on our project in the competition page. 

This repository only focuses on developing the deep learning model used in the Arduino Nano 33 BLE Sense board. You can find the full repository [here](https://github.com/King-Of-Spades-K).

You can check out our presentation slides [here](https://docs.google.com/presentation/d/e/2PACX-1vSJeOw8KLRakesKPEGnFp0DGCtCOXtDSc4LEjiDSzc49gd4yT7DtWOCcceC3zgQa_U1ViXx2yKjNA4j/pub?start=false&loop=false&delayms=3000&slide=id.p).

## Below is a snippet of our writeup in Devpost:
---
What it does:
- SafeSteps is a wearable IoT device that can be strapped to the arm
- Detects when the wearer falls
- Immediately sends a Telegram message to family members, alerting them
- Also displays falls in a dashboard to see if the elderly are very prone to falling, thus requiring more care
- Allows doctors/nurses to also monitor all patients under their care

How we built it:
- We used edge computing to perform computation on a low-performant device using embedded-C.
- We used an Arduino board and used Tensorflow-lite to deploy a Machine Learning model in it.
- Fall detection is performed within the Arduino itself.
- We wrote python scripts for an RPi server. Arduino sends data to RPi through serial communication.
- RPi server is connected to the internet and updates the Firebase real-time db.
- RPi also calls the Telegram API to send a text to the family member.
- Family members/doctors can monitor falls through a web client.
- They can see past history of falls to see if the elderly are more prone to falls, thus getting more attention.
- Web client was built using React, Typescript, Tailwindcss.
- When a fall occurs, the client gets a push notification as well.

What we learned
- Hardware development
- Machine Learning in edge computing devices
- Front End Web Development
- Server Side Development
