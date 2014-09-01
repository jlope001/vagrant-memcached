# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

ENV['VAGRANT_DEFAULT_PROVIDER'] ||= 'docker'

# we require defaults
if ! ENV.has_key?("MEMCACHED_SETUP")
  puts 'required environment variables not setup, please source defaults'
  exit 1
end

# setup environment variables
env_config = {}
ENV.each do |k, v|
  if k.match(/^MEMCACHED/)
    env_config[k] = v
  end
end

Vagrant.configure("2") do |config|
  config.vm.define "memcached" do |v|
    v.vm.provider "docker" do |d|
      d.build_dir = "./memcached"
      d.name = "memcached"
      d.env = env_config
    end
  end
end
