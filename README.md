# Export your card collection from MTG: Arena
You need to install [python-mtga](https://github.com/mtgatracker/python-mtga) to use the export tool.

#### Note:
mtga-export.py reads the MTGA/Unity log file located under: 
    
    "%AppData%\LocalLow\Wizards Of The Coast\MTGA\output_log.txt"
    
If the MTGA game developers stop logging to this file, this export tool will not work anymore.

## Quick installation without python on Windows
Just download the standalone windows [latest](https://github.com/kelesi/mtga-utils/releases/download/latest/mtga-export.exe) pre-built executable from [releases](https://github.com/kelesi/mtga-utils/releases).

### Run it from cmd
Export your collection in [mtggoldfish](https://www.mtggoldfish.com/help/import_formats#mtggoldfish) format:

`mtga-export.exe --goldfish -f mtga_collection_goldfish.csv`

Export your collection in [deckstats](https://www.mtggoldfish.com/help/import_formats#deckstats) format:

`mtga-export.exe --deckstats -f mtga_collection_deckstats.csv`

Your collection will be saved to the current folder into mtga_collection_goldfish.csv or mtga_collection_deckstats.csv, which you can use to  import into mtggoldfish.com or deckstats.net.

## Examples:
Export your collection in [mtggoldfish](https://www.mtggoldfish.com/help/import_formats#mtggoldfish) format:

`mtga-export.py --goldfish -f mtga_collection_goldfish.csv`

Export your collection in [deckstats](https://www.mtggoldfish.com/help/import_formats#deckstats) format:

`mtga-export.py --deckstats -f mtga_collection_deckstats.csv`


## General usage:

```
usage: mtga-export.py [-h] [-l LOG_FILE] [-k KEYWORD] [--collids] [-c]
                      [-e {name,pretty_name,cost,sub_types,set,set_number,card_type,mtga_id} [{name,pretty_name,cost,sub_types,set,set_number,card_type,mtga_id} ...]]
                      [-gf] [-ds] [-f FILE]

Parse MTGA log file

optional arguments:
  -h, --help            show this help message and exit
  -l LOG_FILE, --log_file LOG_FILE
                        MTGA/Unity log file [Win: %AppData%\LocalLow\Wizards
                        Of The Coast\MTGA\output_log.txt]
  -k KEYWORD, --keyword KEYWORD
                        List json under keyword
  --collids             List collection ids
  -c, --collection      List collection with card data
  -e {name,pretty_name,cost,sub_types,set,set_number,card_type,mtga_id} [{name,pretty_name,cost,sub_types,set,set_number,card_type,mtga_id} ...], --export {name,pretty_name,cost,sub_types,set,set_number,card_type,mtga_id} [{name,pretty_name,cost,sub_types,set,set_number,card_type,mtga_id} ...]
                        Export collection in custom format
  -gf, --goldfish       Export in mtggoldfish format
  -ds, --deckstats      Export in deckstats format
  -f FILE, --file FILE  Store export to file
```
