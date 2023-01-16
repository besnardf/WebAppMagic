## Plugins

Grab a list of plugins and make it a dictionary (based on [this idea](https://twitter.com/nullenc0de/status/1319667713179004928) from @nullenc0de):
```bash
curl https://data.wpscan.org/metadata.json | jq -r '.plugins' | grep ": {" | cut -d "\"" -f2 | while read word; do echo wp-content/plugins/$word/readme.txt; done > wordpress_dict.txt
```
