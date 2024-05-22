
Vagrant.configure("2") do |config|
 
  config.vm.box = "ubuntu/xenial64"
  config.vm.hostname = "servidor-examen"

  
  config.vm.provision "shell", inline: <<-SHELL
    
    sudo apt update

    echo "-- Creación de archivo.sql" > /home/vagrant/datos_pacientes.sql

    echo "create database gestion_clinica_veterinaria;" >> /home/vagrant/datos_pacientes.sql

    echo "create table pacientes(
        idPaciente int auto_increment  primary key,
        nombre varchar(25),
        especie varchar(25),
        raza varchar(25),
        edad int,
        dueno varchar(25)
        );" >> /home/vagrant/datos_pacientes.sql



  SHELL
end
