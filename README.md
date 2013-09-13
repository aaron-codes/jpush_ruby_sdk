# JpushRubySdk

目前仅仅实现了 **推送全功能接口**, 注意：此gem正在完善中，欢迎发PR。

## Installation

Add this line to your application's Gemfile:

    gem 'jpush_ruby_sdk'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install jpush_ruby_sdk

## Usage

* 推送全功能接口

```ruby

jpush_client = JpushRubySdk::Client.new(app_key, master_secret)

receiver = Hash[:receiver_type => "4", :receiver_value => ""]

msg_content = MultiJson.dump(Hash[:n_content=> "test gogograd haha"])
msg = Hash[:msg_type => "1", :msg_content => msg_content, :platform => "ios"]

jpush_client.pushNotification("3322",receiver, msg, {})


```

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
