# Korpus.cz API #

## Preface ##

This is a simple tool to run queries agains the [Korpus.cz] web application. As far as I know, it does not have any public API, but sometimes it’s useful to get some data from the database automatically.

## Functionality ##

Currently the tool consists of a single scriptlet that just runs a [CQL] query and prints retrieved sentences to the console. There is no way to customize the query or to get any metadata from the results. Pagination is not supported.

The app does not check for any errors, does not handle any edge cases and is absolutely untested. It’s just a scrap.

## Requirements ##

* [Ruby], the closer to 2.5.1 the better

## Usage ##

First, install the required dependencies using [Bundler].

```shell
$ bundle install
```

Then run the scriptlet, passing the [CQL] query as its argument.

```shell
$ ruby bin/korpus_cz_api '[lemma="Pokémon"&tag="....4..........."]'
```

Example output:

    a hry Invizimals . Hra je jakousi variací na slavné [ Pokémony]  : po světě sbíráte rozličné potvůrky a následně s nimi
    nějak zvlášť nadšená , když se i on vrhl na [ Pokémony]  , které zbožňovala jeho sestra , na druhou stranu jsem
    času . „ Vezměte si malé děti , které hrají [ Pokémony]  , “ říká Gee . „ Pokémoni jsou hra pro
    kravina , ale když nepovolím Julii , dají na něj [ Pokémona]  nebo Šmoulu nebo co já vím , co zrovna letí

[Korpus.cz]: https://www.korpus.cz/
[CQL]: https://www.sketchengine.eu/documentation/corpus-querying/
[Ruby]: https://www.ruby-lang.org/
[Bundler]: https://bundler.io
