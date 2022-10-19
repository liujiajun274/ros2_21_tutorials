# A workspace
workspace is a container for your project, at local computer. You can modify and test your code in the workspace

    mkdir -p ~/dev_ws/src     # create the directory for DEVelopment WorkSpace's SouRCe code
    cd ~/dev_ws/src           # change directory
    git clone ....            # clone the git repo

## install the dependencies 
Command-line tool for installing system dependencies 

    sudo apt install -y python3-pip
    sudo pip3 install rosdepc
    sudo rosdepc init
    rosdepc update
    cd ..
    rosdepc intall -i --from-path src --rosdistro humble -y

## build the workspace
This is a simple test on compiling the the workspace

    sudo apt intall python3-colcon-ros
    cd ~/dev_ws/
    colcon build

## set the environment

    source intall/local_setup.sh # only effective at current terminal
    echo "source ~/dev_ws/intall/local_setup.sh" >> ~./bashrc # effective for all terminals

# A Package
The command. BUILD-TYPE can be ament_cmake / ament_python

    ros2 pkg create --build-type <BUILD-TYPE> <PACKAGE-NAME>

eg:

    cd ~/dev_ws/src
    ros2 pkg create --build-type ament_python myfirstpackage 
    cd ~/dev-ws
    colcon build
    source install/local_setup.bash