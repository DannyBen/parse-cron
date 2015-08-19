# parse-cron

[![Build Status](https://travis-ci.org/siebertm/parse-cron.png)](https://travis-ci.org/siebertm/parse-cron)

Parse crontab syntax & determine next and last times


The goal of this gem is to parse a crontab timing specification and determine when the
job should be run. It is not a scheduler, it does not run the jobs.

## Install

```shell
$ gem install 'parse-cron'
```

## API example

```ruby
cron_parser = CronParser.new('30 * * * *')

# Get next time
next_time = cron_parser.next(Time.now)

# Get last time
last_time = cron_parser.last(Time.now)
```

