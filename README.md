# Fritzbox::Smarthome

Ruby client library to interface with Smarthome features of your FritzBox.

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'fritzbox-smarthome'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install fritzbox-smarthome

## Usage

```ruby
Fritzbox::Smarthome.configure do |config|
  config.endpoint   = 'https://fritz.box'
  config.username   = 'smarthome'
  config.password   = 'verysmart'
  config.verify_ssl = false
end

actors = Fritzbox::Smarthome::Actor.all

actor = actors.last
actor.update_hkr_temp_set(BigDecimal.new('21.5'))
```

## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `rake spec` to run the tests. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/klausmeyer/fritzbox-smarthome.

## License

The gem is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).
