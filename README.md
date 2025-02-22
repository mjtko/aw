# Aw

[![Build Status](https://travis-ci.org/fixrb/aw.svg?branch=master)][travis]
[![Code Climate](https://codeclimate.com/github/fixrb/aw/badges/gpa.svg)][codeclimate]
[![Gem Version](https://badge.fury.io/rb/aw.svg)][gem]
[![Inline docs](http://inch-ci.org/github/fixrb/aw.svg?branch=master)][inchpages]
[![Documentation](http://img.shields.io/:yard-docs-38c800.svg)][rubydoc]

> Aw, fork!

Creates a subprocess to execute a block inside.

## Contact

* Home page: https://github.com/fixrb/aw
* Bugs/issues: https://github.com/fixrb/aw/issues
* Support: https://stackoverflow.com/questions/tagged/fixrb

## Rubies

* [MRI](https://www.ruby-lang.org/)
* [Rubinius](https://rubinius.com/)

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'aw'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install aw

## Usage

It executes the block in a subprocess, and returns the result in the current process:

```ruby
Aw.fork! { 6 * 7 } # => 42
```

Of course, it prevents from side effects:

```ruby
arr = ['foo']

Aw.fork! { arr << 'FUU' } # => ["foo", "FUU"]

arr # => ["foo"]
```

## Security

As a basic form of security __Aw__ provides a set of SHA512 checksums for
every Gem release.  These checksums can be found in the `checksum/` directory.
Although these checksums do not prevent malicious users from tampering with a
built Gem they can be used for basic integrity verification purposes.

The checksum of a file can be checked using the `sha512sum` command.  For
example:

    $ sha512sum pkg/aw-0.1.0.gem
    548d9f669ded4e622182791a5390aaceae0bf2e557b0864f05a842b0be2c65e10e1fb8499f49a3b9efd0e8eaeb691351b1c670d6316ce49965a99683b1071389  pkg/aw-0.1.0.gem

## Versioning

__Aw__ follows [Semantic Versioning 2.0](https://semver.org/).

## Contributing

1. [Fork it](https://github.com/fixrb/aw/fork)
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request

## License

See `LICENSE.md` file.

[gem]: https://rubygems.org/gems/aw
[travis]: https://travis-ci.org/fixrb/aw
[codeclimate]: https://codeclimate.com/github/fixrb/aw
[inchpages]: http://inch-ci.org/github/fixrb/aw
[rubydoc]: http://rubydoc.info/gems/aw/frames

***

This project is sponsored by:

[![Sashite](https://sashite.com/img/sashite.png)](https://sashite.com/)
