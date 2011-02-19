# Now Playing

Class that returns information about the current track playing, using the Last.fm API. 

Requires PHP 5.

----

Erik Jansson <erik@eriknow.com>

----
 
For this script to work, you need to apply for a Last.fm API account: http://www.last.fm/api/account
 
----

## Bare bones usage:
 
    require_once 'nowplaying.class.php';
    $nowPlaying = new NowPlaying('YourUsername', 'API-key');
    $playing->setNoTrackPlayingMessage('My custom message!'); // optional
    echo $playing->getNowPlaying();
    
----
 
## Step-by-step usage:

1. Assuming the class file resides in the same directory as your
 script, include it as such: `require_once 'nowplaying.class.php';`

2. Then, instantiate the class: `$nowPlaying = new NowPlaying('Username', 'API key');
 
 - The first parameter is the Last.fm username you want info about.
 - The second parameter is the API key which you will find in your
   API account after signing up: http://www.last.fm/api/account

3. To display the current track playing, call the getNowPlaying() method: `echo $playing->getNowPlaying();`

4. When no music is currently being played, a message will be shown 
   saying so. This message can be customized with `setNoTrackPlayingMessage()`: `$playing->setNoTrackPlayingMessage('emptyness');
   
   Remember to call this method before getNowPlaying(), otherwise your custom
   message won't be used.
   
----
 
If anything is unclear, shoot me an email: erik@eriknow.com
 
Erik Jansson
2011