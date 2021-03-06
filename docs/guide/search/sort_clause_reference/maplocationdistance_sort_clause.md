# MapLocationDistance Sort Clause

The [`MapLocationDistance` Sort Clause](https://github.com/ezsystems/ezplatform-kernel/blob/v1.0.0/eZ/Publish/API/Repository/Values/Content/Query/SortClause/MapLocationDistance.php)
sorts search results by the distance of the indicated MapLocation Field to the provided location.

## Arguments

- `typeIdentifier` - string representing the identifier of the Content Type to which the MapLocation Field belongs
- `fieldIdentifier` - string representing the identifier of the MapLocation Field to sort by
- `latitude` - float representing the latitude of the location to calculate distance to
- `longitude`- float representing the longitude of the location to calculate distance to
- `sortDirection` (optional) - Query or LocationQuery constant, either `Query::SORT_ASC` or `Query::SORT_DESC`.

## Limitations

The `MapLocationDistance` Sort Clause is not available in [Repository filtering](../../../api/public_php_api_search.md#repository-filtering).

## Example

``` php
$query = new LocationQuery();
$query->sortClauses = [new SortClause\MapLocationDistance('place', 'location', 49.542889, 20.111349)];
```
