# Smart-Home-Plan
# What this project does
* The Pico W reads the temperature. If it gets too hot, it turns something on (like an LED or fan) and sends an
alert message to Discord.
* What we need
* Part Job
* Raspberry Pi Pico W The brain of the project
* Temperature sensor Measures the temperature
* LED (or fan/buzzer) Turns on when it gets too hot
* The one simple rule
a. If temperature is above 30°C Ô turn the LED on and send a Discord alert.
b. If temperature drops back below 30°C, the LED turns off again.
# The alert message
* Temperature too high!
* Current: 31.8°C
* Limit: 30.0°C
# How it connects
* The Pico W connects to Wi-Fi. When the temperature rule is triggered, it sends the alert message straight to
a Discord channel using a webhook link.
# System architecture
* The system follows three simple steps: sense the temperature, decide with the rule, and act by switching
the LED and sending the alert.
Temperature sensor
measures the
temperature
Raspberry Pi Pico W
reads temperature,
checks the rule
LED (or fan/buzzer)
on when too hot,
off when OK
reading on / off
Wi-Fi router
and the Internet
Discord channel
shows the alert
Wi-Fi (only when too hot)
webhook link
INPUT (sense) PROCESSING (decide) OUTPUT (act)
NETWORK ALERT (cloud)
*Figure 1: System architecture. The LED reacts directly on the Pico. The Discord alert travels over Wi-Fi and the Internet
through the webhook link.

| Block  | What it does |
| :--- | :--- |
| **Input: temperature sensor** | Measures the temperature and sends the reading to the Pico W. | 
| **Processing: Pico W** | Reads the sensor, checks if the temperature is above 30°C, and decides what to do. | 
| **Output: LED** | Turns on above 30°C and off again when the temperature drops below 30°C. | 
| **Network: Wi-Fi + webhook** | Carries the alert message from the Pico W to the Discord channel. |

What happens each time
1. The sensor measures the temperature.
2. The Pico W reads it and compares it with the 30°C limit.
3. Above 30°C: the LED turns on and the alert is sent to Discord.
4. Below 30°C: the LED stays off.
5. The Pico W waits a couple of seconds and repeats.
That's it
One sensor, one output, one rule, one alert. This covers the basic idea of the assignment in the simplest
way possible.
