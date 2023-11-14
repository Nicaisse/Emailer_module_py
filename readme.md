Module Emailer
Le module Emailer est une bibliothèque Python simple et légère conçue pour faciliter l'envoi d'e-mails via SMTP. Son objectif est de simplifier le processus d'envoi d'e-mails en fournissant une configuration rapide et une interface conviviale.

Configuration du Serveur
Avant d'utiliser les fonctionnalités d'envoi d'e-mails, il est impératif de configurer le serveur SMTP en utilisant la méthode configurer_emailer. Cette méthode prend en charge les paramètres essentiels tels que l'adresse du serveur, le port, l'adresse e-mail de l'expéditeur et le mot de passe.

Exemple de configuration du serveur :
# Configurer le serveur
from emailer import setup_email_email, send_email
serveur_config = setup_email_email(
    serveur="smtp.example.com",
    port=587,
    sender_email="votre_email@example.com",
    password="motdepasse"    #mot de passe generer a partir de botre compte gmail
)
Envoi d'E-mails
Une fois le serveur configuré, vous pouvez utiliser la méthode send_email pour envoyer des e-mails. Assurez-vous que le serveur a été configuré avec succès avant d'appeler cette méthode.

Exemple d'envoi d'e-mail :


try:
    send_email(
        destinataire="destinataire@example.com",
        sujet="Sujet de l'e-mail",
        corps="Corps de l'e-mail",
        server=serveur_config
    )
except :
    print(f"Erreur : {e}")
