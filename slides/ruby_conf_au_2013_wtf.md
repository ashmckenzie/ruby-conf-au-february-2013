!SLIDE

# Ruby Conf Australia 2013 #

!SLIDE classes="small-bullets"

# Presentations #

* **Ben Orenstein** - Refactoring from Good to Great
* **Charles Nutter** - High Performance Ruby
* **Ben Hoskings** - State of the Ruby
* **Nick Sutterer** - Off the Tracks

!SLIDE classes="small-bullets-x2"

# Ben Orenstein #

## Refactoring from Good to Great ##

* Dev at thoughtbot - [@r00k](http://twitter.com/r00k)
* Live refactoring, lots of audience participation
* [fastrailstests.com](http://www.fastrailstests.com) mailing list with tips
* [Presentation](http://vimeo.com/61087282)
* [Code used in demonstration](https://github.com/r00k/refactoring-good-to-great)

!SLIDE classes="small-bullets"

# Charles Nutter #

## High Performance Ruby ##

* Lead dev on JRuby, works for RedHat - [@headius](http://twitter.com/headius)
* Performance comparison MRI vs. everything
* Use JRuby for [profiling](https://github.com/jruby/jruby/wiki/Profiling-jruby)
* Einsten's insanity quote
* Golden rule of optimisation - 'Do less work'
* [Presentation](http://vimeo.com/61087282)

!SLIDE classes="small-bullets"

# Ben Hoskings #

## State of the Ruby ##

* Dev at The Conversation - [@ben_h](http://twitter.com/ben_h)
*  Lazy Enumerables - Eval'd as requested
* Refinements - better monkey patching
* Keyword arguments
* DTrace support

!SLIDE classes="small-bullets-x2" language="haml"

%h2 Ben Hoskings - State of the Ruby

%h3 .lazy Enumerables

%pre{ 'data-language' => 'ruby' }
  :escaped
    def natural_numbers
      (1..Float::INFINITY).lazy
    end

    def primes
      natural_numbers.select do |n|
        (2..(n**0.5)).all? do |f|
          n % f > 0
        end
      end
    end

    p primes.take(5).to_a

    # [1, 2, 3, 5, 7]

!SLIDE classes="small-bullets-x2" language="haml"

%h2 Ben Hoskings - State of the Ruby

%h3 Refinements

%pre{ 'data-language' => 'ruby' }
  :escaped
    module Demo
      refine Array do
        def count
          'ruh roh'
        end
      end
    end

    p [].count
    using Demo
    p [].count

    # 0
    # "ruh roh"

!SLIDE classes="small-bullets-x2" language="haml"

%h2 Ben Hoskings - State of the Ruby

%h3 Keyword arguments

%pre{ 'data-language' => 'ruby' }
  :escaped
    def parse(test: true)
      p test
    end

    parse
    parse(test: false)

    # true
    # false

!SLIDE classes="small-bullets"

## Ben Hoskings - State of the Ruby ##

### Links ###

* [Presentation](http://vimeo.com/61255648)
* [Ruby 2.0 by example](http://benhoskin.gs/2013/02/24/ruby-2-0-by-example)
* [Getting to know Ruby 2.0](http://benhoskin.gs/2013/02/24/getting-to-know-ruby-2-0)

!SLIDE classes="small-bullets"

# Keith and Mario's<br/>Guide to Fast Websites #

<br/>
## Sadly, there was no room :sob: ##

* [Presentation](http://vimeo.com/61342267)

!SLIDE classes="small-bullets"

# Nick Sutterer #

## Off the Tracks ##

* Freelance dev - [@apotonick](http://twitter.com/apotonick)
* Crazy dude
* [ROAR](https://github.com/apotonick/roar) - Object oriented REST objects
* [cells](https://github.com/apotonick/cells) - Components for Rails
* [Presentation](http://vimeo.com/61255731)

!SLIDE classes="small-bullets"

# Take aways #

* We're doing an awesome job at Hooroo! :metal:
* We should spruik what we do to the community
* Ruby 2.0 / JRuby really exciting
* Rails core 'team' ruled by DHH
* Everyone loves Aaron Patterson
* Rails 4 + PostgreSQL == :heart: :blue_heart: :yellow_heart:

!SLIDE classes="small-bullets"

# Done #

:smile:

* [Ruby Conf AU Videos](http://vimeo.com/rubyau)
* [This presentation](http://ashmckenzie.github.com/ruby-conf-au-february-2013)
