# PaloAltoNetwork config analysis help

This is a simple library that parses and extract useful information from
PaloAlto Network firewalls XML configuration.

## Idea

PaloAlto Network exports its configuration in an XML file that can be used by
security auditors for analysis.

This is a bit of convenience classes and methods to extract that information.
It is thought to do the analysis on `irb` although a simple example cli program
is provided.

## Instalation

At the moment, just download it. I'll try to provide a gem soon.

## Usage

### On irb

On `irb` you can `require 'paloalto'` and use its classes to do your analysis,
like this:

    >> require 'paloalto'
    >> PaloAlto::Config.new(open 'paloalto_config.xml')

### paloalto_config_analysis.rb

Just run the following to get a summary that may be useful for your analysis:

    ruby paloalto_config_analysis.rb paloalto_config.xml 
