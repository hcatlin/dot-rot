DOTROT_HOME = File.dirname(__FILE__)

def symlink_dotfile(name)
  print "symlinking #{name}... "
  FileUtils.ln_s File.join(DOTROT_HOME, "dot.#{name}"), "#{ENV['HOME']}/.#{name}", :force => true
  puts 'done!'
end

desc "Install dotfiles"
task :install do
  symlink_dotfile "bash_profile"
  symlink_dotfile "gitconfig"
  symlink_dotfile "gemrc"
  puts ""
  puts "Now run this command to reload the shell:"
  puts ""
  puts "  source ~/.bash_profile"
  puts ""
end