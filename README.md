tor-node-map
======

Fetches tor relay information from [https://onionoo.torproject.org/](https://onionoo.torproject.org/). Plots relay nodes as bubbles (circles) with area proportional to their observed bandwidth. The bubbles are plotted on a [kinetic.js](http://kineticjs.com/) canvas, overlayed on top of a [d3.js](http://d3js.org/) map. I did it this way (kinetic/d3 mashup) for better performance. On my machine, panning/zooming more than a few hundred d3 svg elements is too slow. But it can comfortably handle a few thousand canvas sprites. Kinetic provides event handlers on canvas sprites, d3 does not.

Use the map: [http://cdetrio.github.io/tor-node-map/](http://cdetrio.github.io/tor-node-map/)

To fetch latest relay details from onionoo: `wget https://onionoo.torproject.org/details?type=relay -O onionoo-relay-details.json`

To view a local copy: `python -m SimpleHTTPServer`


inspired by 
[jordan-wright/tormap](https://github.com/jordan-wright/tormap)
[http://raidersec.blogspot.com/2013/09/mapping-tor-relays-and-exit-nodes.html](http://raidersec.blogspot.com/2013/09/mapping-tor-relays-and-exit-nodes.html)

Other tor relay maps:
------
[Vidalia Network Map](https://tails.boum.org/doc/anonymous_internet/vidalia/index.en.html#index1h1)

[Vidalia Network Map using Marble 3D Globe](https://blog.torproject.org/blog/technology-preview-marble-and-vidalia020)

[void.gr world map](https://tormap.void.gr/) - [World City Map of Tor Nodes](http://www.void.gr/kargig/blog/2012/11/27/world-city-map-of-tor-nodes/)

[Visualization: Tor nodes on Google Maps and Google Earth](http://moblog.wiredwings.com/archives/20101213/visualization-tor-nodes-on-google-maps-and-google-earth.html)

[Tor exit nodes located and mapped](http://hackertarget.com/tor-exit-node-visualization/)

[Tor V3 consensus servers worldwide](http://freehaven.net/~ioerror/) (long load time)

[endast/Tormap](https://github.com/endast/Tormap/) - [http://bitly.com/tor_map](http://bitly.com/tor_map)
