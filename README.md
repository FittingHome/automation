# automation
All Ansible's scripts necessary to update and prevent IT infrastructure anomaly

— Installation d’Ansible --- Ubuntu/Debian

Tout d’abord, rafraîchissez l’index des packages de votre système avec :

-First, refresh the package index of your system with :

    sudo apt update
    sudo apt upgrade -y

Suite à cette mise à jour, vous pouvez installer le logiciel Ansible avec :

-Following this update, you can install the Ansible software with :

    sudo apt install ansible -y

Votre nœud de contrôle Ansible dispose maintenant de tous les logiciels nécessaires pour administrer vos hôtes.

-Your Ansible control node now has all the necessary software to administer your hosts.


— Utilisatation d’Ansible --- Ubuntu/Debian

Voici une commande type permettant d'executer votre script Ansible en demandant à l'utilisateur de saisir son MDP SSH et son MDP Sudoer:

    sudo ansible-playbook -i <fichier d'inventaire> <fichier ansible> -K --ask-pass

L'arguement -i permet de specifier le fichier d'inventaire suivie de chemin d'accès au fichier.

L'argument -K permet de demander le MDP sudo.

Tandis que l'argument --ask-pass permet de demander le mot de passe de connexion au lien SSH.
