task :default => ['opentransact.txt', 'opentransact.html']

file 'opentransact.xml' => 'opentransact.md' do |t|
  puts "generating opentransact.xml"
  `bundle exec kramdown-rfc2629 #{ t.prerequisites[0] }> #{ t.name }`
end

file 'opentransact.txt' => 'opentransact.xml' do |t|
  puts "generating opentransact.txt"
  `xml2rfc #{t.prerequisites[0]}`
end

file 'opentransact.html' => 'opentransact.xml' do |t|
  puts "generating opentransact.html"
  `curl http://xml.resource.org/cgi-bin/xml2rfc.cgi -F input=@#{t.prerequisites[0]} -F "modeAsFormat=html/ascii" -F checking=fast -o #{t.name}`
end