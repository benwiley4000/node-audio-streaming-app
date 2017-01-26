# BenFM

Yo, run this Node app to stream mp3 files from your local machine to a web page on your local network.

```bash
npm install
npm start
```

## specifying directories

Your audio directories should be specified in a file called `.env`. They can be anywhere on your machine - relative or absolute paths.

See `.env.example` - specify a comma-separated list of directories.

```
AUDIO_DIRECTORY=~/Music/MyAudioFiles,/home/User/audio files,audio_mp3s
```

The app will serve all mp3s from:
* `~/Music/MyAudioFiles`
* `/home/User/audio files`
* `audio_mp3s` (within the app directory)

Child directories, however, will not be searched and should be explicitly specified at this time.

Once the server starts, the directory configuration cannot be modified. However, new songs can be added to the music directories, since the list is gathered on each page request.
