Installation
=============

Add the following to your Gemfile:

``
  gem 'facebook_code_snippet'
``

Then run:

``
  bundle install
``

Example Configuration
====

In config/environments/production.rb :

```ruby
Facebook.appId = "123456" # Where 123456 is your app ID from developer.facebook.com
```

In app/views/layouts/application.html.erb:

```erb
<body>
  <%= facebook_code_snippet %>
  ...
```

Per environment config
----

facebook_code_snippet will only write out a tag if `Facebook.appId` is set. If you don't set the value in your development, testing, or staging environments, no tags will be written.

If you'd like to add them, in config/environments/{development,staging}.rb :

```ruby
Facebook.appId = "123456" # Where 123456 is your app ID from developer.facebook.com
```
