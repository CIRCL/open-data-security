# open-data-security description format

open-data-security description format is a simple JSON format to describe dataset released
as open data by security researchers, security vendors or CSIRTs. The aim is to ensure interoperable description of dataset collected in security monitoring and analysis.

## Overview

## Schema

|Field name|Required|Description |
|:----|:--:|:------|
|`title`|yes|A comprehensive and concise `title` of the dataset.|
|`subtitle`|no|An extended title of the dataset.|
|`description`|no|An exhaustive `description` of the dataset including methods of collection, extraction or analysis.|
|`license`|yes|`license` MUST be expressed in [SPDX format](https://spdx.github.io/spdx-spec/SPDX-license-list/) to describe under which license the dataset is distributed.|
|`tags`|no|`tag` is an array of tags. The `tag` SHOULD come from a [MISP taxonomy namespace](https://www.misp-project.org/taxonomies.html). Free `tags` are permitted but their use is discouraged.|
|`source`|no|`source` is an array of value. A source is a free text describing the origin of the dataset. This can be an url but also a free text describing the source.|
|`time-precision`|no|`time-precision` MUST be expressed in years, months, days, hours, minutes or seconds to describe the precision of the time expressed.|
|`frequency`|no|`frequency` of the dataset generation which MUST be expressed in yearly, monthly, daily, hourly, continuous. Continuous is used for streamed dataset.|
|`producer`|no|`producer` MUST be expressed as an URI to reference the original producer of the dataset.|
|`human-validated`|no|`human-validated` describes if the dataset has been manually validated.|
|`machine-validated`|no|`machine-validated` describes if the dataset has been automatically validated.|

## JSON Schema

* [open-data-security](schema.json)

# Sample files

* [a honeypot dataset](sample/sample.json)

# How to use it?

- Add your JSON file in the directory where the dataset is published and the filename must be named `meta.json`.

# Where is it used?

- VARIoT project to describe the [dataset available](https://cra.circl.lu/opendata/variot/iot-exposed-infected-device-stats/meta/).

# License

The work for the open-data-security is released by [CIRCL](https://www.circl.lu/) as CC0 1.0 Universal (CC0 1.0).

