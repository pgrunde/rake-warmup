namespace :greeting do
  desc "Say howdy"
  task :howdy do
    puts "Howdy partner"
  end

  desc "Print a nice greeting"
  task :greet do
    puts "Hello there"
  end
end

task :default do
  puts "DOUBLE DOWN"
end

desc "Prints current time"
task :time_now do
  puts Time.new
end

desc "Prints favorite food env var"
task :print_favorite_food do
  puts ENV["FAVORITE_FOOD"]
end

task :wake_up do
  puts "You wake up."
end

task :get_dressed => :wake_up do
  puts "You put on clothes."
end

task :eat_breakfast => :get_dressed do
  puts "You eat breakfast."
end

task :brush_teeth => :eat_breakfast do
  puts "You brush your teeth."
end

task :ready_for_class => :brush_teeth do
  puts "You are now prepared for class."
end

# If your tasks require arguments:
#
# namespace :my_tasks do
#   task :foo, :arg1, :arg2 do |t, args|
#     do_something
#   end
#
#   task :bar, :arg1, :arg2  do |t, args|
#     do_something_else
#   end
#
# end
#
# task :my_tasks, :arg1, :arg2 do |t, args|
#   Rake::Task["my_tasks:foo"].invoke( args.arg1, args.arg2 )
#   Rake::Task["my_tasks:bar"].invoke( args.arg1, args.arg2 )
# end