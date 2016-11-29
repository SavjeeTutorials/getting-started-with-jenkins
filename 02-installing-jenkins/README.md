# Installing Jenkins on Ubuntu Server 15.10 or 16.10

Commands used in my video "[Installing Jenkins on Ubuntu Server](https://www.youtube.com/watch?v=AXlN-f6Uk64&list=PLzvRQMJ9HDiSaisKr7OnM4Fl7JXCDDcmt&index=2)".

```bash
# Download the security key for the Jenkins repository & add it to the keychain
wget -q -O - https://jenkins-ci.org/debian/jenkins-ci.org.key | sudo apt-key add -

# Add the Jenkins sources to apt
sudo sh -c 'echo deb http://pkg.jenkins-ci.org/debian binary/ > /etc/apt/sources.list.d/jenkins.list'

# Update the list of packages
sudo apt-get update

# Install Jenkins (will also install its dependencies, eg OpenJDK)
sudo apt-get install jenkins
```

This should work in any version of Ubuntu Server and Debian.