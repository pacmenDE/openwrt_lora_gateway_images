# openwrt_v18.09_lora_gateway_images
openwrt 18.06 with running lora Gateway and packet forwarder based on https://github.com/xueliu/lora-feed here you can find running openwrt images for some devices.


# RASPI how to

1.) flash image to sdcard

2.) connect HDMI in keyboard

3.) turn on 

4.) with passwd change root password

5.) set wireless on with

  uci set wireless.radio0.disabled=0
  
  uci commit
  
  reboot

6) configure wifi as wifi client as descriped here :https://openwrt.org/docs/guide-user/network/wifi/connect_client_wifi

7.) setup your gateway id

    uci set lora-global.gateway_conf.gateway_ID='YOUR GATEWAYID' TTN
    uci set lora-global.SX1301_conf.reset_pin='YOUR RESET PIN'

8.) reboot your device.

After reboot the device takes about 1 min and packet forwarder connects to ttn.
