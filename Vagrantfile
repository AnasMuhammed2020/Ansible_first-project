Vagrant.configure("2") do |config|
        config.vm.box = 'centos/7'
	config.vm.provider :virtualbox do |v|
		v.memory = 512
        end
       
 	config.vm.define "master" do |master|
		master.vm.hostname = "ansible-master"
		master.vm.network :private_network, ip: "192.168.50.20"
 	end
config.vm.define "web" do |web|
		web.vm.hostname = "web"
		web.vm.network :private_network, ip: "192.168.50.21"
		web.vm.network "forwarded_port", guest:80, host:8090
 	end
config.vm.define "app" do |app|
		app.vm.hostname = "app"
		app.vm.network :private_network, ip: "192.168.50.22"
 	end
config.vm.define "db" do |db|
		db.vm.hostname = "db"
		db.vm.network :private_network, ip: "192.168.50.23"
 	end

end
