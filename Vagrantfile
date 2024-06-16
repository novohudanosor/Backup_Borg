
Vagrant.configure("2") do |config|
	config.vm.box="bento/ubuntu-22.04"
	config.vm.provider :virtualbox do |v|
		v.memory = 1512
		v.cpus = 2
	end
	
	boxes = [
		{	:name => "backup_server",
			:ip => "192.168.56.20",
		},
		{	:name => "client",
			:ip => "192.168.56.21",
		}
		]
		
		# provision each of the vm
	boxes.each do |opts|
		config.vm.define opts[:name] do |config|
			config.vm.network "private_network", ip: opts[:ip]
			
		end
	end
end