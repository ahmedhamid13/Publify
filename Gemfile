# frozen_string_literal: true

source "https://rubygems.org"

gem "rails", "~> 6.1.4"

gem "mysql2"
gem "pg"
gem "sqlite3", "~> 1.4.0"

# Store sessions in the database
gem "activerecord-session_store", "~> 2.0.0"

# Use Puma as the app server
gem "puma", ["~> 5.6", ">= 5.6.4"]

gem "publify_amazon_sidebar", path: "publify_amazon_sidebar"
gem "publify_core", path: "publify_core"
gem "publify_textfilter_code", path: "publify_textfilter_code"

# Use Uglifier as compressor for JavaScript assets
gem "uglifier", ">= 1.3.0"

# Needed for the lightbox and flickr text filters
gem "flickraw", "~> 0.9.8", require: false

gem "non-digest-assets", "~> 2.0"
gem "rake", "~> 13.0"
gem "reverse_markdown", "~> 2.0"

# Force newer sprockets
gem "sprockets", "~> 4.0"

# Allow throttling requests
gem "rack-attack", "~> 6.5"

group :development, :test do
  # Call 'byebug' anywhere in the code to stop execution and get a debugger console
  gem "byebug", platforms: [:mri, :mingw, :x64_mingw]

  gem "capybara", "~> 3.9"
  gem "factory_bot", "~> 6.1"
  gem "i18n-tasks", "~> 0.9.31", require: false
  gem "pry", "~> 0.14.0"
  gem "pry-rails", "~> 0.3.4"
  gem "rspec-rails", "~> 5.0"
  gem "rubocop", "~> 1.22.3", require: false
  gem "rubocop-performance", "~> 1.12.0", require: false
  gem "rubocop-rails", "~> 2.12.4", require: false
  gem "rubocop-rspec", "~> 2.6.0", require: false
  gem "simplecov", "~> 0.21.2", require: false
end

group :development do
  # Access an interactive console on exception pages or by calling 'console'
  # anywhere in the code.
  gem "web-console", "~> 4.1"

  gem "listen", "~> 3.3"
  # Display performance information such as SQL time and flame graphs for each
  # request in your browser.
  # Can be configured to work on production as well see: https://github.com/MiniProfiler/rack-mini-profiler/blob/master/README.md
  gem "rack-mini-profiler", "~> 2.0"
  # Spring speeds up development by keeping your application running in the
  # background. Read more: https://github.com/rails/spring
  gem "spring", "~> 3.0.0"
  gem "spring-commands-cucumber", "~> 1.0"
  gem "spring-commands-rspec", "~> 1.0"

  gem "fast_stack"
  gem "flamegraph"
  gem "memory_profiler"
  gem "stackprof"
end

group :test do
  gem "feedjira", "~> 3.1"
  gem "launchy", "~> 2.4"
  gem "rails-controller-testing", "~> 1.0.1"
  gem "timecop", "~> 0.9.0"
  gem "webmock", "~> 3.3"
end

# Install gems from each theme
Dir.glob(File.join(File.dirname(__FILE__), "themes", "**", "Gemfile")) do |gemfile|
  eval(File.read(gemfile), binding)
end
