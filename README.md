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
