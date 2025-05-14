# Crypto_messagerie
Une messagerie chiffré, création user, message chiffré, lecture message 

-----------------------------------------------------------------
#commande pour read message: 
#option 3
#messages/xxxxxxxxxx.enc
-----------------------------------------------------------------
#commandes manuel pas passer pas menu.py

# 1. Placez-vous à la racine du projet
cd messagerie_secure_release

# 2. (Re)créez Alice et Bob
./scripts/create_user.sh alice
./scripts/create_user.sh bob

# 3. Envoyez un message d'Alice vers Bob
./scripts/send_message.sh alice bob
# → Tapez votre message, puis Ctrl-D. 
#   Vous verrez un nouveau fichier .enc dans messages/.

# 4. Listez pour récupérer le nom exact
ls messages/*.enc
# ex. messages/msg-alice-to-bob-20250514153000.enc

# 5. Bob lit et vérifie le message
./scripts/read_message.sh bob alice messages/msg-alice-to-bob-20250514153000.enc

