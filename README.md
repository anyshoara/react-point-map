# react-point-map

Base react component for point.map. [Leaflet](http://leafletjs.com/) wrapper in general with very limited configurability.

## Installation

```bash
npm install --save @simpals-dev/react-point-map
```

## General usage

```jsx
import Map, { Marker } from '@simpals-dev/react-point-map';

<Map
  width={800}
  height={600}
>
  <Marker lat={47.0229} lng={28.8353} />
</Map>
```

## Props

```jsx
import Map, { Marker } from '@simpals-dev/react-point-map';

export default () => (
  <Map
    /*
      Number indicating map width in pixels.
    */
    width={800}

    /*
      Number indicating map height in pixels.
    */
    height={600}

    /*
      Number indicating latitude of center map position.
      Default is Main post office of Chisinau.
    */
    lat={47.0229}

    /*
      Number indicating longitude of center map position.
      Default is Main post office of Chisinau.
    */
    lng={28.8353}

    /*
      Number indicating initial map zoom level.
      Minimum is 8, maximum is 20 (19 for retina displays).
    */
    zoom={13}

    /*
      Function that will be run after click on map.
      See: http://leafletjs.com/reference-1.3.0.html#domevent
    */
    onClick={handleMapClick}
  >
    <Marker
      /*
        Number indicating latitude of marker position.
      */
      lat={47.0229}

      /*
        Number indicating longitude of marker position.
      */
      lng={28.8353}

      /*
        Function that will be run after click on marker.
        See: http://leafletjs.com/reference-1.3.0.html#domevent
      */
      onClick={handleMarkerClick}
    />
  </Map>
);
```
