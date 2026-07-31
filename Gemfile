source "https://rubygems.org"

gem "jekyll", "~> 4.3"

# Pull Just the Docs straight from GitHub instead of installing it as a
# gem-based theme (see remote_theme in _config.yml).
gem "jekyll-remote-theme", "~> 0.4"
gem "just-the-docs", "~> 0.10"

group :jekyll_plugins do
  gem "jekyll-include-cache", "~> 0.2" # required by just-the-docs
  gem "jekyll-relative-links", "~> 0.7" # lets [text](page.md) links work in Obsidian and on the site
  gem "jekyll-seo-tag", "~> 2.8"
  gem "jekyll-sitemap", "~> 1.4"
end

# Windows / JRuby do not include zoneinfo files.
platforms :windows, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end

# Performance booster for watching directories on Windows.
gem "wdm", "~> 0.1", platforms: [:windows]
