# activate environment

source .venv/bin/activate  

# setup remote upstram repo 

original repo added as second remote 

git remote rename origin upstream
you renamed the common repo to upstream
git pull upstream main (to pull from there)
git remote add origin https://github.com/clemvg/cool_robot_stuff.git
git push -u origin main (u flag to set by default) 

git remote -v
origin  https://github.com/clemvg/cool_robot_stuff.git (fetch)
origin  https://github.com/clemvg/cool_robot_stuff.git (push)
upstream        https://github.com/huggingface/lerobot.git (fetch)
upstream        https://github.com/huggingface/lerobot.git (push)

How to Stay Up to Date
git fetch upstream
Merge updates from the original repo into your main branch
git merge upstream/main

----
Tutorial fro my Robot arm 
https://github.com/huggingface/lerobot/blob/main/examples/10_use_so100.md


# install dependencies

pip install -e ".[feetech]"

# install dependencies

Need klemmen and dongle
Missing one gripper 

# Configure the motors

python lerobot/scripts/find_motors_bus_port.py

python lerobot/scripts/configure_motor.py \
  --port /dev/tty.usbmodem58FA0956361 \
  --brand feetech \
  --model sts3215 \
  --baudrate 1000000 \
  --ID 1

Removed the gear from leader arm 
I think I did this for both..

# Step-by-Step Assembly Instructions