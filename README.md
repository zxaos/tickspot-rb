# Tickspot-rb

[![Code Climate](https://codeclimate.com/github/cmason/tickspot-rb.png)](https://codeclimate.com/github/cmason/tickspot-rb)
[![Build Status](https://travis-ci.org/cmason/tickspot-rb.png?branch=master)](https://travis-ci.org/cmason/tickspot-rb)
[![Gem Version](https://badge.fury.io/rb/tickspot-rb.png)](http://badge.fury.io/rb/tickspot-rb)

Ruby wrapper for the [Tick API](http://www.tickspot.com/api/).

## Installation

    $ gem install tickspot-rb

## Bundler

    gem "tickspot-rb", :require => 'tickspot'

## Example Usage

    require 'tickspot'

    tick = Tickspot::Client.new('myCompanyName', 'myemail@example.com', 'myTickPassword')
    tick.clients

    => [{"id"=>123, "name"=>"Acme"}, {"id"=>231, "name"=>"Sterling Cooper"}, {"id"=>321, "name"=>"Justice League"}]

You can also initialize the client with a configuration block:

    # config/initializers/tickspot.rb (for instance)
    Tickspot.configure do |config|
      config.company = 'acme'
      config.email = 'wilie@acme.com'
      config.password = 'secret'
    end

    # elsewhere
    client = Tickspot::Client.new

## Note on Patches/Pull Requests

* Fork the project.
* Make your feature addition or bug fix.
* Add tests for it. This is important so I don't break it in a
  future version unintentionally.
* Commit, do not mess with rakefile, version, or history.
  (if you want to have your own version, that is fine but
   bump version in a commit by itself I can ignore when I pull)
* Send me a pull request. Bonus points for topic branches.

## Copyright

Copyright (c) 2012 Chris Mason. See [LICENSE](LICENSE) for details.
