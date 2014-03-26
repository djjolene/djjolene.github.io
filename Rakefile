require 'haml'
require 'sass'

task default: [:build]
task build: [:css, :html]

task :html do
  File.open("index.html", "w") do |f|
    f.write(Haml::Engine.new(IO.read("index.html.haml")).render)
  end
end

task :css do
  File.open("site.css", "w") do |f|
    f.write(Sass::Engine.new(IO.read("site.css.scss"),
      syntax: :scss, style: :compressed).render)
  end
end