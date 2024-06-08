# Music-Utils

Various utilities for my music setup.

## Usage

```sh
  -save-spotify
        Save Spotify playlists to files
  -to-tidal
        Imports Spotify playlists to Tidal
 -import-navidrome
        Generates Navidrome playlist files from Tidal using Navidrome's database
  -save-tidal
        Save provided Tidal playlists to files
  -process-lidarr-wanted
        Find wanted Lidarr albums on Tidal and save to file
```

## Setup

1. Modify and run the `docker-compose.yml` file. Run `docker compose up`. This will create the config file in `/data/config` for you with the correct keys.
2. Fill in your Spotify client ID and secret in `./data/config/config.json`.
3. Edit the `docker-compose.yml` with the commands you want to run.

## Notes

Attempting to find music between platforms proved to be quite difficult. Tidal does not have an ISRC endpoint leaving me to search track by Title - Artist or Title - Album which can fail due to slight differences in naming between platforms. Any tracks not found during any steps are saved to a file within the `data` directory. A majority of the time these tracks do exist but has a difference causing it to be not found.
