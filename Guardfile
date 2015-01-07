# See http://asciidoctor.org/docs/editing-asciidoc-with-live-preview/ for how
# to use this file.

require 'asciidoctor'
require 'erb'

guard 'shell' do
  watch(/^.*\.asciidoc$/) {|m|
    Asciidoctor.convert_file(m[0], :in_place => true, :safe => 'unsafe')
  }
end

guard 'livereload' do
  watch(%r{^.+\.(css|js|html)$})
end
