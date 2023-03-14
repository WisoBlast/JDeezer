
# JDeezer

Is a Java library that provides access to the Deezer API, allowing developers to search for music tracks, albums, and artists, as well as access information about playlists and users. The library also includes functionality to download music tracks from the Deezer platform.

JDeezer is a remake of the PyDeezer library for Python, with a similar API and functionality.


## Usage
To use JDeezer in your Java code, you will need to create a Deezer object and use its methods to interact with the Deezer API.
```
import com.tools.Deezer;

public class Main {
    public static void main(String[] args) throws Exception {
        String arl = "Your Arl from cookies!";
        Deezer deezer = new Deezer(arl); //login
        String track_id = "781592622";
        String download_dir = "C:\\Users\\User\\Music";
        deezer.get_track(track_id); //get track Id to download it
        deezer.download_track(download_dir, "MP3_128", null);
        //Search
        JSONObject popularPlaylists = deezer.get_popular_playlists();
        System.out.println(popularPlaylists);
        JSONObject getSuggestedInfo = deezer.SearchByQuery("never gonna give you up"); //replace it with the name of the artist or song you want to search for.
        System.out.println(getSuggestedInfo);
```


## Installation
To use JDeezer in your Java project, you will need to add the JDeezer jar file to your project's classpath. You can do this by downloading the latest release from the JDeezer releases page and adding it to your project's dependencies.

## Kotlin Version
A Kotlin version of JDeezer is currently in development, which will provide a more idiomatic interface for Kotlin developers, as well as seamless integration with Android apps. Stay tuned for updates!
