<img width="935" height="623" alt="image" src="https://github.com/user-attachments/assets/91085fa2-9d82-48ea-b7a1-3659e0f325a1" />

🛠️ ESP32 & FreeRTOS: The Multi-Functional Workshop Assistant I Designed

🎯 The Story Behind the Project and My Goal During my workshop sessions, I needed a compact and reliable assistant that could monitor environmental conditions (temperature, light, noise) in real-time. Instead of using individual solutions available on the market, I designed this device with a “Digital Swiss Army Knife” vision, which collects all this data on a single screen.

While developing this project, my main goal was not only to read sensor data but also to overcome performance bottlenecks commonly encountered in embedded systems using modern methods.

💡 My Technical Approach: Why Did I Choose FreeRTOS? I noticed that the loop() architecture used in traditional Arduino projects blocks (freezes) the system, especially when reading slow sensors like the DHT11.

To solve this problem:

My Hardware Choice: I chose the ESP32 because of its dual-core architecture.

Software Architecture: I integrated the FreeRTOS operating system into my project to fully utilize the processor's power.

Thus, I designed sensor reading, screen updating, and button responses as independent Tasks. As a result, I created a real-time system that operates without any freezing on the interface.
