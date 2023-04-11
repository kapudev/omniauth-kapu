# OmniAuth Kapu

This gem contains the KapuID strategy for OmniAuth.

## Before You Begin

You should have already installed OmniAuth into your app; if not, read the [OmniAuth README](https://github.com/omniauth/omniauth) to get started.

Now sign in into the [KapuID developer area](https://id.bykapu.com/apps) and create an application. Take note of your APP_ID and APP Secret because that is what your web application will use to authenticate against the Kapu API. Make sure to set a callback URL or else you may get authentication errors. (It doesn't matter what it is, just that it is set.)

## Using This Strategy

First start by adding this gem to your Gemfile:

```ruby
gem 'omniauth-kapu'
```

If you need to use the latest HEAD version, you can do so with:

```ruby
gem 'omniauth-kapu', :github => 'earlbalai/omniauth-kapu'
```

Next, tell OmniAuth about this provider. For a Rails app, your `config/initializers/omniauth.rb` file should look like this:

```ruby
Rails.application.config.middleware.use OmniAuth::Builder do
  provider :twitter, "API_KEY", "API_SECRET"
end
```

Replace `"KAPU_APP_ID"` and `"Kapu_APP_SECRET"` with the appropriate values you obtained [earlier](https://id.bykapu.com/apps).
