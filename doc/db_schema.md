AcaManager Database Schema
=========================

###Member
> **uid** - A unique identifier
> **username** - Same username as email account

Info
> **firstName** - Member first name
> **lastName** - Member last name
> **year** - Year in school
> **graduationYear** - Year of graduation
> **voicePart** - General voice part
> **hometownCity** - Hometown city
> **hometownState** - Hometown state

Social Media
> **website** - Website url
> **facebook** - Facebook url
> **twitter** - Twitter url

Contact
> **cell** - Cell phone number
> **email** - Non-group email

Roles []
> **roleType** - Role held (music director, etc.)
> **start** - Start date
> **end** - End date

###Repertoire
Song
> **name** - The name of the song
> **obp** - The original producer of the song
> **arranger** - The arranger of the song
> **instrumentation** - Solo, duet, trio/quartet, choir
> **speed** - The speed of the song (default: [ballad, funky, rocker, groove])
> **types** - Type of song (opener, closer, anthem, etc.); can be multiple types
> **partDistribution** - The distribution of parts. Part names are determined by group admin
> > **part1 []** - [uid1, uid2, ...]
> > ...

###Past Repertoire
Song
> **name** - The name of the song
> **obp** - The original producer of the song
> **arranger** - The arranger of the song
> **timePeriod** - The time period the song was performed
> **partDistributions** - The distribution of parts. Part names are determined by group admin. We track any changes to parts and save the old distribution for historical purposes.
> > **timePeriod**
> > > **part1 []** - [uid1, uid2, ...]
> > > ...

###Song Suggestions
Song
> **name** - The name of the song
> **obp** - The original producer of the song
> **performanceLink** - Link to a performance similar to how submitter wants it performed (audio or video)
> **lyricsLink** - Link to the lyrics
> **genre** - Genre of music
> **releaseYear** - The year the song was released
> **adjectives** - Choose from a set of adjectives set by music director (default: [fun, ...])
> **instrumentation** - Solo, duet, trio/quartet, choir
> **speed** - The speed of the song (default: [ballad, funky, rocker, groove])
> **types** - Type of song (opener, closer, anthem, etc.); can be multiple types
> **why** - Long text of reasoning behind wanting to perform the song
> **additionalNotes** - Any notes that don't fall under other categories
> **votes** - Music directors will be able to set their own voting schema. Below is an example yes/no schema:
> > **0 []** A list of votes for 0 (no) [uid1, uid2, ...]
> > **1 []** A list of votes for 1 (yes) [uid1, uid2, ...]
> 
> **comments []** - Any comments people have about a song
> > **uid** - A member's uid
> > **comment** - A text comment
> 
> **chosen** - If the song is chosen, not chosen, or undecided
