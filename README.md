#=======================================================================#
#                             IOA31000                                  #
# Script  : beef_strike                                                 #
# Date    : 08/09/2017                                                  #
# Author  : Tito                                                        #
# Version : v0.2                                                        #
# License : GNU General Public License v3.0                             #
# Distrib : Kali-Linux amd64                                            #
# Session : root                                                        #
# Site Web: https://www.ioa31000.com	        		                #
# YouTube : https://www.youtube.com/user/IOA32000/playlists             #
# Github  : https://github.com/IOA31000?tab=repositories                #
#                                                                       #
#=======================================================================#


# Caractéristiques

Intergre le plugin beef_strike dans armitage
    

# Exigences

    Avoir installé hpricot
    Avoir installé json

# Installation

    Rendez-vous dans le dossier /etc/beef-xss
    Ouvrez le fichier config.yaml
    Descendez a la ligne 156
    Modifiez comme ceci :

    metasploit:
            enable: true

    Rendez-vous dans le dossier /usr/share/beef-xss/extensions/metasploit
    Ouvrez le fichier config.yaml
    Descendez a la ligne 18
    Modifiez l'IP par la votre
    Descendez a la ligne 28
    Modifiez l'IP par la votre
    Dezippez le dossier beef_msf_armitage
    Deplacez le dossier beef_strike vers /root
    Deplacez le dossier beef vers /usr/share/metasploit-framework/lib
    Deplacez beef.rb vers /usr/share/metasploit-framework/plugins
    
    Ouvrez un terminal et tapez :
    
    gem install hpricot
    gem install json
    
    Rendez-vous dans le dossier /var/lib/gems/2.3.0/gems/hpricot-0.8.6/lib
    Copiez l'integralite du contenu
    Rendre-vous dans le dossier /usr/lib/ruby/vendor_ruby
    Coller l'integralite precedement copier

    Ouvrez un terminal et tapez :

    msfconsole
    load beef
    load msgrpc ServerHost=127.0.0.1 Pass=abc123

    Ouvrez un autre terminal terminal et tapez :
    
    cd /usr/share/beef-xss
    ./beef

    Ouvrez armitage
    Rendez-vous dans Armitage/script/load/beef_strike
    Selectionnez beef_strike.cna
    Render-vous dans attacks/beef strike/start/connect
    Renseignez les informations de connection comme ceci :
    
    http://votre IP:3000
    beef
    beef
    
    Render-vous dans attacks/beef strike/start/key
    Renseignez votre clef API (situer dans le panneau beef strike de armitage)    
    Render-vous dans attacks/beef strike/auto import/ON
    
    A partir de maintenant chaque nouvelle victime online de beef apparaitra dans armitage


# Mise a jour

    Lien de mise a jour dans le fichier source.txt
