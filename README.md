# DGA Detector
DGA Domains detection

DGA domain detection is based on ngram analysis with trained markov chain model.
It is incorporate code by https://github.com/rrenaud/Gibberish-Detector<br>
#https://underdefense.com/guides/detecting-dga-domains-machine-learning-approach/<br>
https://otx.alienvault.com/browse/global/indicators?q=dga&include_inactive=0&sort=-modified&page=1&indicatorsSearch=dga<br>

The decision is based solely on results by this check.

In addition to ngram analysis it is also provide additional methods:
* entropy - High entropy is another indicator of DGA domain. Threshold is 3.8
* consonants - High consonants count is an indicator of DGA domain. Threshold is 7
* length - High domain length can also indicate DGA. Threshold is 12.

# Usage
```

_______________________       ________     _____           _____
___  __ \_  ____/__    |      ___  __ \______  /_____________  /______________
__  / / /  / __ __  /| |      __  / / /  _ \  __/  _ \  ___/  __/  __ \_  ___/
_  /_/ // /_/ / _  ___ |      _  /_/ //  __/ /_ /  __/ /__ / /_ / /_/ /  /
/_____/ \____/  /_/  |_|      /_____/ \___/\__/ \___/\___/ \__/ \____//_/
        
usage: dga_detector.py [-h] [-d DOMAIN] [-f FILE]

DGA domain detection

optional arguments:
  -h, --help            show this help message and exit
  -d DOMAIN, --domain DOMAIN
                        Domain to check
  -f FILE, --file FILE  File with domains. One per line
```
