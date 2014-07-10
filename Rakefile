task :default do |t|
	exec "bundle exec jekyll"
end

task :new do |t|
	puts "Enter title"
	title = STDIN.gets.chomp
	safetitle = title.gsub " ", "-"
	safetitle.gsub! /[^A-Za-z0-9-]/, ""
	safetitle.downcase!
	date = Time.now.strftime "%Y-%m-%d"
	filename = "#{date}-#{safetitle}.md"
	content = "---
layout: post
title: \"#{title}\"
---
"
	File.open "_posts/#{filename}", "w" do |f|
		f.write content
	end
end