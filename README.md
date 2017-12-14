# Tools, tools everywhere

This is a list of resources and notes provided as companion material for the session [“Tools, tools everywhere”](http://hamburg.onruby.de/topics/tools-tools-everywhere-571), delivered at:

- [Ruby User Group Hamburg](http://hamburg.onruby.de/) (12-13-2017).

__Note:__ _WIP_ (“work in progress”): this repository is expected to receive relevant content updates during next weeks. Stay tuned ;)

## Resources

### Books

- [eXtreme Programming explained: embrace change](https://www.amazon.com/Extreme-Programming-Explained-Embrace-Change/dp/0321278658), by Kent Beck.
- [The Pragmatic Programmer: From Journeyman to Master](https://www.amazon.com/Pragmatic-Programmer-Journeyman-Master/dp/020161622X), by Andrew Hunt and David Thomas.
- [Book: Apprenticeship Patterns: Guidance for the Aspiring Software Craftsman, 2009](https://www.amazon.de/Apprenticeship-Patterns-Guidance-Aspiring-Craftsman/dp/0596518382) by Dave Hoover and Adewale Oshineye.
- [99 bottles of OOP](https://www.sandimetz.com/99bottles/), by Sandi Metz & Katrina Owen.

### Other resources

- (Web) [eXtreme Programming](http://extremeprogramming.org)
- (Article) [Deciphering Ruby Code Metrics](https://codeclimate.com/blog/deciphering-ruby-code-metrics/)
- (Talk) [Perusing the Rails Source Code - A Beginners Guide](https://www.youtube.com/watch?v=Q_MpGRfnY5s), by Alex Kitchens @ RailsConf 2017.
- (Talk) [Rules](https://youtu.be/npOGOmkxuio), by Sandi Metz @ Baruco 2013

## Notes on tools

### RuboCop

> “A Ruby static code analyzer, based on the community Ruby style guide.”

- Common (team/company wide) master file. Tweaks proposed with pull requests.
- Automatically fixing offenses: `--auto-correct`.
- Integrating in legacy codebases: `--auto-gen-config`.
- Excluding concrete cops: per line / per file.
- Rails-specific support.
- Integrable with development workflows (local, CI...).

To learn more:

- https://github.com/bbatsov/rubocop
- Annotated default config. file: https://github.com/bbatsov/rubocop/blob/master/config/default.yml

Ruby & Rails style guides:

- https://github.com/bbatsov/ruby-style-guide
- https://github.com/bbatsov/rails-style-guide

### Flog

> “Flog reports the most tortured code in an easy to read pain report. The higher the score, the more pain the code is in.”

- `--group`: “group and sort by class.”
- `--all`: “display all flog results, not top 60%.”
- `--extended`: “put file:line on a separate line (for rubymine & friends).”

To learn more:

- https://github.com/seattlerb/flog
- http://ruby.sadi.st/Flog.html

### Reek

> “Code smell detector for Ruby”

- `--sort-by-issue-count`: “sort by "issue-count", listing the "smelliest" files first.”
- `--single-line`: “show IDE-compatible single-line-per-warning.”
- Rails-specific configuration: https://github.com/troessner/reek#working-with-rails

To learn more:

- https://github.com/troessner/reek (README includes links to blog posts and talk)
- https://github.com/troessner/reek/blob/master/docs/Code-Smells.md
- [“Reek Driven Development”](https://github.com/troessner/reek/blob/master/docs/Reek-Driven-Development.md)


### Brakeman

> “A static analysis security vulnerability scanner for Ruby on Rails applications”.

- `--checks`: “list all available vulnerability checks.”
- `--run-all-checks`: “run all default and optional checks.”
- `--rails3`, `--rails4`, `--rails5`: “force Rails X mode.”

To learn more:

- https://github.com/presidentbeef/brakeman

To “have fun injecting SQL into a Ruby on Rails application”:

- https://github.com/presidentbeef/inject-some-sql

### Bundler-audit

> “Patch-level verification for Bundler. Looks for security vulnerabilities in dependencies.”.

- `bundler-audit update`: “updates the ruby-advisory-db.”

To learn more:

- https://github.com/rubysec/bundler-audit

### Flay

> “Flay analyzes code for structural similarities. Differences in literal values, variable, class, method names, whitespace, programming style, braces vs do/end, etc are all ignored. Making this totally rad.”

- `--summary`: “summarize. Show flay score per file only.”
- Code Climate's duplication engine wraps flay, and supports JavaScript as well.

To learn more:

- https://github.com/seattlerb/flay
- http://ruby.sadi.st/

About Code Climate's duplication engine & concept:

- https://github.com/codeclimate/codeclimate-duplication
- https://docs.codeclimate.com/docs/duplication-concept

### SandiMeter

> “Static analysis tool for checking Ruby code for Sandi Metz' rules.”

- `--rules`: “show rules.”
- `--graph`: “HTML mode. Create folder, log data and output stats to HTML file.”
- `--thresholds`: “thresholds for each rule (default: 90,90,90,90) or in config.yml.”

To learn more:

- https://github.com/makaroni4/sandi_meter

### Travis

https://travis-ci.org/

### Code Climate

https://codeclimate.com/product
https://docs.codeclimate.com/v1.0/docs/getting-started-team-adoption

### Danger

https://github.com/danger/danger
http://danger.systems
