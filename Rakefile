# encoding: UTF-8
require 'rake'

desc "Kompileeri töö"
task :compile do
  puts "Kompileerin töö"
  `pdflatex thesis.tex`
  
  puts "Genereerin viited"
  `bibtex thesis`
  
  puts "Genereerin sõnastiku"
  `makeglossaries thesis`
 
  puts "Kompileerin töö koos viidete ja sõnastikuga uuesti"
  `pdflatex thesis.tex`
end

desc "Puhasta kataloog ajutistest failidest"
task :clean do

  # Defineerime failid, mida ei tohi kustutada
  source_files = ['LICENSE', 'Rakefile', 'Readme.md', 'acknowledgements.tex',
                  'glossary.tex', 'figures', 'introduction.tex',
                  'library.bib', 'methods.tex', 'overview.tex', 'results.tex',
                  'summary.tex', 'summary_en.tex', 'supplementary1.tex',
                  'thesis.tex', 'title.tex', '.gitignore', '.git', '.', '..']
  
  # Käime läbi kõik kataloogis olevad failid
  Dir.foreach(Dir.pwd) do |file|
    if not source_files.include? file
      # Kui ei ole oluliste failide nimekirjas, kustutame
      File.delete file
    end
  end

end

# Kompileerime ja avame PDFi (töötab OS X-is)
desc "Ava töö"
task :open do
  Rake::Task['compile'].execute
  `open thesis.pdf`
end

# Kiire kompileerimine juhul, kui viited/sõnastik pole muutunud
desc "Kompileeri töö"
task :fast do
  puts "Kompileerin töö"
  `pdflatex thesis.tex`
  `open thesis.pdf`
end