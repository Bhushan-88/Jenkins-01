# Jenkins Installation on ubuntu 
# add repo
sudo wget -O /etc/apt/keyrings/jenkins-keyring.asc \
  https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key
echo "deb [signed-by=/etc/apt/keyrings/jenkins-keyring.asc]" \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null

# Install jenkins
sudo apt-get update
apt install openjdk-21-jre -y # java package
sudo apt-get install jenkins -y
# access instance Ip http://184.72.127.27:8080/
# copy password location
cat /var/lib/jenkins/secrets/initialAdminPassword

# Need to install plugin
SSH Agent by using jenkins console for access slave/node
Git plugin by using jenkins console for pull code(This plugin integrates Git with Jenkins.) 
install plugin --> Pipeline 

# Types of pipeline 
1. Declarative pipeleine
2. Scripted pipeline


