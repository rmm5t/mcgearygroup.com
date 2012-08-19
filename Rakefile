SETTINGS = {
  :rsync_server  => "mcgearygroup.com:~/mcgearygroup.com",
  :rsync_options => "-e ssh -avz --delete --exclude=.DS_Store"
}

desc "publish to the web server"
task :publish do
  sh("rsync #{SETTINGS[:rsync_options]} ./public/ #{SETTINGS[:rsync_server]}")
end
