# INSTALL TOR
sudo apt install tor

# HOST WEBSITE (eg:-python)
python -m http.server --bind 127.0.0.1 8080 //any desired port

# TOR CONFIGURATION
cd /etc/tor/
nano torrc

add lines (torrc file) >>
          HiddenServiceDir /var/lib/tor/hidden_service/
          HiddenServicePort 80 127.0.0.1:8080 //based on your website port

# START TOR
sudo systemctl start tor

# GET HOSTNAME (Onion URL)

cat /var/lib/tor/hidden_service/

# STOP TOR
sudo systemctl stop tor
            
