
this is the code for the node.js part at my NDC 2013 talk

# Pipe video to player

## Pipe from file to player
Prerecorded, no slides
Play from file (ytdl.mp4) 
```javascript
videoStream.pipe(player.stdin);
```
## Pipe video from drone to player
Show that droneVideoStream is a stream made of streams
![test slide](https://raw.github.com/bjartwolf/ndc-2013-streams/master/presentation/20130530_123049.jpg)

# Pipe video to file
Show slide
Play back video if time (but not so important, as it's the same as the previous, except possibly corrupt in the end since it's not closed properly
![test slide](https://raw.github.com/bjartwolf/ndc-2013-streams/master/presentation/20130530_123610.jpg)

# Pipe navdata to a database as well
Show the droneDataStream.js 
Using logdata.js
![test slide](https://raw.github.com/bjartwolf/ndc-2013-streams/master/presentation/savenavdata.jpg)
   
# Play back again if time using playDroneData.js
No slides, just piping data out again
Consider using a slowpipe for piping slowly.

# Show facedetection stream
Show slide
Introduce different types in data, JSON objects, buffers, strings 
Very much like an eventemitter with objects (but with pause and buffering etc)

# Introduce Rx  
Can pipe this object-type stream into Rx for processing
(this will break things as buffering and backpressure, this is just a hack I'm doing)
Especially when writing from Rx back into a pipe.... Hopefully someone smart does this one day in a robust way. 




