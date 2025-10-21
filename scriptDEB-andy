#!/bin/bash
# Script : infos_systeme.sh
# Description : Affiche la date, l’espace disque libre et l’adresse IP, puis les enregistre dans un fichier journal.

# Définir le fichier de log
LOGFILE="/var/log/infos_systeme.log"

# Créer le fichier s'il n'existe pas
touch $LOGFILE

# Récupérer les informations
DATE=$(date)
DISK=$(df -h / | tail -1 | awk '{print $4}')
IP=$(hostname -I | awk '{print $1}')

# Afficher à l’écran
echo "==========================="
echo "Date : $DATE"
echo "Espace libre : $DISK"
echo "Adresse IP : $IP"
echo "==========================="

# Sauvegarder dans le fichier log
{
  echo "==========================="
  echo "Date : $DATE"
  echo "Espace libre : $DISK"
  echo "Adresse IP : $IP"
} >> "$LOGFILE"
