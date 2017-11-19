#=======================================================================#
#                             IOA31000                                  #
# Script  : beef_strike                             		        #
# Date    : 16/11/2017                                                  #
# Author  : Tito                                                        #
# Version : v0.1                                                        #
# License : GNU General Public License v3.0                             #
# Distrib : Kali-Linux 2017.2 amd64                                     #
# Session : root  			      	               		#
# Site Web: https://www.ioa31000.com	                	        #
# YouTube : https://www.youtube.com/user/IOA32000/playlists             #
# Discord : https://discordapp.com/invite/cyBjPjN                       #
#                                                                       #
#=======================================================================#


# Caractéristiques

Integration de beef strike pour armitage et msf 

# Installation

Copier/Coller dans un terminal :

DANS LE FICHIER QUI VAS S'OUVRIR MODIFIER LA LIGNE 156 COMME CECI :

			metasploit:
			        enable: true
		        
DANS LE FICHIER /etc/beef-xss/config.yam MODIFIER VOTRE ID ET MDP BEEF A LA LIGNE 113 ET 114
		
			sed -i 's/localhost/127.0.0.1/g' /usr/share/beef-xss/extensions/metasploit/config.yaml
			sed -i 's/auto_msfrpcd: false/auto_msfrpcd: true/g' /usr/share/beef-xss/extensions/metasploit/config.yaml
			apt update
			git clone https://github.com/IOA31000/beef_strike.git /root/Desktop/beef_strike
			mv -f /root/Desktop/beef_strike/beef_strike /root/
			mv -f /root/Desktop/beef_strike/beef /usr/share/metasploit-framework/lib
			mv -f /root/Desktop/beef_strike/beef.rb /usr/share/metasploit-framework/plugins
			rm -rf /root/Desktop/beef_strike
			gem install hpricot json
			cp -r /var/lib/gems/2.3.0/gems/hpricot-0.8.6/lib/* /usr/lib/ruby/vendor_ruby
			rm -f /usr/bin/beef-xss

DANS LE FICHIER /etc/beef-xss/config.yaml MODIFIER LE PORT A LA LIGNE 58 COMME CECI :
(VOUS POUVEZ MODIFIER VOTRE ID ET MDP BEEF A LA LIGNE 59 ET 60)

		        http://127.0.0.1:3000
      
			echo "cd /usr/share/beef-xss" >> /usr/bin/beef-xss
			echo "./beef" >> /usr/bin/beef-xss
			chmod +x /usr/bin/beef-xss
			git clone https://github.com/IOA31000/redirect_beef.git /root/Desktop/redirect_beef
			mv -f /root/Desktop/redirect_beef/index.html /var/www/html
			rm -rf /root/Desktop/redirect_beef
			msfdb init
			
Ouvrez armitage

Rendez-vous dans Armitage/script/load/beef_strike

Selectionnez beef_strike.cna
Render-vous dans attacks/beef strike/start/connect
Renseignez les informations de connection comme ceci :
http://votre IP:3000
Votre ID (default = beef)
Votre MDP (default = beef)
Render-vous dans attacks/beef strike/start/key
Renseignez votre clef API (situer dans le panneau beef strike de armitage)
Render-vous dans attacks/beef strike/auto import/ON
A partir de maintenant chaque nouvelle victime online de beef apparaitra dans armitage
