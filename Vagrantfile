VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
    # Use the same key for each machine
    config.ssh.insert_key = false

    config.vm.define "vagrant1" do |vagrant1|
        vagrant1.vm.box = "centos/7"
        vagrant1.vm.network "forwarded_port", guest: 80, host: 8880
        vagrant1.vm.network "forwarded_port", guest: 443, host: 8443
    end

    config.vm.define "vagrant2" do |vagrant2|
        vagrant2.vm.box = "centos/7"
        vagrant2.vm.network "forwarded_port", guest: 80, host: 8881
        vagrant2.vm.network "forwarded_port", guest: 443, host: 8444
    end

    config.vm.define "vagrant3" do |vagrant3|
        vagrant3.vm.box = "centos/7"
        vagrant3.vm.network "forwarded_port", guest: 80, host: 8882
        vagrant3.vm.network "forwarded_port", guest: 443, host: 8445
    end
end