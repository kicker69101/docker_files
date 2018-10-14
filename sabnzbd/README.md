# Setup
This doc assumes you have some basic knowledge of sabnzbd, sonarr, radarr, and/or google

Here are the steps to setup
1. Create a local user that will link all these together
2. Create a place to store your media and configs
  * In this file I use /opt/data/tv for tv shows
  * /opt/data/movies for movies
  * I allow store all the configs in /opt for each container, with /opt/downloads being centerized for all three containers
  * you might want to adjust this based on your setup.
3. Run: docker-compose up -d and assuming no errors you can move forward
4. Log into sabnzbd by going to <ip for server>:8080
  * First thing you want to do is enable https, then use port 9090 going forward
  * Configure usenet
  * Get the api key
5. Log into sonarr(port 8989) and radarr(port 7878), then configure them to use the sabnzbd container.
  * Since this containers will be on one network, you can just refer sabnzbd as the hostname. Docker will handle the hosts file for this
6. Configure your indexer for both sonarr and radarr.
7. Enjoy the downloads fly.
