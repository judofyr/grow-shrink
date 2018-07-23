require 'asciidoctor'

task :default => :build


file 'index.html' => 'README.adoc' do |t|
  Asciidoctor.convert_file(t.source,
    to_file: t.name,
    mkdirs: true,
    attributes: { 'source_highlighter' => 'coderay', 'linkcss' => false }
  )
end

task :build => 'index.html'

