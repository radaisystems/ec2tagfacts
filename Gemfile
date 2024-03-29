source ENV['GEM_SOURCE'] || "https://rubygems.org"

group :test do
  gem "rake", ">= 12.3.3"
  gem "puppet", ENV['PUPPET_GEM_VERSION'] || '~> 4.2.3'
  gem "rspec", '< 3.2.0'
  gem "rspec-puppet"
  gem "puppetlabs_spec_helper"
  if RUBY_VERSION < '2.0.0'
    gem 'metadata-json-lint', '1.0.0'
  else
    gem "metadata-json-lint"
  end
  gem "rspec-puppet-facts"

  if RUBY_VERSION < '2.0.0'
    gem 'rubocop', '< 0.49.0'
  else
    gem "rubocop"
  end

  gem 'simplecov', '>= 0.11.0'
  gem 'simplecov-console', '< 0.4.2' 

  gem "puppet-lint-absolute_classname-check"
  gem "puppet-lint-leading_zero-check"
  gem "puppet-lint-trailing_comma-check"
  gem "puppet-lint-version_comparison-check"
  gem "puppet-lint-classes_and_types_beginning_with_digits-check"
  gem "puppet-lint-unquoted_string-check"
  gem 'puppet-lint-resource_reference_syntax'

  gem 'json_pure', '<= 2.0.1' if RUBY_VERSION < '2.0.0'
end

group :development do
  gem "travis"              if RUBY_VERSION >= '2.1.0'
  gem "travis-lint"         if RUBY_VERSION >= '2.1.0'
  gem "puppet-blacksmith"
  gem "guard-rake" if RUBY_VERSION >= '2.2.5' # per dependency https://rubygems.org/gems/ruby_dep
end

group :system_tests do
  gem "beaker", '< 3.0.0'
  gem "beaker-rspec"
  gem "beaker-puppet_install_helper"
end
