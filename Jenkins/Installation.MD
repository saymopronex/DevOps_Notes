**Commands: Setup Machine and Install Jenkins**

1. Verify Installed Java Version

<sub> java -version </sub>

2. Install Java8 on Linux machine

<sub> sudo apt-get -y install openjdk-8-jdk openjdk-8-jre </sub>

<sub> java -version </sub>

3. Set JAVA_HOME variables

<sub> cat >> /etc/environment <<EOL </sub>

<sub> JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64 </sub>

<sub> JRE_HOME=/usr/lib/jvm/java-8-openjdk-amd64/jre </sub>

<sub> EOL </sub>

4. First, add the repository key to the system

<sub> wget -q -O - https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo apt-key add - </sub>

5. Next, append the Debian package repository address to the server’s sources.list

<sub> sudo sh -c 'echo deb http://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list' </sub>

6. Update System packages

<sub> sudo apt update </sub>

7. Install Jenkins and its dependencies

<sub> sudo apt -y install jenkins </sub>

8. Start Jenkins using systemctl

<sub> sudo systemctl start jenkins </sub>

9. Get Service Status

<sub> sudo systemctl status jenkins </sub>

10. Enable Jenkins Service

<sub> sudo systemctl enable jenkins </sub>

11. Use the cat command to display the password:

<sub> sudo cat /var/lib/jenkins/secrets/initialAdminPassword  </sub>
