# pasword-generator

sudo apt update && sudo apt install -y argon2
echo -n "Your Master Phrase Here" | argon2 "UniqueSalt123!" -id -k 65536 -t 4 -p 2 -e | openssl base64 | tr -d '=\n' | head -c 32
