#Foxglove bridge
ros2 run rosbridge_server rosbridge_websocket
ros2 run rosapi rosapi_node

#Foxglove Web Socket
ros2 launch foxglove_bridge foxglove_bridge_launch.xml port:=8765

#bag
ros2 bag record <topic1> <topic2> 
ros2 bag play <bag>

#maps - https://github.com/danielsnider/MapViz-Tile-Map-Google-Maps-Satellite?tab=readme-ov-file
sudo docker run -p 8080:8080 -d -t -v ~/mapproxy:/mapproxy danielsnider/mapproxy
http://127.0.0.1:8080/demo/
http://localhost:8080/wmts/gm_layer/gm_grid/{level}/{x}/{y}.png

#gps
ros2 run atgm336h5n3x nmea_node --dev /dev/myserial

#imu
ros2 launch witmotion_ros yahboom10x_launch.py
