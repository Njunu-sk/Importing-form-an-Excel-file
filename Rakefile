require 'roo'
require_relative './product.rb'

namespace :import do
  desc "Import data from spreadsheet"
  task :data do
    puts 'Importing Data'
    data = Roo::Spreadsheet.open('lib/products.xlsx')
    headers = data.row(1)
    data.each_with_index do |row, index|
      next if index == 0

      product_data = Hash[[headers, row].transpose]
      name = product_data.values[0]
      amount = product_data.values[1]

      product = Product.new(name, amount)

      p product
    end
  end
end


# Resource - https://echobind.com/post/ruby-on-rails-importing-data-from-an-excel-file
