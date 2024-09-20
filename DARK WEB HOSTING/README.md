# INSTALL TOR
sudo apt install tor

# HOST WEBSITE (eg:-python)
cd [website directory] <br/>
python -m http.server --bind 127.0.0.1 8080 //any desired port

# TOR CONFIGURATION
cd /etc/tor/ <br/>
nano torrc <br/>

add lines (torrc file) >> <br/>
          HiddenServiceDir /var/lib/tor/hidden_service/ <br />
          HiddenServicePort 80 127.0.0.1:8080 //based on your website port

# START TOR
sudo systemctl start tor

# GET HOSTNAME (Onion URL)

cat /var/lib/tor/hidden_service/

# STOP TOR
sudo systemctl stop tor
            
