# ESP32 MQTT Server Set up
- source : https://docs.espressif.com/projects/esp-idf/en/stable/esp32/get-started/index.html

# sMQTT
- https://www.youtube.com/watch?v=ji_nfVEI25g

## For WiFi Hotspot
- replace the following codes 
```
const char *ssid="FRITZ!Box 6660-Cable-IF-2.4";
const char *password = "12424743535889846960";
    WiFi.begin(ssid, password);
    while. (WiFi.status() != WL_CONNECTED) { // Wait for the Wi-Fi-to-connect
delay(1000);
}
    Serial.println("Connection established!");..
    Serial.print("IP-address:\t");
    Serial.println(WiFi.localIP());
```
 - with

```
WiFi.softAP("ESP32_Hotspot", "12345678");
// Replace with your SSID and password
I
// Display the IP address of the ESP32
IPAddress IP WiFi.softAPIP();
Serial.print("AP IP address: ");
Serial.println(IP);

```
