# ![LOGO](logo.png) Geocoder **flow**ground Connector

## Description

A generated **flow**ground connector for the Geocoder API (version 2.0.0).

Generated from: https://api.apis.guru/v2/specs/gov.bc.ca/geocoder/2.0.0/openapi.json<br/>
Generated at: 2019-05-07T17:42:11+03:00

## API Description

This API represents address cleaning, correction, completion, geocoding, reverse geocoding, and proximity resources for intersection addresses, physical addresses and their occupants in British Columbia. Please read our [data collection notice](https://github.com/bcgov/api-specs/blob/master/COLLECTION_NOTICE.md#collection-notice).  

Please note that you may experience issues when submitting requests to the delivery or test environment if using this [OpenAPI specification](https://github.com/bcgov/api-specs) in other API console viewers. 

[Developer API keys](https://github.com/bcgov/gwa/wiki/Developer-Guide#developer-api-keys) are unique and provide the ability to make up to 2 requests per second. Production government applications may use organization API keys which are further described in [the Developer guide](https://github.com/bcgov/gwa/wiki/Developer-Guide#developer-api-keys).

 **Notification: If you have applications or web pages that link to the public geocoder at one of the following URLs, please note that they are now deprecated [More Details](https://www2.gov.bc.ca/gov/content?id=103ADC5A956842828554238DEF28D6E5).  
 - http://apps.gov.bc.ca/pub/geocoder 
 - https://apps.gov.bc.ca/pub/geocoder
 
 
 **To acquire an API key please visit the [API Key Request](https://kq.apps.gov.bc.ca/) application.**
 

## Authorization

Supported authorization schemes:
- API Key
## Actions

### Geocode an address

> Represents the set of geocoded and standardized sites and intersections whose address best matches a given query address.

*Tags:* `sites` `intersections`

#### Input Parameters
* `outputFormat` - _required_ - Results format. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#outputFormat target="_blank">outputFormat</a>
    Possible values: json, geojson, xhtml, kml, gml, csv, shpz.
* `addressString` - _optional_ - Civic or intersection address as a single string. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#addressString target="_blank">addressString</a>
* `locationDescriptor` - _optional_ - Describes the nature of the address location. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#locationDescriptor target="_blank">locationDescriptor</a>
    Possible values: any, accessPoint, frontDoorPoint, parcelPoint, rooftopPoint, routingPoint.
* `maxResults` - _optional_ - The maximum number of search results to return.
* `interpolation` - _optional_ - accessPoint interpolation method. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#interpolation target="_blank">interpolation</a>
    Possible values: adaptive, linear, none.
* `echo` - _optional_ - If true, include unmatched address details such as site name in results.
* `brief` - _optional_ - If true, include only basic match and address details in results. Not supported for shp, csv, and gml formats.
* `autoComplete` - _optional_ - If true, addressString is expected to contain a partial address that requires completion. Not supported for shp, csv, gml formats.
* `setBack` - _optional_ - The distance to move the accessPoint away from the curb and towards the inside of the parcel (in metres). Ignored if locationDescriptor not set to accessPoint.
* `outputSRS` - _optional_ - The EPSG code of the spatial reference system (SRS) to use for output geometries. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#outputSRS target="_blank">outputSRS</a>
    Possible values: 4326, 4269, 3005, 26907, 26908, 26909, 26910, 26911.
* `minScore` - _optional_ - The minimum score required for a match to be returned. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#minScore target="_blank">minScore</a>
* `matchPrecision` - _optional_ - Example: street,locality.  A comma separated list of individual match precision levels to include in results. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#matchPrecision target="_blank">matchPrecision</a>
* `matchPrecisionNot` - _optional_ - Example: street,locality.  A comma separated list of individual match precision levels to exclude from results. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#matchPrecisionNot target="_blank">matchPrecisionNot</a>
* `siteName` - _optional_ - A string containing the name of the building, facility, or institution (e.g., Duck Building, Casa Del Mar, Crystal Garden, Bluebird House).See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#siteName target="_blank">siteName</a>
* `unitDesignator` - _optional_ - The type of unit within a house or building. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#unitDesignator target="_blank">unitDesignator</a>
    Possible values: APT, BLDG, BSMT, FLR, LOBBY, LWR, PAD, PH, REAR, RM, SIDE, SITE, SUITE, TH, UNIT, UPPR.
* `unitNumber` - _optional_ - The number of the unit, suite, or apartment within a house or building.
* `unitNumberSuffix` - _optional_ - A letter that follows the unit number as in Unit 1A or Suite 302B.
* `civicNumber` - _optional_ - The official number assigned to a site by an address authority. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#civicNumber target="_blank">civicNumber</a>
* `civicNumberSuffix` - _optional_ - A letter or fraction that follows the civic number (e.g., the A in 1039A Bledsoe St). See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#civicNumberSuffix target="_blank">civicNumberSuffix</a>
* `streetName` - _optional_ - The official name of the street as assigned by an address authority (e.g., the Douglas in 1175 Douglas Street). See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#streetName target="_blank">streetName</a>
* `streetType` - _optional_ - The type of street as assigned by a municipality (e.g., the ST in 1175 DOUGLAS St). See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#streetType target="_blank">streetType</a>
* `streetDirection` - _optional_ - The abbreviated compass direction as defined by Canada Post and B.C. civic addressing authorities. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#streetDirection target="_blank">streetDirection</a>
    Possible values: N, S, E, W, O, NE, NO, NW, SE, SO, SW.
* `streetQualifier` - _optional_ - Example: the Bridge in Johnson St Bridge. The qualifier of a street name. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#streetQualifier target="_blank">streetQualifier</a>
* `localityName` - _optional_ - The name of the locality assigned to a given site by an address authority. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#localityName target="_blank">localityName</a>
* `provinceCode` - _optional_ - The ISO 3166-2 Sub-Country Code. The code for British Columbia is BC.
* `localities` - _optional_ - A comma separated list of locality names that matched addresses must belong to. For example, setting localities to Nanaimo only returns addresses in Nanaimo
* `notLocalities` - _optional_ - A comma-separated list of localities to exclude from the search.
* `bbox` - _optional_ - Example: -126.07929,49.7628,-126.0163,49.7907.  A bounding box (xmin,ymin,xmax,ymax) that limits the search area. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#bbox target="_blank">bbox</a>
* `centre` - _optional_ - Example: -124.0165926,49.2296251 .  The coordinates of a centre point (x,y) used to define a bounding circle that will limit the search area. This parameter must be specified together with 'maxDistance'. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#centre target='_blank'>centre</a>
* `maxDistance` - _optional_ - The maximum distance (in metres) to search from the given point.  If not specified, the search distance is unlimited.
* `extrapolate` - _optional_ - If true, uses supplied parcelPoint to derive an appropriate accessPoint.           See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#extrapolate target="_blank">extrapolate</a>
* `parcelPoint` - _optional_ - The coordinates of a point (x,y) known to be inside the parcel containing a given address. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#parcelPoint target="_blank">parcelPoint</a>

### Find intersections near to a geographic point

> Represents intersections near a given point

*Tags:* `intersections`

#### Input Parameters
* `outputFormat` - _required_ - Results format. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#outputFormat target="_blank">outputFormat</a>
    Possible values: json, geojson, xhtml, kml, gml, csv, shpz.
* `point` - _required_ - The point (x,y) from which the nearest site will be identified. The coordinates must be specified in the same SRS as given by the 'outputSRS' parameter.
* `maxDistance` - _optional_ - The maximum distance (in metres) to search from the given point.  If not specified, the search distance is unlimited.
* `outputSRS` - _required_ - The EPSG code of the spatial reference system (SRS) to use for output geometries. See <a href=https://github.com/bcgovapi-specs/blob/master/geocoder/glossary.md#outputSRS target="_blank">outputSRS</a>
    Possible values: 4326, 4269, 3005, 26907, 26908, 26909, 26910, 26911.
* `maxResults` - _optional_ - The maximum number of search results to return.
* `minDegree` - _optional_ - The minimum degree an intersection can have to be included in results. A dead-end has a degree of 1.
* `maxDegree` - _optional_ - The maximum degree an interesection can have to be included in results. A four-way stop has a degree of 4.

### Find nearest intersection to a geographic point

> Represents the closest intersection to a given point

*Tags:* `intersections`

#### Input Parameters
* `outputFormat` - _required_ - Results format. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#outputFormat target="_blank">outputFormat</a>
    Possible values: json, geojson, xhtml, kml, gml, csv, shpz.
* `point` - _required_ - Example: -122.377,50.121  The point (x,y) from which the nearest site will be identified. The coordinates must be specified in the same SRS as given by the 'outputSRS' parameter.
* `maxDistance` - _optional_ - The maximum distance (in metres) to search from the given point.  If not specified, the search distance is unlimited.
* `outputSRS` - _optional_ - The EPSG code of the spatial reference system (SRS) to use for output geometries. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#outputSRS target="_blank">outputSRS</a>
    Possible values: 4326, 4269, 3005, 26907, 26908, 26909, 26910, 26911.
* `minDegree` - _optional_ - The minimum degree an intersection can have to be included in results. A dead-end has a degree of 1.
* `maxDegree` - _optional_ - The maximum degree an interesection can have to be included in results. A four-way stop has a degree of 4.

### Find intersections in a geographic area

> Represents all intersections within a given area

*Tags:* `intersections`

#### Input Parameters
* `outputFormat` - _required_ - Results format. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#outputFormattarget="_blank">outputFormat</a>
    Possible values: json, geojson, xhtml, kml, gml, csv, shpz.
* `bbox` - _required_ - A bounding box (xmin,ymin,xmax,ymax) used to limit the search area. See <a href=https://github.com/bcgovapi-specs/blob/master/geocoder/glossary.md#bbox target="_blank">bbox</a>
* `outputSRS` - _optional_ - The EPSG code of the spatial reference system (SRS) to use for output geometries. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#outputSRS target="_blank">outputSRS</a>
    Possible values: 4326, 4269, 3005, 26907, 26908, 26909, 26910, 26911.
* `maxResults` - _optional_ - The maximum number of search results
* `minDegree` - _optional_ - The minimum degree an intersection can have to be included in results. A dead-end has a degree of 1.
* `maxDegree` - _optional_ - The maximum degree an interesection can have to be included in results. A four-way stop has a degree of 4.

### Get an intersection by its unique ID

> Represents a individual intersection

*Tags:* `intersections`

#### Input Parameters
* `intersectionID` - _required_ - A unique intersection identifier
* `outputFormat` - _required_ - Results format. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#outputFormat target="_blank">outputFormat</a>
    Possible values: json, geojson, xhtml, kml, gml, csv, shpz.
* `outputSRS` - _optional_ - The EPSG code of the spatial reference system (SRS) to use for output geometries. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#outputSRS target="_blank">outputSRS</a>
    Possible values: 4326, 4269, 3005, 26907, 26908, 26909, 26910, 26911.

### Geocode an address and identify site occupants

> Represents the set of occupants whose addresses best match a given query address. Every occupant has an associated site which has a standardized address and a coordinate location on the Earth.

*Tags:* `occupants`

#### Input Parameters
* `outputFormat` - _required_ - Results format. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#outputFormat target="_blank">outputFormat</a>
    Possible values: json, geojson, xhtml, kml, gml, csv, shpz.
* `addressString` - _optional_ - Occupant name OR Occupant name ** address
* `tags` - _optional_ - Example: schools;courts;employment<br>A list of tags separated by semicolons.
* `locationDescriptor` - _optional_ - Describes the nature of the address location. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#locationDescriptor target="_blank">locationDescriptor</a>
    Possible values: any, accessPoint, frontDoorPoint, parcelPoint, rooftopPoint, routingPoint.
* `maxResults` - _optional_ - The maximum number of search results to return.
* `interpolation` - _optional_ - accessPoint interpolation method. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#interpolation target="_blank">interpolation</a>
    Possible values: adaptive, linear, none.
* `echo` - _optional_ - If true, include unmatched address details such as site name in results.
* `brief` - _optional_ - If true, include only basic match and address details in results. Not supported for shp, csv, and gml formats.
* `autoComplete` - _optional_ - If true, addressString is expected to contain a partial address that requires completion. Not supported for shp, csv, gml formats.
* `setBack` - _optional_ - The distance to move the accessPoint away from the curb and towards the inside of the parcel (in metres). Ignored if locationDescriptor not set to accessPoint.
* `outputSRS` - _optional_ - The EPSG code of the spatial reference system (SRS) to use for output geometries. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#outputSRS target="_blank">outputSRS</a>
    Possible values: 4326, 4269, 3005, 26907, 26908, 26909, 26910, 26911.
* `minScore` - _optional_ - The minimum score required for a match to be returned. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#minScore target="_blank">minScore</a>
* `matchPrecision` - _optional_ - Example: street,locality.  A comma separated list of individual match precision levels to include in results. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#matchPrecision target="_blank">matchPrecision</a>
* `matchPrecisionNot` - _optional_ - Example: street,locality.  A comma separated list of individual match precision levels to exclude from results. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#matchPrecisionNot target="_blank">matchPrecisionNot</a>
* `siteName` - _optional_ - A string containing the name of the building, facility, or institution (e.g., Duck Building, Casa Del Mar, Crystal Garden, Bluebird House).See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#siteName target="_blank">siteName</a>
* `unitDesignator` - _optional_ - The type of unit within a house or building. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#unitDesignator target="_blank">unitDesignator</a>
    Possible values: APT, BLDG, BSMT, FLR, LOBBY, LWR, PAD, PH, REAR, RM, SIDE, SITE, SUITE, TH, UNIT, UPPR.
* `unitNumber` - _optional_ - The number of the unit, suite, or apartment within a house or building.
* `unitNumberSuffix` - _optional_ - A letter that follows the unit number as in Unit 1A or Suite 302B.
* `civicNumber` - _optional_ - The official number assigned to a site by an address authority. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#civicNumber target="_blank">civicNumber</a>
* `civicNumberSuffix` - _optional_ - A letter or fraction that follows the civic number (e.g., the A in 1039A Bledsoe St). See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#civicNumberSuffix target="_blank">civicNumberSuffix</a>
* `streetName` - _optional_ - The official name of the street as assigned by an address authority (e.g., the Douglas in 1175 Douglas Street). See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#streetName target="_blank">streetName</a>
* `streetType` - _optional_ - The type of street as assigned by a municipality (e.g., the ST in 1175 DOUGLAS St). See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#streetType target="_blank">streetType</a>
* `streetDirection` - _optional_ - The abbreviated compass direction as defined by Canada Post and B.C. civic addressing authorities. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#streetDirection target="_blank">streetDirection</a>
    Possible values: N, S, E, W, O, NE, NO, NW, SE, SO, SW.
* `streetQualifier` - _optional_ - The qualifier of a street name (e.g., the Bridge in Johnson St Bridge)
* `localityName` - _optional_ - The name of the locality assigned to a given site by an address authority. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#streetDirection target="_blank">streetDirection</a>
* `provinceCode` - _optional_ - The ISO 3166-2 Sub-Country Code. The code for British Columbia is BC.
* `localities` - _optional_ - A comma separated list of locality names that matched addresses must belong to. For example, setting localities to Nanaimo only returns addresses in Nanaimo
* `notLocalities` - _optional_ - A comma-separated list of localities to exclude from the search.
* `bbox` - _optional_ - Example: -126.07929,49.7628,-126.0163,49.7907.  A bounding box (xmin,ymin,xmax,ymax) that limits the search area. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#bbox target="_blank">bbox</a>
* `centre` - _optional_ - Example: -124.0165926,49.2296251 .  The coordinates of a centre point (x,y) used to define a bounding circle that will limit the search area. This parameter must be specified together with 'maxDistance'. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#centre target='_blank'>centre</a>
* `maxDistance` - _optional_ - The maximum distance (in metres) to search from the given point.  If not specified, the search distance is unlimited.
* `extrapolate` - _optional_ - If true, uses supplied parcelPoint to derive an appropriate accessPoint.           See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#extrapolate target="_blank">extrapolate</a>
* `parcelPoint` - _optional_ - The coordinates of a point (x,y) known to be inside the parcel containing a given address. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#parcelPoint target="_blank">parcelPoint</a>

### Find occupants of sites near to a geographic point

> Represents occupants near a given point in order of closest to farthest

*Tags:* `occupants`

#### Input Parameters
* `outputFormat` - _required_ - Results format. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#outputFormat target="_blank">outputFormat</a>
    Possible values: json, geojson, xhtml, kml, gml, csv, shpz.
* `point` - _required_ - The point (x,y) from which the nearest site will be identified. The coordinates must be specified in the same SRS as given by the 'outputSRS' parameter.
* `tags` - _optional_ - Example: schools;courts;employment<br>A list of tags separated by semicolons.
* `maxDistance` - _optional_ - The maximum distance (in metres) to search from the given point.  If not specified, the search distance is unlimited.
* `outputSRS` - _optional_ - The EPSG code of the spatial reference system (SRS) to use for output geometries. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#outputSRS target="_blank">outputSRS</a>
    Possible values: 4326, 4269, 3005, 26907, 26908, 26909, 26910, 26911.
* `maxResults` - _optional_ - The maximum number of search results to return.
* `locationDescriptor` - _optional_ - Describes the nature of the address location. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#locationDescriptor target="_blank">locationDescriptor</a>
    Possible values: any, accessPoint, frontDoorPoint, parcelPoint, rooftopPoint, routingPoint.
* `brief` - _optional_ - If true, include only basic match and address details in results. Not supported for shp, csv, and gml formats.
* `setBack` - _optional_ - The distance to move the accessPoint away from the curb and towards the inside of the parcel (in metres). Ignored if locationDescriptor not set to accessPoint.

### Find occupants of the site nearest to a geographic point

> Represents the closest occupant to a given point

*Tags:* `occupants`

#### Input Parameters
* `outputFormat` - _required_ - Results format. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#outputFormat target="_blank">outputFormat</a>
    Possible values: json, geojson, xhtml, kml, gml, csv, shpz.
* `point` - _required_ - The point (x,y) from which the nearest site will be identified. The coordinates must be specified in the same SRS as given by the 'outputSRS' parameter.
* `maxDistance` - _optional_ - The maximum distance (in metres) to search from the given point.  If not specified, the search distance is unlimited.
* `tags` - _optional_ - Example: schools;courts;employment<br>A list of tags separated by semicolons.
* `outputSRS` - _optional_ - The EPSG code of the spatial reference system (SRS) to use for output geometries. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#outputSRS target="_blank">outputSRS</a>
    Possible values: 4326, 4269, 3005, 26907, 26908, 26909, 26910, 26911.
* `locationDescriptor` - _optional_ - Describes the nature of the address location. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#locationDescriptor target="_blank">locationDescriptor</a>
    Possible values: any, accessPoint, frontDoorPoint, parcelPoint, rooftopPoint, routingPoint.
* `brief` - _optional_ - If true, include only basic match and address details in results. Not supported for shp, csv, and gml formats.
* `setBack` - _optional_ - The distance to move the accessPoint away from the curb and towards the inside of the parcel (in metres). Ignored if locationDescriptor not set to accessPoint.

### Find occupants of sites in a geographic area

> Represents all occupants within a given area

*Tags:* `occupants`

#### Input Parameters
* `outputFormat` - _required_ - Results format. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#outputFormat target="_blank">outputFormat</a>
    Possible values: json, geojson, xhtml, kml, gml, csv, shpz.
* `bbox` - _required_ - A bounding box (xmin,ymin,xmax,ymax) used to limit the search area. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#bbox target="_blank">bbox</a>
* `tags` - _optional_ - Example: schools;courts;employment<br>A list of tags separated by semicolons.
* `outputSRS` - _optional_ - The EPSG code of the spatial reference system (SRS) to use for output geometries. See <a href=https://github.com/bcgovapi-specs/blob/master/geocoder/glossary.md#outputSRS target="_blank">outputSRS</a>
    Possible values: 4326, 4269, 3005, 26907, 26908, 26909, 26910, 26911.
* `maxResults` - _optional_ - The maximum number of search results to return.
* `locationDescriptor` - _optional_ - Describes the nature of the address location. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#locationDescriptor target="_blank">locationDescriptor</a>
    Possible values: any, accessPoint, frontDoorPoint, parcelPoint, rooftopPoint, routingPoint.
* `brief` - _optional_ - If true, include only basic match and address details in results. Not supported for shp, csv, and gml formats.
* `setBack` - _optional_ - The distance to move the accessPoint away from the curb and towards the inside of the parcel (in metres). Ignored if locationDescriptor not set to accessPoint.

### Get an occupant (of a site) by its unique ID

> Represents an individual occupant

*Tags:* `occupants`

#### Input Parameters
* `occupantID` - _required_ - Occupant identifier
* `outputFormat` - _required_ - Results format. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#outputFormat target="_blank">outputFormat</a>
    Possible values: json, geojson, xhtml, kml, gml, csv, shpz.
* `outputSRS` - _optional_ - The EPSG code of the spatial reference system (SRS) to use for output geometries. See <a href=https://github.com/bcgovapi-specs/blob/master/geocoder/glossary.md#outputSRS target="_blank">outputSRS</a>
    Possible values: 4326, 4269, 3005, 26907, 26908, 26909, 26910, 26911.
* `locationDescriptor` - _optional_ - Describes the nature of the address location. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#locationDescriptor target="_blank">locationDescriptor</a>
    Possible values: any, accessPoint, frontDoorPoint, parcelPoint, rooftopPoint, routingPoint.
* `brief` - _optional_ - If true, include only basic match and address details in results. Not supported for shp, csv, and gml formats.
* `setBack` - _optional_ - The distance to move the accessPoint away from the curb and towards the inside of the parcel (in metres). Ignored if locationDescriptor not set to accessPoint.

### Get a comma-separated string of all pids for a given site

> Represents all parcel identifiers associated with an individual site

*Tags:* `parcels`

#### Input Parameters
* `siteID` - _required_ - A unique, but not immutable, site identifier.
* `outputFormat` - _required_ - Results format. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#outputFormat target="_blank">outputFormat</a>
    Possible values: json, geojson, xhtml, kml, gml, csv, shpz.

### Find sites near to a geographic point

> Represents sites near a given point in the order of closest to farthest

*Tags:* `sites`

#### Input Parameters
* `outputFormat` - _required_ - Results format. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#outputFormat target="_blank">outputFormat</a>
    Possible values: json, geojson, xhtml, kml, gml, csv, shpz.
* `point` - _required_ - The point (x,y) from which the nearby sites will be identified. The coordinates must be specified in the same SRS as given by the 'outputSRS' parameter.
* `maxDistance` - _optional_ - The maximum distance (in metres) to search from the given point.  If not specified, the search distance is unlimited.
* `outputSRS` - _optional_ - The EPSG code of the spatial reference system (SRS) to use for output geometries. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#outputSRS target="_blank">outputSRS</a>
    Possible values: 4326, 4269, 3005, 26907, 26908, 26909, 26910, 26911.
* `maxResults` - _optional_ - The maximum number of search results to return.
* `locationDescriptor` - _optional_ - Describes the nature of the address location. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#locationDescriptor target="_blank">locationDescriptor</a>
    Possible values: any, accessPoint, frontDoorPoint, parcelPoint, rooftopPoint, routingPoint.
* `setBack` - _optional_ - The distance to move the accessPoint away from the curb and towards the inside of the parcel (in metres). Ignored if locationDescriptor not set to accessPoint.
* `brief` - _optional_ - If true, include only basic match and address details in results. Not supported for shp, csv, and gml formats.
* `excludeUnits` - _optional_ - If true, excludes sites that are units of a parent site
* `onlyCivic` - _optional_ - If true, excludes sites without a civic address

### Find the site nearest to a geographic point

> Represents the site nearest a given point

*Tags:* `sites`

#### Input Parameters
* `outputFormat` - _required_ - Results format. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#outputFormat target="_blank">outputFormat</a>
    Possible values: json, geojson, xhtml, kml, gml, csv, shpz.
* `point` - _required_ - Centre point of search. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#point target="_blank">point</a>
* `maxDistance` - _optional_ - The maximum distance (in metres) to search from the given point.  If not specified, the search distance is unlimited.
* `outputSRS` - _optional_ - The EPSG code of the spatial reference system (SRS) to use for output geometries. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#outputSRS target="_blank">outputSRS</a>
    Possible values: 4326, 4269, 3005, 26907, 26908, 26909, 26910, 26911.
* `locationDescriptor` - _optional_ - Describes the nature of the address location. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#locationDescriptor target="_blank">locationDescriptor</a>
    Possible values: any, accessPoint, frontDoorPoint, parcelPoint, rooftopPoint, routingPoint.
* `setBack` - _optional_ - The distance to move the accessPoint away from the curb and towards the inside of the parcel (in metres). Ignored if locationDescriptor not set to accessPoint.
* `brief` - _optional_ - If true, include only basic match and address details in results. Not supported for shp, csv, and gml formats.
* `excludeUnits` - _optional_ - If true, excludes sites that are units of a parent site
* `onlyCivic` - _optional_ - If true, excludes sites without a civic address

### Find sites in a geographic area

> Represents sites within a given area

*Tags:* `sites`

#### Input Parameters
* `outputFormat` - _required_ - Results format. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#outputFormat target="_blank">outputFormat</a>
    Possible values: json, geojson, xhtml, kml, gml, csv, shpz.
* `bbox` - _required_ - A bounding box (xmin,ymin,xmax,ymax) used to limit the search area. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#bbox target="_blank">bbox</a>
* `outputSRS` - _optional_ - The EPSG code of the spatial reference system (SRS) to use for output geometries. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#outputSRS target="_blank">outputSRS</a>
    Possible values: 4326, 4269, 3005, 26907, 26908, 26909, 26910, 26911.
* `maxResults` - _optional_ - The maximum number of search results to return.
* `locationDescriptor` - _optional_ - Describes the nature of the address location. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#locationDescriptor target="_blank">locationDescriptor</a>
    Possible values: any, accessPoint, frontDoorPoint, parcelPoint, rooftopPoint, routingPoint.
* `setBack` - _optional_ - The distance to move the accessPoint away from the curb and towards the inside of the parcel (in metres). Ignored if locationDescriptor not set to accessPoint.
* `brief` - _optional_ - If true, include only basic match and address details in results. Not supported for shp, csv, and gml formats.
* `excludeUnits` - _optional_ - If true, excludes sites that are units of a parent site
* `onlyCivic` - _optional_ - If true, excludes sites without a civic address

### Get a site by its unique ID

> Represents an individual site

*Tags:* `sites`

#### Input Parameters
* `siteID` - _required_ - A unique, but not immutable, site identifier.
* `outputFormat` - _required_ - Results format. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#outputFormat target="_blank">outputFormat</a>
    Possible values: json, geojson, xhtml, kml, gml, csv, shpz.
* `outputSRS` - _optional_ - The EPSG code of the spatial reference system (SRS) to use for output geometries. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#outputSRS target="_blank">outputSRS</a>
    Possible values: 4326, 4269, 3005, 26907, 26908, 26909, 26910, 26911.
* `locationDescriptor` - _optional_ - Describes the nature of the address location. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#locationDescriptor target="_blank">locationDescriptor</a>
    Possible values: any, accessPoint, frontDoorPoint, parcelPoint, rooftopPoint, routingPoint.
* `brief` - _optional_ - If true, include only basic match and address details in results. Not supported for shp, csv, and gml formats.
* `setBack` - _optional_ - The distance to move the accessPoint away from the curb and towards the inside of the parcel (in metres). Ignored if locationDescriptor not set to accessPoint.

### Represents all subsites of a given site

*Tags:* `sites`

#### Input Parameters
* `siteID` - _required_ - A unique, but not immutable, site identifier.
* `outputFormat` - _required_ - Results format. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#outputFormat target="_blank">outputFormat</a>
    Possible values: json, geojson, xhtml, kml, gml, csv, shpz.
* `outputSRS` - _optional_ - The EPSG code of the spatial reference system (SRS) to use for output geometries. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#outputSRS target="_blank">outputSRS</a>
    Possible values: 4326, 4269, 3005, 26907, 26908, 26909, 26910, 26911.
* `locationDescriptor` - _optional_ - Describes the nature of the address location. See <a href=https://github.com/bcgov/api-specs/blob/master/geocoder/glossary.md#locationDescriptor target="_blank">locationDescriptor</a>
    Possible values: any, accessPoint, frontDoorPoint, parcelPoint, rooftopPoint, routingPoint.
* `brief` - _optional_ - If true, include only basic match and address details in results. Not supported for shp, csv, and gml formats.
* `setBack` - _optional_ - The distance to move the accessPoint away from the curb and towards the inside of the parcel (in metres). Ignored if locationDescriptor not set to accessPoint.

## License

**flow**ground :- Telekom iPaaS / gov-bc-ca-geocoder-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
