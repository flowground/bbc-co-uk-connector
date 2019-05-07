# ![LOGO](logo.png) Radio & Music Services **flow**ground Connector

## Description

A generated **flow**ground connector for the Radio & Music Services API (version 1.0.0).

Generated from: https://api.apis.guru/v2/specs/bbc.co.uk/1.0.0/swagger.json<br/>
Generated at: 2019-05-07T17:39:30+03:00

## API Description

We encapsulate Radio & Music business logic for iPlayer Radio and BBC Music products on all platforms. We add value by reliably providing the right blend of metadata needed by clients.

## Authorization

This API does not require authorization.

## Actions

### Broadcasts

> All broadcasts

*Tags:* `Broadcasts`

#### Input Parameters
* `X-API-Key` - _required_ - API_KEY
* `offset` - _optional_ - Paginated results offset
* `limit` - _optional_ - Paginated results limit
* `service_id` - _optional_ - Filter by Service ID. E.g. bbc_radio_fourfm
* `date` - _optional_ - Filter by date. E.g. 2016-06-17
* `sort` - _optional_ - Sort by provided query. E.g. 'start_at' sorts in ascending order, and '-start_at' sorts in descending order
    Possible values: start_at, -start_at, end_at, -end_at.

### Latest Broadcasts

> Broadcasts for the current day

*Tags:* `Broadcasts`

#### Input Parameters
* `X-API-Key` - _required_ - API_KEY
* `offset` - _optional_ - Paginated results offset
* `limit` - _optional_ - Paginated results limit
* `service_id` - _optional_ - Filter by Service ID. E.g. bbc_radio_fourfm
* `on_air` - _optional_ - Filter what is on air. E.g. 'now' returns current programme being broadcasted.
    Possible values: now, previous, next.
* `next` - _optional_ - Filter what will be on air next in minutes. E.g. '240' returns programmes broadcasted in the next four hurs
* `previous` - _optional_ - Filter what was on air previously in minutes. E.g. '240' returns programmes broadcasted in the previous four hurs
* `sort` - _optional_ - Sort by provided query. E.g. 'start_at' sorts in ascending order, and '-start_at' sorts in descending order
    Possible values: start_at, -start_at, end_at, -end_at.

### Broadcasts by PID

> Find broadcast by PID

*Tags:* `Broadcasts`

#### Input Parameters
* `X-API-Key` - _required_ - API_KEY
* `pid` - _required_ - pid

### List of categories

> Retrieve Categories

*Tags:* `Categories`

#### Input Parameters
* `X-API-Key` - _required_ - API_KEY
* `kind` - _optional_ - Filter by provided query. E.g. 'promoted' returns promoted categories
    Possible values: promoted.

### Category by ID

> Retrieve Categories by ID

*Tags:* `Categories`

#### Input Parameters
* `X-API-Key` - _required_ - API_KEY
* `id` - _required_ - Retrieve information about the category. E.g. 'sport-football-europeanchampionship'

### Collection Members

> Episodes and Clips from Collection

*Tags:* `Collections`

#### Input Parameters
* `X-API-Key` - _required_ - API_KEY
* `pid` - _required_ - pid
* `offset` - _optional_ - Paginated results offset
* `limit` - _optional_ - Paginated results limit

### Homepage Experience

> Homepage Experience

*Tags:* `Experience`

#### Input Parameters
* `X-API-Key` - _required_ - API_KEY

### Popular Artists

> List of Most Popular artists from BBC Music.

*Tags:* `Music`

#### Input Parameters
* `X-API-Key` - _required_ - API_KEY
* `since` - _optional_ - ISO 8601 Date yyyy-mm-dd.  Returns items between given time period and now
* `until` - _optional_ - ISO 8601 Date yyyy-mm-dd.  Returns items between given 'since' and 'until' date params
* `decomposed` - _optional_ - In addition to the overall score, return a list of scores broken down by day N.B Must be used in conjunction with since and/or until and since is >= 31 days
* `offset` - _optional_ - Paginated results offset
* `limit` - _optional_ - Paginated results limit

### Single Artist Popularity

> Popularity Artist By Id

*Tags:* `Music`

#### Input Parameters
* `X-API-Key` - _required_ - API_KEY
* `since` - _optional_ - ISO 8601 Date yyyy-mm-dd.  Returns items between given time period and now
* `until` - _optional_ - ISO 8601 Date yyyy-mm-dd.  Returns items between given 'since' and 'until' date params
* `decomposed` - _optional_ - In addition to the overall score, return a list of scores broken down by day N.B Must be used in conjunction with since and/or until and since is >= 31 days
* `id` - _required_ - MusicBrainz Id - Used to get single resource score

### Popular Playlists

> List of Most Popular playlists from BBC Music.

*Tags:* `Music`

#### Input Parameters
* `X-API-Key` - _required_ - API_KEY
* `since` - _optional_ - ISO 8601 Date yyyy-mm-dd.  Returns items between given time period and now
* `until` - _optional_ - ISO 8601 Date yyyy-mm-dd.  Returns items between given 'since' and 'until' date params
* `decomposed` - _optional_ - In addition to the overall score, return a list of scores broken down by day N.B Must be used in conjunction with since and/or until and since is >= 31 days
* `offset` - _optional_ - Paginated results offset
* `limit` - _optional_ - Paginated results limit

### Single Playlist Popularity

> Popular playlist by Id

*Tags:* `Music`

#### Input Parameters
* `X-API-Key` - _required_ - API_KEY
* `since` - _optional_ - ISO 8601 Date yyyy-mm-dd.  Returns items between given time period and now
* `until` - _optional_ - ISO 8601 Date yyyy-mm-dd.  Returns items between given 'since' and 'until' date params
* `decomposed` - _optional_ - In addition to the overall score, return a list of scores broken down by day N.B Must be used in conjunction with since and/or until and since is >= 31 days
* `id` - _required_ - BBC Music Playlist Id - Used to get single resource score

### Popular Tracks

> List of popular tracks for BBC Music. Filter by time, network, artist, playlist or programme.

*Tags:* `Music`

#### Input Parameters
* `X-API-Key` - _required_ - API_KEY
* `since` - _optional_ - ISO 8601 Date yyyy-mm-dd.  Returns items between given time period and now
* `until` - _optional_ - ISO 8601 Date yyyy-mm-dd.  Returns items between given 'since' and 'until' date params
* `network` - _optional_ - Return items with given Network ID
* `programme` - _optional_ - Items with given Programme Pid
* `artist` - _optional_ - MusicBrainz artist ID
* `decomposed` - _optional_ - In addition to the overall score, return a list of scores broken down by day N.B Must be used in conjunction with since and/or until and since is >= 31 days
* `offset` - _optional_ - Paginated results offset
* `limit` - _optional_ - Paginated results limit

### Single Track Popularity

> Popular Track for BBC Music

*Tags:* `Music`

#### Input Parameters
* `X-API-Key` - _required_ - API_KEY
* `since` - _optional_ - ISO 8601 Date yyyy-mm-dd.  Returns items between given time period and now
* `until` - _optional_ - ISO 8601 Date yyyy-mm-dd.  Returns items between given 'since' and 'until' date params
* `network` - _optional_ - Return items with given Network ID
* `programme` - _optional_ - Items with given Programme Pid
* `artist` - _optional_ - MusicBrainz artist ID
* `decomposed` - _optional_ - In addition to the overall score, return a list of scores broken down by day N.B Must be used in conjunction with since and/or until and since is >= 31 days
* `id` - _required_ - BBC Music Track Id - Used to get single resource score

### Unfollow category

*Tags:* `Personalised Categories`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-API-Key` - _required_ - API_KEY

### List of followed categories

> List of followed categories for a given user.

*Tags:* `Personalised Categories`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-API-Key` - _required_ - API_KEY
* `offset` - _optional_ - Paginated results offset
* `limit` - _optional_ - Paginated results limit

### Follow category

*Tags:* `Personalised Categories`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-API-Key` - _required_ - API_KEY

### Music Exports

> Returns status of all previous third party export actions for a given BBC Music user.

*Tags:* `Music Export`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-Authentication-Provider` - _required_ - Authentication type
* `X-API-Key` - _required_ - API_KEY
* `offset` - _optional_ - Paginated results offset
* `limit` - _optional_ - Paginated results limit

### Music Export Jobs

> All items associated to a users export request

*Tags:* `Music Export`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-Authentication-Provider` - _required_ - Authentication type
* `X-API-Key` - _required_ - API_KEY
* `over16` - _required_ - Boolean age check
* `vendor` - _optional_ - Specify Vendor Jobs
    Possible values: spotify, deezer, youtube, itunes.

### Music Export Jobs

> Create Export Job for a user

*Tags:* `Music Export`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-Authentication-Provider` - _required_ - Authentication type
* `X-API-Key` - _required_ - API_KEY
* `over16` - _required_ - Boolean age check
* `vendor` - _optional_ - Specify Vendor Jobs
    Possible values: spotify, deezer, youtube, itunes.

### Music Export Tracks

> Retrieves vendor and status specific tracks

*Tags:* `Music Export`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-Authentication-Provider` - _required_ - Authentication type
* `X-API-Key` - _required_ - API_KEY
* `over16` - _required_ - Boolean age check
* `offset` - _optional_ - Paginated results offset
* `limit` - _optional_ - Paginated results limit
* `vendor` - _optional_ - Specify Vendor Tracks
    Possible values: spotify, deezer, youtube, itunes.
* `status` - _optional_ - Specify Track status
    Possible values: failed, done, pending.

### Favourite Tracks or Clips

> List of favourited tracks and clips for a given user for BBC Music.

*Tags:* `Music`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-Authentication-Provider` - _required_ - Authentication type
* `X-API-Key` - _required_ - API_KEY
* `offset` - _optional_ - Paginated results offset
* `limit` - _optional_ - Paginated results limit
* `action` - _optional_ - Filters activities based on the type of action
    Possible values: favourited, unfavourited.
* `music-data` - _optional_ - Omits music data from the response, defaults to true

### Favourite Tracks or Clips

> Add multiple tracks and/or clips to a BBC Music user's favourites.<br/>
> <br/>
> N.B. Any HTML tags submitted in metadata will be removed

*Tags:* `Music`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-Authentication-Provider` - _required_ - Authentication type
* `X-API-Key` - _required_ - API_KEY

### Favourite Tracks or Clips

> Update tracks or clips from a BBC Music user favourites.<br/>
> <br/>
> N.B. Any HTML tags submitted in metadata will be removed

*Tags:* `Music`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-Authentication-Provider` - _required_ - Authentication type
* `X-API-Key` - _required_ - API_KEY

### Favourite Tracks or Clips by Type

> List of favourited tracks or clips for a given user for BBC Music.

*Tags:* `Music`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-Authentication-Provider` - _required_ - Authentication type
* `X-API-Key` - _required_ - API_KEY
* `type` - _required_ - Supported Music favourite types: Clips or Tracks
    Possible values: clips, tracks.
* `action` - _optional_ - Filters activities based on the type of action
    Possible values: favourited, unfavourited.
* `offset` - _optional_ - Paginated results offset
* `limit` - _optional_ - Paginated results limit

### Favourite Track or Clip

> Delete track or clip from a BBC Music user favourites.

*Tags:* `Music`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-Authentication-Provider` - _required_ - Authentication type
* `X-API-Key` - _required_ - API_KEY
* `type` - _required_ - Supported Music favourite types: Clips or Tracks
    Possible values: clips, tracks.
* `id` - _required_ - Clip PID or Track ID

### Favourite Track or Clip

> Check to see if a single track or clip entity is in a users favourites - determines UX of add button.

*Tags:* `Music`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-Authentication-Provider` - _required_ - Authentication type
* `X-API-Key` - _required_ - API_KEY
* `type` - _required_ - Supported Music favourite types: Clips or Tracks
    Possible values: clips, tracks.
* `id` - _required_ - Clip PID or Track ID

### Favourite Track or Clip

> Add track or clip to a BBC Music user favourites.<br/>
> <br/>
> N.B. Any HTML tags submitted in metadata will be removed

*Tags:* `Music`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-Authentication-Provider` - _required_ - Authentication type
* `X-API-Key` - _required_ - API_KEY
* `type` - _required_ - Supported Music favourite types: Clips or Tracks
    Possible values: clips, tracks.
* `id` - _required_ - Clip PID or Track ID

### Favourite Track or Clip

> Update tracks or clips from a BBC Music user favourites.<br/>
> <br/>
> N.B. Any HTML tags submitted in metadata will be removed

*Tags:* `Music`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-Authentication-Provider` - _required_ - Authentication type
* `X-API-Key` - _required_ - API_KEY
* `type` - _required_ - Supported Music favourite types: Clips or Tracks
    Possible values: clips, tracks.
* `id` - _required_ - Clip PID or Track ID

### Followed Networks, Categories, Artists, Playlists and Genres

> List of followed networks, categories, artists, playlists and genres for a given user for BBC Music.

*Tags:* `Music`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-Authentication-Provider` - _required_ - Authentication type
* `X-API-Key` - _required_ - API_KEY
* `action` - _optional_ - Filters activities based on the type of action
    Possible values: followed, unfollowed.
* `music-data` - _optional_ - Omits music data from the response, defaults to true
* `music_context` - _optional_ - Specify context to be passed to Music API
    Possible values: events, ivote, music, musicplaylist, programmes, radio, unknown.
* `music_within_uk` - _optional_ - Specify location to be passed to Music API
* `offset` - _optional_ - Paginated results offset
* `limit` - _optional_ - Paginated results limit

### Followed Networks, Categories, Artists, Playlists and Genres

> Add networks, categories, artists, playlists, networks, genres or services in a users follows<br/>
> <br/>
> N.B. Any HTML tags submitted in metadata will be removed

*Tags:* `Music`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-Authentication-Provider` - _required_ - Authentication type
* `X-API-Key` - _required_ - API_KEY
* `action` - _optional_ - Filters activities based on the type of action
    Possible values: followed, unfollowed.
* `music-data` - _optional_ - Omits music data from the response, defaults to true
* `music_context` - _optional_ - Specify context to be passed to Music API
    Possible values: events, ivote, music, musicplaylist, programmes, radio, unknown.
* `music_within_uk` - _optional_ - Specify location to be passed to Music API

### Followed Networks, Categories, Artists, Playlists and Genres

> Update networks, categories, artists, playlists, networks, genres or services in a users follows<br/>
> <br/>
> N.B. Any HTML tags submitted in metadata will be removed

*Tags:* `Music`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-Authentication-Provider` - _required_ - Authentication type
* `X-API-Key` - _required_ - API_KEY
* `action` - _optional_ - Filters activities based on the type of action
    Possible values: followed, unfollowed.
* `music-data` - _optional_ - Omits music data from the response, defaults to true
* `music_context` - _optional_ - Specify context to be passed to Music API
    Possible values: events, ivote, music, musicplaylist, programmes, radio, unknown.
* `music_within_uk` - _optional_ - Specify location to be passed to Music API

### Followed Networks, Categories, Artists, Playlists and Genres by Type

> List of followed networks, categories, artists, playlists, networks, genres, categories or services for a given BBC Music user.

*Tags:* `Music`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-Authentication-Provider` - _required_ - Authentication type
* `X-API-Key` - _required_ - API_KEY
* `type` - _required_ - Supported Music follows types: Playlists, Services, Genres & Artists
    Possible values: playlists, services, networks, genres, categories, artists.
* `action` - _optional_ - Filters activities based on the type of action
    Possible values: followed, unfollowed.
* `music-data` - _optional_ - Omits music data from the response, defaults to true
* `music_context` - _optional_ - Specify context to be passed to Music API
    Possible values: events, ivote, music, musicplaylist, programmes, radio, unknown.
* `music_within_uk` - _optional_ - Specify location to be passed to Music API
* `offset` - _optional_ - Paginated results offset
* `limit` - _optional_ - Paginated results limit

### Followed Network, Category, Artist, Playlist and Genre

> Remove a single network, category, artist, playlist, network, genre or service entity is in a users follows

*Tags:* `Music`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-Authentication-Provider` - _required_ - Authentication type
* `X-API-Key` - _required_ - API_KEY
* `type` - _required_ - Supported Music follows types: Playlists, Services, Genres & Artists
    Possible values: playlists, services, networks, genres, categories, artists.
* `id` - _required_ - Playlists, Services, Networks, Genres, Categories or Artists ID
* `music-data` - _optional_ - Omits music data from the response, defaults to true
* `music_context` - _optional_ - Specify context to be passed to Music API
    Possible values: events, ivote, music, musicplaylist, programmes, radio, unknown.
* `music_within_uk` - _optional_ - Specify location to be passed to Music API

### Followed Network, Category, Artist, Playlist and Genre

> Check to see if a single network, category, artist, playlist, network, genre or service entity is in a users follows - determines UX of add button.

*Tags:* `Music`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-Authentication-Provider` - _required_ - Authentication type
* `X-API-Key` - _required_ - API_KEY
* `type` - _required_ - Supported Music follows types: Playlists, Services, Genres & Artists
    Possible values: playlists, services, networks, genres, categories, artists.
* `id` - _required_ - Playlists, Services, Networks, Genres, Categories or Artists ID
* `music-data` - _optional_ - Omits music data from the response, defaults to true
* `music_context` - _optional_ - Specify context to be passed to Music API
    Possible values: events, ivote, music, musicplaylist, programmes, radio, unknown.
* `music_within_uk` - _optional_ - Specify location to be passed to Music API

### Followed Network, Category, Artist, Playlist and Genre

> Add a single network, category, artist, playlist, network, genre or service entity is in a users follows<br/>
> <br/>
> N.B. Any HTML tags submitted in metadata will be removed

*Tags:* `Music`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-Authentication-Provider` - _required_ - Authentication type
* `X-API-Key` - _required_ - API_KEY
* `type` - _required_ - Supported Music follows types: Playlists, Services, Genres & Artists
    Possible values: playlists, services, networks, genres, categories, artists.
* `id` - _required_ - Playlists, Services, Networks, Genres, Categories or Artists ID
* `music-data` - _optional_ - Omits music data from the response, defaults to true
* `music_context` - _optional_ - Specify context to be passed to Music API
    Possible values: events, ivote, music, musicplaylist, programmes, radio, unknown.
* `music_within_uk` - _optional_ - Specify location to be passed to Music API

### Followed Network, Category, Artist, Playlist and Genre

> Update a single network, category, artist, playlist, network, genre or service entity is in a users follows<br/>
> <br/>
> N.B. Any HTML tags submitted in metadata will be removed

*Tags:* `Music`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-Authentication-Provider` - _required_ - Authentication type
* `X-API-Key` - _required_ - API_KEY
* `type` - _required_ - Supported Music follows types: Playlists, Services, Genres & Artists
    Possible values: playlists, services, networks, genres, categories, artists.
* `id` - _required_ - Playlists, Services, Networks, Genres, Categories or Artists ID
* `music-data` - _optional_ - Omits music data from the response, defaults to true
* `music_context` - _optional_ - Specify context to be passed to Music API
    Possible values: events, ivote, music, musicplaylist, programmes, radio, unknown.
* `music_within_uk` - _optional_ - Specify location to be passed to Music API

### Music Export Preferences

> Remove export preferences (e.g. 3rd party vendors, partner id's) for a given BBC Music user.

*Tags:* `Music Export`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-Authentication-Provider` - _required_ - Authentication type
* `X-API-Key` - _required_ - API_KEY

### Music Export Preferences

> Returns export preferences (e.g. 3rd party vendors, partner id's) for a given BBC Music user.

*Tags:* `Music Export`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-Authentication-Provider` - _required_ - Authentication type
* `X-API-Key` - _required_ - API_KEY

### Music Export Preferences

> Create export preferences (e.g. 3rd party vendors, partner id's) for a given BBC Music user.

*Tags:* `Music Export`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-Authentication-Provider` - _required_ - Authentication type
* `X-API-Key` - _required_ - API_KEY

### Music Export Vendor Preferences

> Remove Vendor specific export preferences (e.g. 3rd party vendors, partner id's) for a given BBC Music user.

*Tags:* `Music Export`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-Authentication-Provider` - _required_ - Authentication type
* `X-API-Key` - _required_ - API_KEY
* `vendor` - _required_ - Supported 3rd Party Vendor
    Possible values: spotify, deezer, youtube, itunes.

### Music Export Vendor Preferences

> Returns vendor specific export preferences for a given BBC Music user.

*Tags:* `Music Export`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-Authentication-Provider` - _required_ - Authentication type
* `X-API-Key` - _required_ - API_KEY
* `vendor` - _required_ - Supported 3rd Party Vendor
    Possible values: spotify, deezer, youtube, itunes.

### Music Export Vendor Preferences

> Create Vendor specific export preferences (e.g. 3rd party vendors, partner id's) for a given BBC Music user.

*Tags:* `Music Export`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-Authentication-Provider` - _required_ - Authentication type
* `X-API-Key` - _required_ - API_KEY
* `vendor` - _required_ - Supported 3rd Party Vendor
    Possible values: spotify, deezer, youtube, itunes.

### Music Export Vendor Preferences

> Update vendor specific export preferences for a given BBC Music user.

*Tags:* `Music Export`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-Authentication-Provider` - _required_ - Authentication type
* `X-API-Key` - _required_ - API_KEY
* `vendor` - _required_ - Supported 3rd Party Vendor
    Possible values: spotify, deezer, youtube, itunes.

### Unfollow network

*Tags:* `Personalised Networks`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-API-Key` - _required_ - API_KEY
* `offset` - _optional_ - Paginated results offset
* `limit` - _optional_ - Paginated results limit

### List of followed networks

> List of followed networks for a given user.

*Tags:* `Personalised Networks`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-API-Key` - _required_ - API_KEY
* `offset` - _optional_ - Paginated results offset
* `limit` - _optional_ - Paginated results limit

### Follow network

*Tags:* `Personalised Networks`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-API-Key` - _required_ - API_KEY
* `offset` - _optional_ - Paginated results offset
* `limit` - _optional_ - Paginated results limit

### Write Play Event

*Tags:* `Personalised Plays`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-API-Key` - _required_ - API_KEY

### Suggested Playspace Container

> Suggested Playspace Container

*Tags:* `Playspace`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-API-Key` - _required_ - API_KEY
* `previous_pid` - _required_ - Clip or Episode PID of the previous or first content item in the Playspace stream.
* `previous_container` - _optional_ - Container ID of the previous container in the Playspace stream.

### Playspace Container by ID

> Playspace Container by ID

*Tags:* `Playspace`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-API-Key` - _required_ - API_KEY
* `id` - _required_ - Playspace Container ID

### Recommended Programmes

> Recommended Programmes from the Audience Platforms' Recomendations Service

*Tags:* `Programmes`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-API-Key` - _required_ - API_KEY
* `offset` - _optional_ - Paginated results offset
* `limit` - _optional_ - Paginated results limit
* `rights` - _required_ - Only return available results for the web/mobile.
    Possible values: web, mobile.

### Favourite Episodes and Clips

> List of favourited episodes and clips for a given user for iPlayer Radio.<br/>
> <br/>
> N.B.  Swagger schemas cannot currently handle multiple combinations of object in an array i.e. a mix of Episode<br/>
> and Clip Summaries so we are defining data as a Programme Summary here.  This will be resolved in V3 with full support for<br/>
>  anyOf https://www.openapis.org/blog/2017/01/24/a-new-year-a-new-specification

*Tags:* `Radio`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-Authentication-Provider` - _required_ - Authentication type
* `X-API-Key` - _required_ - API_KEY
* `offset` - _optional_ - Paginated results offset
* `limit` - _optional_ - Paginated results limit
* `sort` - _optional_ - Sort order for Personalised Radio results
    Possible values: programme_titles, available_from_date, available_to_date.
* `show_all_activity` - _optional_ - Include items which have been 'soft' unfavourited in response. I.e items with UAS type of 'unfavourited'

### Favourite Episodes and Clips

> Add User favourites<br/>
> <br/>
> N.B. Any HTML tags submitted in metadata will be removed

*Tags:* `Radio`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-Authentication-Provider` - _required_ - Authentication type
* `X-API-Key` - _required_ - API_KEY

### Favourite Episodes and Clips

> Update user favourites<br/>
> <br/>
> N.B. Any HTML tags submitted in metadata will be removed

*Tags:* `Radio`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-Authentication-Provider` - _required_ - Authentication type
* `X-API-Key` - _required_ - API_KEY

### Favourite Episodes and Clips by Type

> List of followed 'clips' or 'episode' items for a given iPlayer Radio user<br/>
> <br/>
> N.B.  Swagger schemas cannot currently handle multiple combinations of object in an array i.e. a mix of Episode<br/>
> and Clip Summaries so we are defining data as a Programme Summary here.  This will be resolved in V3 with full support for<br/>
>  anyOf https://www.openapis.org/blog/2017/01/24/a-new-year-a-new-specification

*Tags:* `Radio`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-Authentication-Provider` - _required_ - Authentication type
* `X-API-Key` - _required_ - API_KEY
* `type` - _required_ - Supported Radio favourite types: Clips or Episodes
    Possible values: clips, episodes.
* `sort` - _optional_ - Sort order for Personalised Radio results
    Possible values: programme_titles, available_from_date, available_to_date.
* `show_all_activity` - _optional_ - Include items which have been 'soft' unfavourited in response. I.e items with UAS type of 'unfavourited'
* `offset` - _optional_ - Paginated results offset
* `limit` - _optional_ - Paginated results limit

### Favourite Episode or Clip

> Remove User favourite

*Tags:* `Radio`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-Authentication-Provider` - _required_ - Authentication type
* `X-API-Key` - _required_ - API_KEY
* `type` - _required_ - Supported Radio favourite types: Clips or Episodes
    Possible values: clips, episodes.
* `pid` - _required_ - pid

### Favourite Episode or Clip

> Check to see if a single clip or episode entity is in a users favourites - determines UX of add button.<br/>
> <br/>
> N.B.  Swagger schemas cannot currently handle multiple combinations of object in an array i.e. a mix of Episode<br/>
> and Clip Summaries so we are defining data as a Programme Summary here.  This will be resolved in V3 with full support for<br/>
>  anyOf https://www.openapis.org/blog/2017/01/24/a-new-year-a-new-specification

*Tags:* `Radio`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-Authentication-Provider` - _required_ - Authentication type
* `X-API-Key` - _required_ - API_KEY
* `type` - _required_ - Supported Radio favourite types: Clips or Episodes
    Possible values: clips, episodes.
* `pid` - _required_ - pid
* `show_all_activity` - _optional_ - Include items which have been 'soft' unfavourited in response. I.e items with UAS type of 'unfavourited'

### Favourite Episode or Clip

> Add User favourite<br/>
> <br/>
> N.B. Any HTML tags submitted in metadata will be removed

*Tags:* `Radio`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-Authentication-Provider` - _required_ - Authentication type
* `X-API-Key` - _required_ - API_KEY
* `type` - _required_ - Supported Radio favourite types: Clips or Episodes
    Possible values: clips, episodes.
* `pid` - _required_ - pid

### Favourite Episode or Clip

> Update user favourite<br/>
> <br/>
> N.B. Any HTML tags submitted in metadata will be removed

*Tags:* `Radio`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-Authentication-Provider` - _required_ - Authentication type
* `X-API-Key` - _required_ - API_KEY
* `type` - _required_ - Supported Radio favourite types: Clips or Episodes
    Possible values: clips, episodes.
* `pid` - _required_ - pid

### Followed Brands and Series

> List of favourited brands and series for a given user for iPlayer Radio.<br/>
> <br/>
> N.B.  Swagger schemas cannot currently handle multiple combinations of object in an array i.e. a mix of Episode<br/>
> and Clip Summaries so we are defining data as a Programme Summary here.  This will be resolved in V3 with full support for<br/>
>  anyOf https://www.openapis.org/blog/2017/01/24/a-new-year-a-new-specification

*Tags:* `Radio`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-Authentication-Provider` - _required_ - Authentication type
* `X-API-Key` - _required_ - API_KEY
* `offset` - _optional_ - Paginated results offset
* `limit` - _optional_ - Paginated results limit
* `sort` - _optional_ - Sort order for Personalised Radio results
    Possible values: programme_titles, available_from_date, available_to_date.
* `show_all_activity` - _optional_ - Include items which have been 'soft' unfollowed in response. I.e items with UAS type of 'unfollowed'

### Followed Brands and Series

> Add 'brand' or 'series' items to a users iPlayer Radio follows<br/>
> <br/>
> N.B. Any HTML tags submitted in metadata will be removed

*Tags:* `Radio`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-Authentication-Provider` - _required_ - Authentication type
* `X-API-Key` - _required_ - API_KEY

### Followed Brands and Series

> Update 'brands' or 'series' items from a users iPlayer Radio follows<br/>
> <br/>
> N.B. Any HTML tags submitted in metadata will be removed

*Tags:* `Radio`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-Authentication-Provider` - _required_ - Authentication type
* `X-API-Key` - _required_ - API_KEY

### Followed Brands or Series by Type

> List of followed 'brand' or 'series' items for a given iPlayer Radio user<br/>
> <br/>
> N.B.  Swagger schemas cannot currently handle multiple combinations of object in an array i.e. a mix of Episode<br/>
> and Clip Summaries so we are defining data as a Programme Summary here.  This will be resolved in V3 with full support for<br/>
>  anyOf https://www.openapis.org/blog/2017/01/24/a-new-year-a-new-specification

*Tags:* `Radio`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-Authentication-Provider` - _required_ - Authentication type
* `X-API-Key` - _required_ - API_KEY
* `type` - _required_ - Supported Radio follows types: Brands or Series
    Possible values: brands, series.
* `sort` - _optional_ - Sort order for Personalised Radio results
    Possible values: programme_titles, available_from_date, available_to_date.
* `offset` - _optional_ - Paginated results offset
* `limit` - _optional_ - Paginated results limit
* `show_all_activity` - _optional_ - Include items which have been 'soft' unfollowed in response. I.e items with UAS type of 'unfollowed'

### Followed Brand or Series

> Remove 'brand' or 'series' items from a users iPlayer Radio follows

*Tags:* `Radio`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-Authentication-Provider` - _required_ - Authentication type
* `X-API-Key` - _required_ - API_KEY
* `type` - _required_ - Supported Radio follows types: Brands or Series
    Possible values: brands, series.
* `pid` - _required_ - pid

### Followed Brand or Series

> Check to see if a single brand or series entity is in a users follows - determines UX of add button.

*Tags:* `Radio`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-Authentication-Provider` - _required_ - Authentication type
* `X-API-Key` - _required_ - API_KEY
* `type` - _required_ - Supported Radio follows types: Brands or Series
    Possible values: brands, series.
* `pid` - _required_ - pid

### Followed Brand or Series

> Add 'brand' or 'series' items from a users iPlayer Radio follows<br/>
> <br/>
> N.B. Any HTML tags submitted in metadata will be removed

*Tags:* `Radio`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-Authentication-Provider` - _required_ - Authentication type
* `X-API-Key` - _required_ - API_KEY
* `type` - _required_ - Supported Radio follows types: Brands or Series
    Possible values: brands, series.
* `pid` - _required_ - pid

### Followed Brand or Series

> Update 'brand' or 'series' items from a users iPlayer Radio follows<br/>
> <br/>
> N.B. Any HTML tags submitted in metadata will be removed

*Tags:* `Radio`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-Authentication-Provider` - _required_ - Authentication type
* `X-API-Key` - _required_ - API_KEY
* `type` - _required_ - Supported Radio follows types: Brands or Series
    Possible values: brands, series.
* `pid` - _required_ - pid

### Played Episode or Clip

> Returns mixed episode and clip plays for a given BBC iPlayer radio user.<br/>
> <br/>
> N.B.  Swagger schemas cannot currently handle multiple combinations of object in an array i.e. a mix of Episode<br/>
> and Clip Summaries so we are defining data as a Programme Summary here.  This will be resolved in V3 with full support for<br/>
>  anyOf https://www.openapis.org/blog/2017/01/24/a-new-year-a-new-specification

*Tags:* `Radio`

#### Input Parameters
* `Authorization` - _required_ - Bearer OAUTH_TOKEN
* `X-Authentication-Provider` - _required_ - Authentication type
* `X-API-Key` - _required_ - API_KEY
* `offset` - _optional_ - Paginated results offset
* `limit` - _optional_ - Paginated results limit
* `sort` - _optional_ - Sort order for Personalised Radio results
    Possible values: programme_titles, available_from_date, available_to_date.
* `show_all_activity` - _optional_ - Include expired/unavailable items

### All Podcasts

> Retrieve all Podcasts

*Tags:* `Podcasts`

#### Input Parameters
* `X-API-Key` - _required_ - API_KEY
* `offset` - _optional_ - Paginated results offset
* `limit` - _optional_ - Paginated results limit
* `sort` - _optional_ - Sort order for Podcasts results
    Possible values: title, -title, available_from_date, -available_from_date.
* `network` - _optional_ - Network Master Brand ID (mid)
* `network_url_key` - _optional_ - Network URL key
* `category` - _optional_ - Category ID
* `q` - _optional_ - Search query String
* `coverage` - _optional_ - Local, National or Regional Coverage
    Possible values: local, national, regional.

### Featured Podcasts

> Retrieve featured podcasts

*Tags:* `Podcasts`

#### Input Parameters
* `X-API-Key` - _required_ - API_KEY

### Podcast

> Retrieve data about the podcast with the supplied PID

*Tags:* `Podcasts`

#### Input Parameters
* `X-API-Key` - _required_ - API_KEY
* `pid` - _required_ - pid
* `offset` - _optional_ - Paginated results offset
* `limit` - _optional_ - Paginated results limit

### Podcast Episodes

> Retrieve all episodes for a specific podcast

*Tags:* `Podcasts`

#### Input Parameters
* `X-API-Key` - _required_ - API_KEY
* `pid` - _required_ - pid
* `offset` - _optional_ - Paginated results offset
* `limit` - _optional_ - Paginated results limit

### Networks

> All iPlayer Radio networks - contains business logic for masterbrand and service relationships

*Tags:* `Networks`

#### Input Parameters
* `X-API-Key` - _required_ - API_KEY
* `preset` - _optional_ - Returns all networks needed for iPlayer Radio responsive web navigation
* `international` - _optional_ - Returns all networks available internationally

### Popular Episodes & Clips

> Retrieve Popular Episodes & Clips

*Tags:* `Programmes`

#### Input Parameters
* `X-API-Key` - _required_ - API_KEY
* `type` - _optional_ - Programme type required. Accepts comma separated values
    Possible values: episode, clip, episode,clip.
* `distinct` - _optional_ - Filter by deduplication rule. E.g. 'tleo' returns programmes with distinct top level episode objects
    Possible values: tleo.
* `network` - _optional_ - Filter by network master brand ID (mid). Accepts comma separated values
* `network_url_key` - _optional_ - Filter by network URL key. Accepts comma separated values
* `category` - _optional_ - Filter by category. Accepts comma separated values
* `format` - _optional_ - Filter by format. Accepts comma separated values
* `group` - _optional_ - Filter by group. Accepts comma separated values
    Possible values: tv, radio, tv,radio.
* `media_type` - _optional_ - Filter by programme media type. Accepts comma separated values
    Possible values: audio, video, audio,video.
* `container` - _optional_ - Filter by container. Accepts any pid e.g. brand,series,episode
* `media_set` - _optional_ - Filter by media set name. Accepts comma separated combinations of the following: pc,mobile-download,android-download-high,apple-ios-download-high,mobile-cellular-main,mobile-phone-main,iptv-all
    Possible values: pc, mobile-download, android-download-high, apple-ios-download-high, mobile-cellular-main, mobile-phone-main, iptv-all.
* `q` - _optional_ - Search query String

### Radio programmes

> Provides a paginated list of programmes by PID (brand, series, episode and clip). Accepts various filters and sorting methods.<br/>
> <br/>
> N.B.  Swagger schemas cannot currently handle multiple combinations of object in an array i.e. a mix of Episode<br/>
> and Clip Summaries so we are defining results as an array of Programme Summary here.  This will be resolved in V3 with full support for<br/>
>  anyOf https://www.openapis.org/blog/2017/01/24/a-new-year-a-new-specification

*Tags:* `Programmes`

#### Input Parameters
* `X-API-Key` - _required_ - API_KEY
* `kind` - _optional_ - Filter by provided query. E.g. 'tleo' returns top level objects, ie. brands, orphaned series, and orphaned episodes
    Possible values: tleo.
* `network` - _optional_ - Filter by network master brand ID (mid). Accepts comma separated values
* `network_url_key` - _optional_ - Filter by network URL key. Accepts comma separated values
* `category` - _optional_ - Filter by category id. Accepts comma separated values. See /category endpoint below for the type of response provided
* `sort` - _optional_ - Sort by provided query. E.g. 'title' sorts in ascending order, and -title sorts in descending order
    Possible values: available_from_date, -available_from_date, title, -title.
* `container` - _optional_ - Filter by container. Accepts any brand or series pid
* `type` - _optional_ - Filter by programme type. Accepts comma separated values
    Possible values: brand, series, episode, clip, episode,clip.

### Available radio programme by Pid

> Find programmes by PID (brand, series, episode and clip)<br/>
> <br/>
> N.B.  Swagger schemas cannot currently handle multiple combinations of object in an array i.e. a mix of Episode<br/>
> and Clip Summaries so we are defining results as an array of Programme Summary here.  This will be resolved in V3 with full support for<br/>
>  anyOf https://www.openapis.org/blog/2017/01/24/a-new-year-a-new-specification

*Tags:* `Programmes`

#### Input Parameters
* `X-API-Key` - _required_ - API_KEY
* `pid` - _required_ - pid

## License

**flow**ground :- Telekom iPaaS / bbc-co-uk-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
