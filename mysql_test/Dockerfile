FROM ubuntu:18.04
# Install MySQL.
RUN \
  apt-get update && \
  DEBIAN_FRONTEND=noninteractive apt-get install -y mysql-server && \
  rm -rf /var/lib/apt/lists/* \
  # echo "mysqld &" > /tmp/config && \
  # echo "mysqladmin --silent --wait=30 ping || exit 1" >> /tmp/config && \
  # echo "mysqladmin -u root password root" >> /tmp/config && \
  # echo "mysql -e 'GRANT ALL PRIVILEGES ON *.* TO \"root\"@\"%\" WITH GRANT OPTION;'" >> /tmp/config && \
  # sed -i 's/^\(bind-address\s.*\)/# \1/' /etc/mysql/my.cnf && \
  # sed -i 's/^\(log_error\s.*\)/# \1/' /etc/mysql/my.cnf && \
  bash /tmp/config && \
  rm -f /tmp/config

# Define mountable directories.
VOLUME ["/etc/mysql", "/var/lib/mysql"]

# Define working directory.
WORKDIR /data

# # Define default command.
# echo "mysqld &" > /tmp/config && \
# RUN service mysql start
# CMD ["mysqld"] 
# RUN mysqld &


# CMD ["service", "mysql", "start"]
# WORKDIR /data

# COPY /homemy.cnf /etc/mysql/
# Expose ports.
EXPOSE 3306 
# RUN mysqld &
# CMD ["mysqld"]
# RUN mysqladmin -u root password root

