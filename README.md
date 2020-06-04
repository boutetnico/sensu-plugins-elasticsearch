## Sensu-Plugins-elasticsearch

[![Gem Version](https://badge.fury.io/rb/sensu-plugins-elasticsearch-boutetnico.svg)](https://badge.fury.io/rb/sensu-plugins-elasticsearch-boutetnico.svg)
[![Sensu Bonsai Asset](https://img.shields.io/badge/Bonsai-Download%20Me-brightgreen.svg?colorB=89C967&logo=sensu)](https://bonsai.sensu.io/assets/boutetnico/sensu-plugins-elasticsearch)

## This is an unofficial fork

Due to the lack of activity from owners of [sensu-plugins-elasticsearch](https://github.com/sensu-plugins/sensu-plugins-elasticsearch) I have created this fork. It is automatically tested, built and published to [RubyGems](https://rubygems.org/gems/sensu-plugins-elasticsearch-boutetnico/) and [Bonsai](https://bonsai.sensu.io/assets/boutetnico/sensu-plugins-elasticsearch). It includes some improvements. Please check the changelog at the [GitHub Releases page](https://github.com/boutetnico/sensu-plugins-elasticsearch/releases).

## Sensu Asset  
  The Sensu assets packaged from this repository are built against the Sensu ruby runtime environment. When using these assets as part of a Sensu Go resource (check, mutator or handler), make sure you include the corresponding Sensu ruby runtime asset in the list of assets needed by the resource.  The current ruby-runtime assets can be found [here](https://bonsai.sensu.io/assets/sensu/sensu-ruby-runtime) in the [Bonsai Asset Index](bonsai.sensu.io).

## Functionality

## Files
 * /bin/check-es-circuit-breakers.rb
 * /bin/check-es-cluster-health.rb
 * /bin/check-es-cluster-status.rb
 * /bin/check-es-file-descriptors.rb
 * /bin/check-es-heap.rb
 * /bin/check-es-indices-field-count.rb
 * /bin/check-es-indexes.rb
 * /bin/check-es-indicies-sizes.rb
 * /bin/check-es-node-status.rb
 * /bin/check-es-query-count.rb
 * /bin/check-es-query-exists.rb
 * /bin/check-es-query-ratio.rb
 * /bin/check-es-shard-allocation-status.rb
 * /bin/handler-es-delete-indices.rb
 * /bin/metrics-es-cluster.rb
 * /bin/metrics-es-node.rb
 * /bin/metrics-es-node-graphite.rb

## Usage

## Installation

[Installation and Setup](http://sensu-plugins.io/docs/installation_instructions.html)

## Notes
When using `handler-es-delete-indices.rb` with Sensu Go, you will need to use the event mapping commandline option, see `handler-es-delete-indices.rb --help` for details. And please read [the sensu-plugin README](https://github.com/sensu-plugins/sensu-plugin#sensu-go-enablement) for more information on the event mapping functionality.

## Testing

This repository uses the [Kitchen](https://kitchen.ci/) suite for it's tests.

Note: The test suite uses an elasticsearch instance in order to have passing tests. Execute the following command to create a mock elasticsearch 6 instance:

```bash
docker run -d --name sensu-elasticsearch-7 docker.elastic.co/elasticsearch/elasticsearch:7.1.1
```

Running the tests:

```bash
bundle install --path vendor/bundle
bundle exec kitchen test
```

You can find sample output for all tests running successfully in [this gist](https://gist.github.com/alexandrustaetu/d19feea1296d2ce7e367542265252d7a).
