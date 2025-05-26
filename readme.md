arduino-cli compile --fqbn arduino:samd:mkrwifi1010 ele_monitor2
arduino-cli upload -p /dev/ttyACM1 --fqbn arduino:samd:mkrwifi1010 ele_monitor2
arduino-cli upload -p 192.168.50.131 --fqbn arduino:samd:mkrwifi1010 ele_monitor2

Create arduino_screts.h file that includes:

#define SECRET_SSID "wifi_name"
#define SECRET_PASS "wifi_password"
#define SECRET_SERVER "server_ip"

See arduino_secrets.example.h 

file![Nimetön (2)](https://github.com/user-attachments/assets/e95c3bf1-6e51-4d4a-9980-aa252e9faf1f)
