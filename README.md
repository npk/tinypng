# TinyPNG

TinyPNG is a simple API client for TinyPNG.org, which compresses your PNG images by 50-70% while preserving full transparency.

## Installation

Add this line to your application's Gemfile:

    gem 'tinypng'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install tinypng

## Usage

Use the Ruby API in your programs:

    require 'tinypng'
    image_file = File.open(image_file_name)
    client = TinyPNG::Client.new
	image = client.shrink(image_file.read)
	image.input # => {"size"=>1234}
	image.output # => {"depth"=>8, "size"=>567, "ratio"=>0.459, "url"=>"http://tinypng.org/api/shrink/out/example.png"}
	image.to_file # => #<File:/tmp/tinypng20120910-5552-aturxh.png>

Or use the command line to shrink your images:

    tinypng mybigimage.png myshrunkenimage.png

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
