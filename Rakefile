require 'erb'

desc "Connect to development VM"
task :connect do
  sh "vagrant up"
  puts "SSHing into development VM"  
  sh "vagrant ssh"
end

desc "Run ElasticSearch & Kibana"
task :run do
  puts "Building..."
  process_erb("src/nginx.conf.erb", "etc/nginx.conf")

  puts "TODO"

  puts "Starting..."
  puts "TODO"

  puts "Console showing runtime output"
end

def process_erb(input, output)
  f = File.new(output,'w')
  f.puts(ERB.new(IO.readlines(input).to_s).result())
  f.close
end
