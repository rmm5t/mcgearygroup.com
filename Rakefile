require 'cgi'

# SETTINGS = {
#   :rsync_server  => "mcgearygroup.com:~/mcgearygroup.com",
#   :rsync_options => "-e ssh -avz --delete --exclude=.DS_Store"
# }

# desc "publish to the web server"
# task :publish do
#   sh("rsync #{SETTINGS[:rsync_options]} ./ #{SETTINGS[:rsync_server]}")
# end

desc "Ping relevant services after new content is published."
task :ping do
  ping "http://www.google.com/webmasters/sitemaps/ping?sitemap=#{CGI.escape "http://mcgearygroup.com/sitemap.xml"}"
end

def ping(url)
  require 'open-uri'
  print "\nPinging #{url[0..70]}... "
  io = URI.parse(url).open
  puts io.status[0]
end
