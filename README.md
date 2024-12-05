# Nothing Here
! [ -d /etc/apt/keyrings ] && sudo mkdir -p /etc/apt/keyrings && sudo chmod 755 /etc/apt/keyrings

wget -O- https://download.opensuse.org/repositories/home:/bgstack15:/aftermozilla/Debian_Unstable/Release.key | sudo gpg --dearmor -o /etc/apt/keyrings/home_bgstack15_aftermozilla.gpg
AIzaSyC24v-IDPNksI9RH1dMLmg2vGhtcvRDakk
sudo tee /etc/apt/sources.list.d/home_bgstack15_aftermozilla.sources << EOF > /dev/null
Types: deb
URIs: https://download.opensuse.org/repositories/home:/bgstack15:/aftermozilla/Debian_Unstable/
Suites: /
Signed-By: /etc/apt/keyrings/home_bgstack15_aftermozilla.gpg
EOF

sudo apt update

sudo apt install librewolf -y
