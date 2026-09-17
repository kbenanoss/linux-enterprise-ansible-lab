Vagrant.configure("2") do |config|
  config.vm.box = "generic/centos9s"

  machines = {
    "control" => {
      ip: "192.168.56.20",
      memory: 1536
    },
    "linux01" => {
      ip: "192.168.56.21",
      memory: 1024
    },
    "linux02" => {
      ip: "192.168.56.22",
      memory: 1024
    }
  }

  machines.each do |name, settings|
    config.vm.define name do |machine|
      machine.vm.hostname = name

      machine.vm.network "private_network",
        ip: settings[:ip]

      machine.vm.provider "virtualbox" do |vb|
        vb.name = "enterprise-#{name}"
        vb.memory = settings[:memory]
        vb.cpus = 1
      end
    end
  end
end
