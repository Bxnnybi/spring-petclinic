version: '3.8'

services:
  jenkins:
    image: liatrio/jenkins-alpine
    container_name: my_jenkins
    ports:
      - "8080:8080"  # Expose Jenkins on port 8080
      - "50000:50000"  # Jenkins agent port
    volumes:
      - /jenkins_home:/var/jenkins_home  # Host directory for Jenkins data
      - /var/run/docker.sock:/var/run/docker.sock  

volumes:
  jenkins_home:
    driver: local
