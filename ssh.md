1. https://linuxhint.com/generate-ssh-key-ubuntu/
2. On local , check ssh id_rsa existed : ls -l ~/.ssh/id_*.pub
3. If not existing  then create it : ssh-keygen -t rsa -b 4096 -C "samreena_email@yahoo.com"
4. copy to server :
  4.1 : use ssh copy id : ssh-copy-id user_name@server_IPaddress
  4.2 : If not work : use copy content like this:
    cat ~/.ssh/id_rsa.pub | ssh user_name@server_ipaddress "mkdir -p ~/.ssh && chmod 700 ~/.ssh && cat >> ~/.ssh/authorized_keys && chmod 600 ~/.ssh/authorized_keys"
