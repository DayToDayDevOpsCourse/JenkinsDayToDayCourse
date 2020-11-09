*JenkinsSetup*: https://www.jenkins.io/doc/book/installing/linux/#debianubuntu

**Install Java**:

    #Update the repositories
    sudo apt update
    
    #search of all available packages
    sudo apt search openjdk
    
    #Pick one option and install it
    sudo apt install openjdk-8-jdk -y
    
        If you see any similar message as below follow below steps to solve the issue
        
        Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3327 (apt)... 37s
        
        check the running process: ps aux | grep -i apt
        
        Run the command: sudo kill <processId>

    #check the installation
    java -version
    
**Install Jenkins**:

    wget -q -O - https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo apt-key add -
    sudo sh -c 'echo deb https://pkg.jenkins.io/debian-stable binary/ > \
        /etc/apt/sources.list.d/jenkins.list'
    sudo apt-get update
    sudo apt-get install jenkins -y
    
    
    
