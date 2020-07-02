# PHP Sentiment Analyzer

PHP Sentiment Analyzer is a lexicon and rule-based sentiment analysis tool that is used to understand sentiments in a sentence using VADER (Valence Aware Dictionary and sentiment Reasoner).

[![GitHub license](https://img.shields.io/github/license/davmixcool/php-sentiment-analyzer.svg)](https://github.com/davmixcool/php-sentiment-analyzer/blob/master/LICENSE)
[![GitHub issues](https://img.shields.io/github/issues/davmixcool/php-sentiment-analyzer.svg)](https://github.com/davmixcool/php-sentiment-analyzer/issues)
[![Twitter](https://img.shields.io/twitter/url/https/github.com/davmixcool/php-sentiment-analyzer.svg?style=social)](https://twitter.com/intent/tweet?text=Wow:&url=https%3A%2F%2Fgithub.com%2Fdavmixcool%2Fphp-sentiment-analyzer)

## Features

* Emoji
* Dublin Core
* Facebook OpenGraph
* Twitter Card

## Requirements

- PHP 5.5 and above

## Steps:

* [Install](#install)
* [Usage](#usage)
* [License](#license)
* [Reference](#reference)

### Install

**Composer**

Run the following to include this via Composer

```shell
composer require davmixcool/php-sentiment-analyzer
```

### Usage

```php

Use Sentiment\Analyzer;
$analyzer = new Analyzer(); 

$output_text = $analyzer->getSentiment("David is smart, handsome, and funny.");

$output_emoji = $analyzer->getSentiment("😁");

$output_text_with_emoji = $analyzer->getSentiment("Aproko doctor made me 🤣.");

print_r($output_text);
print_r($output_emoji);
print_r($output_text_with_emoji);

```
##Outputs
```
	David is smart, handsome, and funny. ----------------------------- ['neg'=> 0.0, 'neu'=> 0.337, 'pos'=> 0.663, 'compound'=> 0.7096]

	😁 									 ----------------------------- ['neg' => 0, 'neu' => 0.5, 'pos' => 0.5, 'compound' => 0.4588]
	
	Aproko doctor made me 🤣             ------------------------ ['neg' => 0, 'neu' => 1, 'pos' => 0, 'compound' => 0]

```

### License

This package is licensed under the [MIT license](https://github.com/davmixcool/php-sentiment-analyzer/blob/master/LICENSE).

### Reference

Hutto, C.J. & Gilbert, E.E. (2014). VADER: A Parsimonious Rule-based Model for Sentiment Analysis of Social Media Text. Eighth International Conference on Weblogs and Social Media (ICWSM-14). Ann Arbor, MI, June 2014. 