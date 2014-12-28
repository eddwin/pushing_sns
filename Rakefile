require './app'
require_relative 'model/notification.rb'

namespace :db do
  desc "Create Table"
  task :migrate do
    begin
      Notification.create_table(5,6)
      puts "New table created"
    rescue AWS::DynamoDB::Errors::ResourceInUseException => e
      puts "Table already exists, no changes made, no retry attempted"
    end
  end
end
