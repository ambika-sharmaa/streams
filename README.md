# React app with Redux, Hooks, Google Auth, OBS Streaming
## The App consists of:-

* streams/api - where we fetch and save data (very simple)

* streams/client - the UI where we can create and view streams (note: the Google authorization only handles access to Create, Edit and Delete - without the authorization you can still run the client and watch a stream)

* streams/rtmpserver - hosting the stream from OBS Studio

## and is dependent on (besides the node modules)

* OBS Studio - open source for video streaming and recording

* Google APIs - only for signin with 'gapi.auth2'

## To enable streaming
Start the rtmp server (node-media-server) in a console : streams\rtmpserver> npm start

If not installed, Install OBS Studio - https://obsproject.com/ 

Create a streaming scene, then a Source for display and audio if you want. 
Change settings for stream - File/Settings/Stream

* URL = rtmp://localhost/live

* Stream key = 1 -- note, the stream key must match the id of the stream in the client, example: http://localhost:3000/streams/1 would match on stream key 1

Start streaming (note, you must have started the media server)
