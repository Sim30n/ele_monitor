arduino-cli compile --fqbn arduino:samd:mkrwifi1010 ele_monitor2
arduino-cli upload -p /dev/ttyACM1 --fqbn arduino:samd:mkrwifi1010 ele_monitor2
arduino-cli upload -p 192.168.50.131 --fqbn arduino:samd:mkrwifi1010 ele_monitor2