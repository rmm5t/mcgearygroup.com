SETTINGS = {
  :rsync_server  => "mcgearygroup.com:~/mcgearygroup.com",
  :rsync_options => "-e ssh -avz --delete --exclude=.svn --exclude=.DS_Store"
}

desc "publish to the web server"
task :publish do
  sh("rsync #{SETTINGS[:rsync_options]} ./web/ #{SETTINGS[:rsync_server]}")
end
