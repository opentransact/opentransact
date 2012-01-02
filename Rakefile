task :default => ['opentransact.txt', 'opentransact.html', 'opentransact.pdf', 'opentransact.epub']

file 'opentransact.xml' => 'opentransact.md' do |t|
  puts "generating opentransact.xml"
  `bundle exec kramdown-rfc2629 #{ t.prerequisites[0] }> #{ t.name }`
end

file 'opentransact.txt' => 'opentransact.xml' do |t|
  puts "generating opentransact.txt"
  download_rfc(t.name, "unpg/ascii")
end

file 'opentransact.html' => 'opentransact.xml' do |t|
  puts "generating opentransact.html"
  download_rfc(t.name, "html/ascii")
end

file 'opentransact.pdf' => 'opentransact.xml' do |t|
  puts "generating opentransact.pdf"
  download_rfc(t.name, "html/pdf")
end

file 'opentransact.epub' => 'opentransact.xml' do |t|
  puts "generating opentransact.epub"
  download_rfc(t.name, "html/epub")
end


def download_rfc(output, format)
  `curl http://xml.resource.org/cgi-bin/xml2rfc.cgi -F input=@opentransact.xml -F "modeAsFormat=#{format}" -F checking=fast -o #{output}`
end