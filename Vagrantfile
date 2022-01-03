Vagrant.configure("2") do |config|
    config.vm.define "remnux" do |remnux|
        remnux.vm.provider "virtualbox" do |vb|
            vb.name = "LAB-REMNux"
            vb.cpus = 2
            vb.memory = 2048
            vb.gui = true
            vb.check_guest_additions = false
        end
        remnux.vm.box = "local/remnux"
        remnux.vm.box_check_update = false
        remnux.vm.hostname = "remnux.local"
        remnux.vm.network "private_network", type: "dhcp"

    end

    config.vm.define "flarevm" do |flarevm|
        flarevm.vm.provider "virtualbox" do |vb|
            vb.name = "LAB-FlareVM"
            vb.cpus = 2
            vb.memory = 2048
            vb.gui = true
            vb.check_guest_additions = false
        end
        flarevm.vm.communicator = "winrm"
        flarevm.vm.boot_timeout = 600
        flarevm.vm.graceful_halt_timeout = 600
        flarevm.vm.guest = "windows"
        flarevm.vm.box = "local/flarevm"
        flarevm.vm.box_check_update = false
        flarevm.vm.hostname = "flarevm"
        flarevm.vm.network "private_network", type: "dhcp"
    end
end