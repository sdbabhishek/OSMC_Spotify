# OSMC_Spotify

Steps to Install

curl -sSL https://dtcooper.github.io/raspotify/key.asc | sudo apt-key add -v -

echo 'deb https://dtcooper.github.io/raspotify jessie main' | sudo tee /etc/apt/sources.list.d/raspotify.list

sudo apt-get update
sudo apt-get install apt-transport-https
sudo apt-get -y install raspotify



Changing quality and device name
Edit the config file:
sudo nano /etc/default/raspotify
And change bitrate to 320. This will essentially give you Ogg Vorbis -Q6 which is Spotify’s Extreme setting and hardly distinguishable from FLAC.

Afterwards, restart the service:
sudo systemctl restart raspotify

Check if it is running well:
sudo systemctl status raspotify

