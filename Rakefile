require 'bundler/setup'

Bundler.require

task :default do
  server = Adsf::Server.new(root: 'public')

  %w[INT TERM].each do |s|
    Signal.trap(s) { server.stop }
  end

  server.run
end
