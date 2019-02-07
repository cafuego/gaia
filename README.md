ELK docker stack (except without the 'L') for Gaia data.

## Quick Start

* Edit .env and set a BASE directory with lots and lots of free fast storage space
* Start the docker stack via `docker-compose up -d`
* Apply the Elasticsearch mapping from template.json to your indices
* Fetch some Gaia data from http://cdn.gea.esac.esa.int/Gaia/gdr2, e.g.:
  `wget -m http://cdn.gea.esac.esa.int/Gaia/gdr2/gaia_source_with_rv/csv`
* Edit `config.ini` with the access details for the Elasticsearch instance
* Import the data via `./csv2json ./path/to/Gaia_Data.csv`
* Wait for it...
* Play with your data via Kibana

## What?

* You can make HR diagrams by plotting `lum_val` against `teff_val`
* You can make a sky density map by mapping the `coordinates` field a map

## More Info

You can find information about the available data fields at http://dc.zah.uni-heidelberg.de/tableinfo/gdr2mock.main?tapinfo=True
