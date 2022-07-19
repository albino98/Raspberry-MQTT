# Raspberry-MQTT
Security system with raspberry, mqtt and esp32 cam

## Description

![schema](https://user-images.githubusercontent.com/63566699/179841474-05ebdde3-7ff6-4c4a-b6f4-73e0fe397b97.png)


## Configuration

### Raspberry

- **1** : To **configure an MQTT broker** on our raspberry you can install mosquitto by following the multiple online guides (eg : https://www.ev3dev.org/docs/tutorials/sending-and-receiving-messages-with-mqtt/). However, I summarize below the only three necessary steps:
      
  ```
  sudo apt update && sudo apt upgrade
  ```

  ```
  sudo apt-get install mosquitto
  ```

  You can check if it is working by using the following command:

  ```
  systemctl status mosquitto
  ```

  or

  ```
  sudo service mosquitto status
  ```
  
  Remember that if you want to use the MQTT broker only locally without exposing it to the network you don't need to set up authentication, so just run the commands above. However, if you still want to set up authentication on the broker or want to expose your ip address for remote access then follow the online guides like this: https://randomnerdtutorials.com/how-to-install-mosquitto-broker-on-raspberry-pi/, or official documentation: https://mosquitto.org/documentation/authentication-methods/.
