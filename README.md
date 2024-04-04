# jenkins-installation
apt update
java -version (install 11 version)
sudo wget -O /usr/share/keyrings/jenkins-keyring.asc \
  https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null

  apt-get update
  apt-get install jenkins
  Add 8080 port number in security groups.
  Copy the path and paste in the terminal(for password)

  For changing port number
	systemctl status jenkins 
	systemctl enable --now jenkins
 Cd /usr/lib/systemd/system/
 vi jenkins.service (change the port number in the place of 8080)
 click Esc and then type :q! Enter (Exit)
 systemctl daemon-reload
 systemctl restart jenkins.service
 Add the port number in security groups.
 
