# Usa Ubuntu 22.10 como base
FROM ubuntu:22.10

# Actualiza los repositorios e instala el cliente y servidor OpenSSH
RUN apt-get update && apt-get install -y openssh-client openssh-server

# Crea el usuario "prueba" con la contraseña "prueba"
RUN useradd -m -s /bin/bash prueba && echo "prueba:prueba" | chpasswd

# Expone el puerto 22 para SSH
EXPOSE 22

# Inicia el servidor SSH
CMD ["/usr/sbin/sshd", "-D"]
