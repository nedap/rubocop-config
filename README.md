# 🚔 RuboCop-Config

RuboCop config for Healthcare.

This is explicitly for Rails projects at the moment.

## 🎯 Goal and history

RuboCop provides valuable feedback to Ruby developers, which can both improve code quality and developers' breadth of knowledge of the language. It also provides various formatting rules and is therefore a common source of holy wars and [yak shaving](https://en.wiktionary.org/wiki/yak_shaving).

We use [rubyfmt](https://github.com/fables-tales/rubyfmt) for auto-formatting, but want to make sure that RuboCop does not complain about rubyfmt-formatted code. Enter: this configuration.

Any additional rules added on top of this configuration should be well-thought-out and agreed-upon. We don't want RuboCop needlessly getting in our way, but we do want some of the advantages it can bring.

There are two rubocop configurations here: the base, `rubocop.yml`, is suited for vanilla Ruby applications or gems; `rails.yml` builds upon `rubocop.yml` and offers additional Rails-specific rules, which should be used for Rails applications.

## ✍ Contributing

Want change? Make an issue first and discuss. We will push back on rule changes unless you make a compelling case.

## 💾 Installation

1. Add to Gemfile in the development group:
```ruby
  gem "rubocop", require: false
  # gem "rubocop-rails", require: false # if you're using Rails
  gem "rubocop-rspec", require: false
```
2. Create a `.rubocop.yml` and populate it with your inherit. For a non-Rails app or gem, use:

```yml
inherit_from:
  https://raw.github.com/nedap/rubocop-config/main/rubocop.yml
```
For a Rails app, use:

```yml
inherit_from:
  https://raw.github.com/nedap/rubocop-config/main/rails.yml
```

## 👷 Maintainers

- [Platform Tribe Team 5](https://github.com/orgs/nedap/teams/platform-tribe-team-5)

## 📂 Related documents

- [RuboCop documentation](https://docs.rubocop.org/rubocop/index.html)
- [RuboCop Rails documentation](https://docs.rubocop.org/rubocop-rails/index.html)
- [RuboCop RSpec documentation](https://docs.rubocop.org/rubocop-rspec/cops_rspec.html)

## ⁉ FAQ

### Q: Why is this repository public?
No need to authenticate when using `inherit_from`. There's nothing here that needs hiding.

### Q: How do I update my cached copy?
```
rm .rubocop-https*
```
