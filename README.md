# ArduinoHttpClient - ESP32 Compatible Fork

[![Check Arduino status](https://github.com/arduino-libraries/ArduinoHttpClient/actions/workflows/check-arduino.yml/badge.svg)](https://github.com/arduino-libraries/ArduinoHttpClient/actions/workflows/check-arduino.yml)
[![Compile Examples status](https://github.com/arduino-libraries/ArduinoHttpClient/actions/workflows/compile-examples.yml/badge.svg)](https://github.com/arduino-libraries/ArduinoHttpClient/actions/workflows/compile-examples.yml)
[![Spell Check status](https://github.com/arduino-libraries/ArduinoHttpClient/actions/workflows/spell-check.yml/badge.svg)](https://github.com/arduino-libraries/ArduinoHttpClient/actions/workflows/spell-check.yml)

> This fork tracks upstream with only renamed HttpClient files. This makes it compatible with Arduino-ESP32's built-in HTTPClient class. ESP32's class only supports the built-in Wi-Fi, so this library allows other interfaces to be used for HTTP requests.
>
> This collision only occurs on Windows as the file paths are case-insensitive. The class name can be preserved as the c++ compiler differentiates between HttpClient and HTTPClient.

ArduinoHttpClient is a library to make it easier to interact with web servers from Arduino.

Derived from [Adrian McEwen's HttpClient library](https://github.com/amcewen/HttpClient)

## Dependencies

- Requires a networking hardware and a library that provides transport specific `Client` instance, such as:
  - [WiFiNINA](https://github.com/arduino-libraries/WiFiNINA)
  - [WiFi101](https://github.com/arduino-libraries/WiFi101)
  - [Ethernet](https://github.com/arduino-libraries/Ethernet)
  - [MKRGSM](https://github.com/arduino-libraries/MKRGSM)
  - [MKRNB](https://github.com/arduino-libraries/MKRNB)
  - [WiFi](https://github.com/arduino-libraries/WiFi)
  - [GSM](https://github.com/arduino-libraries/GSM)

## Usage

In normal usage, handles the outgoing request and Host header. The returned status code is parsed for you, as is the Content-Length header (if present).

Because it expects an object of type Client, you can use it with any of the networking classes that derive from that. Which means it will work with WiFiClient, EthernetClient and GSMClient.

See the examples for more detail on how the library is used.
