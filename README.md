# News
We are putting together plans for future changes. We obviously depend on all of you to take part in the planning for the future of goamz and execution of the plans. Other than the regulare 'issues' and 'pull requests' please also have a look at TODO.md.     

It is inevitable that there will be backward-*in*compatible changes. Please subscribe to the google group to get all the news (it will only be used for announcements, all the technical discussions will happen on github). 

Google group: https://groups.google.com/forum/#!forum/goamz-announcements 



# GoAMZ

[![Build Status](https://travis-ci.org/arvindkandhare/goamz.png?branch=master)](https://travis-ci.org/arvindkandhare/goamz)

The _goamz_ package enables Go programs to interact with Amazon Web Services.

This is a fork of the version [developed within Canonical](https://wiki.ubuntu.com/goamz) with additional functionality and services from [a number of contributors](https://github.com/arvindkandhare/goamz/contributors)!

The API of AWS is very comprehensive, though, and goamz doesn't even scratch the surface of it. That said, it's fairly well tested, and is the foundation in which further calls can easily be integrated. We'll continue extending the API as necessary - Pull Requests are _very_ welcome!

The following packages are available at the moment:

```
github.com/arvindkandhare/goamz/aws
github.com/arvindkandhare/goamz/cloudwatch
github.com/arvindkandhare/goamz/dynamodb
github.com/arvindkandhare/goamz/ec2
github.com/arvindkandhare/goamz/elb
github.com/arvindkandhare/goamz/iam
github.com/arvindkandhare/goamz/kinesis
github.com/arvindkandhare/goamz/s3
github.com/arvindkandhare/goamz/sqs
github.com/arvindkandhare/goamz/sns

github.com/arvindkandhare/goamz/exp/mturk
github.com/arvindkandhare/goamz/exp/sdb
github.com/arvindkandhare/goamz/exp/ses
```

Packages under `exp/` are still in an experimental or unfinished/unpolished state.

## API documentation

The API documentation is currently available at:

[http://godoc.org/github.com/arvindkandhare/goamz](http://godoc.org/github.com/arvindkandhare/goamz)

## How to build and install goamz

Just use `go get` with any of the available packages. For example:

* `$ go get github.com/arvindkandhare/goamz/ec2`
* `$ go get github.com/arvindkandhare/goamz/s3`

## Running tests

To run tests, first install gocheck with:

`$ go get launchpad.net/gocheck`

Then run go test as usual:

`$ go test github.com/arvindkandhare/goamz/...`

_Note:_ running all tests with the command `go test ./...` will currently fail as tests do not tear down their HTTP listeners.

If you want to run integration tests (costs money), set up the EC2 environment variables as usual, and run:

`$ gotest -i`
