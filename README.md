# ros2_people_finder

Este projeto tem o objetivo de explorar, mapear e detectar pessoas em um ambiente de um hospital simulado pelo software de simulação [Gazebo](https://gazebosim.org/home) por meio do ROS 2 e posteriormente, simular uma possível rota para guiar essa pessoa localizada para o início do hospital. 

## Dependências Principais 

- [ROS2 - Humble](https://docs.ros.org/en/humble/index.html)
- Python 3
- [Ubuntu 22.04](https://releases.ubuntu.com/jammy/)

### Pacotes do ROS2

- [Turtlebot3](https://github.com/ROBOTIS-GIT/turtlebot3.git)
- [Turtlebot3_simulations](https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git)
- [Turtlebot3_msgs](https://github.com/ROBOTIS-GIT/turtlebot3_msgs)
- [Aws-robomaker-hospital-world](https://github.com/aws-robotics/aws-robomaker-hospital-world)
- [M-explore-ros2](https://github.com/robo-friends/m-explore-ros2)
- [navigation2](https://github.com/ros-planning/navigation2)

### Pacotes do Python

- [Numpy](https://pypi.org/project/numpy/)
- [Opencv](https://opencv.org/)
- [Pytorch](https://pytorch.org/)
- [Yolov5](https://github.com/ultralytics/yolov5)
- Rclpy (Pacote do ROS2)

## Metodologia

Inicialmente o robô é gerado na posição onde é a recepção do hospital, sendo que o mapa do ambiente não é conhecido e nem a localização da pessoa no mundo. Assim, quando detectado a pessoa no mundo, o robô retorna a recepção do hospital.

### Exploração e navegação autônoma

É utilizado o pacote de navegação [M-explore-ros2](https://github.com/robo-friends/m-explore-ros2) para a realização desta exploração, realizando a navegação de forma autônoma do robô móvel por meio da busca de fronteira do mapa de custo. Neste caso, é também utilizado o Slam do [navigation2](https://github.com/ros-planning/navigation2) para realizar a criação do mapa simultaneamente a exploração autônoma.

### Deteção 

É utilizado o pacote NOME DO PACOTE que utiliza o [Yolov5](https://github.com/ultralytics/yolov5) para detectar a pessoa no ambiente.
