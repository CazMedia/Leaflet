Leaflet Changelog
=================

## 0.2 (master)

### Highlights

 * Added **WMS support** (`TileLayer.WMS`).
 * Added **different projections support**, having `EPSG:3857`, `EPSG:4326` and `EPSG:3395` out of the box (through `crs` option in `Map`). Thanks to [@Miroff](https://github.com/Miroff) & [@Komzpa](https://github.com/Komzpa) for great advice and explanation regarding this.
 
### Improvements
 
 * Added `TileLayer.Canvas` for easy creation of canvas-based tile layers.
 * `Circle` is now zoom-dependent (with radius in meters); circle of a permanent size is now called `L.CircleMarker`.
 * Added `mouseover` and `mouseout` events to map, markers and paths; added map `mousemove` event.
 * Added `setLatLngs`, `spliceLatLngs`, `addLatLng`, `getLatLngs` methods to polylines and polygons.
 * Added `setLatLng` and `setRadius` methods to `Circle` and `CircleMarker`.
 * `LatLngBounds contains` method now accepts `LatLng` in addition to `LatLngBounds`, the same for `Bounds contains` and `Point` 
 * Added TMS tile numbering support through `TileLayer` `scheme: 'tms'` option (by [@tmcw](https://github.com/tmcw)). 
 * Added `opacity` option to `TileLayer`.
 * Added `setLatLng` method to `Marker`.
 * Added `title` option to `Marker`.
 * Added `maxZoom` argument to `map.locateAndSetView` method.
 * Improved geolocation error handling: better error messages, explicit timeout, set world view on locateAndSetView failure. [#61](https://github.com/CloudMade/Leaflet/issues/61)
 * Improved `LatLngBounds` & `Bounds` to allow their instantiation without arguments (by [@snc](https://github.com/snc)).
 * Improved `debug/leaflet-include.js` script to allow using it outside of `debug` folder (by [@antonj](https://github.com/antonj)).
 * Added `Makefile` for building `leaflet.js` on non-Windows machines (by [@tmcw](https://github.com/tmcw)).
 * Improved `Popup` to accept HTML elements in addition to strings as its content.
 
### Bug fixes
 
 * Disabled zoom animation on Android by default because it's buggy on some devices (will be enabled back when it's stable enough). [#32](https://github.com/CloudMade/Leaflet/issues/32)
 * Fixed a bug where map would occasionally break while multi-touch-zooming on iOS. [#32](https://github.com/CloudMade/Leaflet/issues/32)
 * Fixed a bug where paths would not appear in IE8. 
 * Fixed a bug where zooming is broken if the map contains a polygon and you zoom to an area where it's not visible. [#47](https://github.com/CloudMade/Leaflet/issues/47)
 * Fixed a bug where closed polylines would not appear on the map.
 * Fixed a bug where marker that was added, removed and then added again would not appear on the map. [#66](https://github.com/CloudMade/Leaflet/issues/66)
 * Fixed a bug where some tiles would not load when panning across the date line. [#97](https://github.com/CloudMade/Leaflet/issues/97)
 * Fixed a bug where map div with `position: absolute` is reset to `relative`. [#100](https://github.com/CloudMade/Leaflet/issues/100) 
 * Fixed a bug that caused an error when trying to add a marker without shadow in its icon.
 * Fixed a bug where popup content would not update on `setContent` call. [#94](https://github.com/CloudMade/Leaflet/issues/94)
 * Fixed incorrect zoom animation & popup styling in Opera 11.11.
 * Fixed a bug where double click zoom wouldn't work if popup is opened on map click
 * Fixed a bug with click propagation on popup close button. [#99](https://github.com/CloudMade/Leaflet/issues/99)
 * Fixed a bug where map isn't displayed in Firefox when there's an `img { max-width: 100% }` rule.
 * Fixed inability to remove ImageOverlay layer.
 * Fixed popup fade animation in Firefox and Opera.

## 0.1 (2011-05-13)

 * Initial Leaflet release.