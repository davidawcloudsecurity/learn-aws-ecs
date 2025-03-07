# learn-aws-ecs
How to use aws ecs to learn about nginx

### Install prerequisites 
sudo yum install -y jq

pip install --user --upgrade awscli

### Install copilot-cli
sudo curl -Lo /usr/local/bin/copilot https://github.com/aws/copilot-cli/releases/latest/download/copilot-linux && sudo chmod +x /usr/local/bin/copilot && copilot --help

### Setting environment variables required to communicate with AWS API's via the cli tools
echo "export AWS_DEFAULT_REGION=$(curl -s 169.254.169.254/latest/dynamic/instance-identity/document | jq -r .region)" >> ~/.bashrc
source ~/.bashrc
