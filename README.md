# 🎵 Spotify Streaming History

Spotify user's complete music streaming history data including timestamps, track, artist, and album names, and reasons for playing and ending each track. Goal is to create a visualization that would uncover insights on the user's listening activities.

Original dataset is sourced from [Maven Analytics' Music Challenge](https://mavenanalytics.io/challenges/maven-music-challenge/e161353d-9967-4297-869c-505de168e610) #mavenmusicchallenge

## Data Preparation
- Separated ts into 2 different columns to split date and time.
- Created 3 separate columns to split date and time into hour of the day and day of the week, day of the week number (for sorting purposes).
- Converted playing time from milliseconds to minutes.
- Replaced blank rows in reason columns with "unknown".
- Fixed data type conversion issues on track name and album name for titles with special characters (e.g. 00:00 was uploaded as date 12/31/1899 12:00:00 AM)
- Created a new track id to correspond to the unique combination of track name, artist and album in order to display the # unique tracks metric. Noticed that spotify track uri can have multiple values despite having the same track/artist/album combination (e.g. Closer/Kings of Leon/Only By The Night has 2 track URIs pointing to the same track when searched on Spotify).

## Business Questions
- What/who are the top artists/albums/tracks that the user likes to listen to?
- Is there a pattern to the user's streaming activity?
- Which platform does the user use the most?
- Which track has the most number of skips? Should Spotify start providing insights on songs that are frequently skipped to improve the user's playlist and keep only songs that the users are actually interested in?
- What is the most played song on shuffle mode? Should Spotify improve their algorithm to make the shuffle mode more random?

## Insights
- User is into alternative rock music with artists such as The Killers, The Beatles and John Mayer dominating his playlist chart since 2017.
- We can observe rising streaming activities between 3PM to 6AM indicating that the user's active period might not be the regular 9AM-5PM schedule.
- The user consistently streams music on a daily basis, spending more time on Fridays, with android being the most used platform.
- There were peak streaming activities during 2020-2021 that could potentially be influenced by the pandemic period as people spent more time working from home.
- Overall, the most skipped song is Paraiso with a skip rate of 85.29%. However, this is not indicative that Paraiso is the least favorite song given that the highest skip rate is 100%, suggesting that there are other songs being played but are consistently being skipped. This is an opportunity for Spotify to enhance their customer experience by providing insights to users and offering a chance to revamp their playlists for a much better streaming experience.
- The user enjoys using the shuffle option proven by the profile's shuffle  rate at 74.46%. The most played song on shuffle mode is "In the Blood" (played 125 times) which poses a question on whether Spotify's algorithm is random enough for users to enjoy every variety of the songs on their playlist. Considering that "In the Blood" comprises only 0.11% of all the shuffled songs, we can initially conclude that the randomization is well distributed. An added information on the total number of tracks in the user's playlist can further support and solidify the claim on whether Spotify's randomization algorithm is effective.

## Visualization
Power BI : [Link](https://app.powerbi.com/view?r=eyJrIjoiMzRhM2Q4ZTQtYjdkZC00ZWEyLTgzZjYtZWUzYTBkNzlkNTBmIiwidCI6IjQwMTE5ZDRmLWY1NzQtNGQzNS05MjNkLTA2NjJiNDc0NTRmNyJ9)

![spotify](https://github.com/user-attachments/assets/2e83445a-99ec-4670-9777-295e3fce7a66)



