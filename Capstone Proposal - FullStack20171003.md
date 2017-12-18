## Capstone Proposal
### Brandon Perard
###### PDX Code Guild FullStack-Day (20171003)

# Title: Music To Video

### Overview
The primary goal of my project is to retrieve playlists from the [Spotify API](https://developer.spotify.com/),
and then utilizing that data to build a music video playlist using the [YouTube API](https://developers.google.com/youtube/iframe_api_reference).

The ability to save and edit playlists and video selection are the other major features that I'd like to round implement.


### Functionality
Utilizing the YouTube media library, the Spotify experience will be enhanced with the following functionality:
* Retrieve & utilize Spotify account data
* Edit and build on account data
* Manually build data set, independent of a Spotify account
* Use data set to interact with YouTube and create an automated media stream
* Ability to customize media stream with manual controls for content selection & interaction
* Store necessary data to replay and share created media streams


### Data Model
Spotify account content
- Access playlists and other content relevant to media stream
  - Store referenced media data, and account specific data(if needed) in separate models
- Combine user input and models to define interaction with YouTube API
- Store stream media data in separate model related to media data model
  - **E.g.** Artist/album/song in one model, videos directly related to song in separate model (most likely many-to-one
    to account individual video preferences)
- Model for grouping/referencing selections into a playlist, while allowing other playlists to utilize data/media used
  in a separate playlist (minimizing need to build new model for redundant data in unique requests)


### Schedule
##### Weeks 0-2
* Develop models based on API functionality
* Structure database and front-end system to build desired experience from both data streams
* Focus and refine project interaction process as model and database structure solidifies

##### Week 3
* Develop front-end to facilitate user interaction with data and media
* Build additional functionality into front-end for further customization & control in UI

##### Week 3.43
* Categorize in-development functionality
  * Necessary: needed for functional product
  * Desired: wanted for current iteration goals
  * Partial: wanted and able to function with partial build
  * Future: ideas saved for addressing after front-end design is solidified
* Use categories to focus production on needed areas
* Focus feature development on functionality, rather than growth

##### Week 4
* Finalize functionality for as many features as possible, following category map for focus
* Sharpen design of the front-end to enhance user experience and facilitate ease of flow


### Stretch & Future Goals
* Research lyrics API options and develop karaoke functionality
* Research options for analyzing media files for larger data set
  * Procedurally generated audio-visual element
  * Strengthen database reach, creating environment for further functionality
    * **E.g.** element matching between songs (BPM sort); new music discovery based on song file, not arbitrary genre,
* Develop "Flappy Bird Part II: Electric Boogaloo" during breaks, make millions, pay someone else to do my coding, win
  Survivor All-Stars, use reality-television stardom as platform for election to starring role on current season of
  America, use season as president to gain invitation to Dancing With the Stars, trip on over-waxed floor, sue ABC

#
#
# It's Alive (planning)
#

Track Model
* Artist
  * featured if listed able to parse from main (key?)
* Title
* Album (key)
* Spotify ID
* Video(s) (key/array)
* Genre
* Length

Album
* Title
* Artist (key)
  * features lists compilation artists
* Release date
* Cover Art

## Style

Intro Page
* Buggles/MTV homage
  * multiple tv/pc screen with multiple (clips?) from versions of "Video Killed"(linked from YouTube) playing
  * lowest quality, on small screens, clicking on screen unmutes the audio and mutes any other page audio
  * can rotate videos from top weekly playlist onto intro page
* Initial playlists
  * MTV first videos playlist (other firsts good)
  * Video countdown playlist archive(either all, or chosen years)
  * Video killed the radio star playlist
    * Buggles, PUSA, Check It Out, VKTRS, Pomplamoose
  * My top music videos
* Top Playlist Jockey
  * Profiles
  * Top playlists earn positions
