servers = [
  {
    name: "myappserver",
    ip: "192.168.5.50"
  },
  {
    name: "mydbserver",
    ip: "192.168.5.51"
  }
]
  

Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"
  config.vm.provider "virtualbox"
  
  servers.each do |server|
    config.vm.define server[:name] do |env|
      env.vm.hostname = server[:name]
      env.vm.network "private_network", ip: server[:ip]
    end
  end
end
