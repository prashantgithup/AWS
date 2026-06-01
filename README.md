
Installing AWS CLI on Ubuntu
You can install AWS CLI on Ubuntu using multiple methods. The official installer is recommended for AWS CLI v2 as it’s maintained by AWS and works independently of system Python versions.

Method 1: Install via Official AWS Installer

Install required tools: sudo apt install curl unzip -y

Download the AWS CLI v2 installer: curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o awscliv2.zip

Extract the installer archive: unzip awscliv2.zip

Run the installation script: sudo ./aws/install

Verify installation: aws --version

Remove installer files: rm -rf awscliv2.zip aws/

-----------------------------------------------------------------------------------------------------------------------------------------------

Method 2: Install via Snap

Ensure Snap is installed: sudo apt install snapd -y

Install AWS CLI v2 from Snap Store: sudo snap install aws-cli --channel=v2/stable --classic

Verify installation: aws --version

-------------------------------------------------------------------------------------------------------------------------------------------------

Method 3: Install via pip (AWS CLI v1)

Install pip and venv: sudo apt install python3-pip python3-venv -y

Create a virtual environment: python3 -m venv ~/.aws-venv

Activate the environment: source ~/.aws-venv/bin/activate

Install AWS CLI v1: pip install awscli

Verify installation: aws --version

Configure AWS CLI

Run the configuration wizard: aws configure

Enter your AWS Access Key ID, Secret Access Key, Default region, and Output format when prompted.

Test configuration by listing S3 buckets: aws s3 ls
