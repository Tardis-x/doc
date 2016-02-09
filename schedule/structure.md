# The schedule consist of three parts:
- [speakers](#speakers)
- [sessions](#sessions)
- [schedule](#schedule)

# Structure
## Speakers

```
[{
    "id": 1,
    "name": "Name Surname",
    "title": "Software Engineer",
    "company": "Company Name",
    "country": "Ukraine",
    "photoUrl": "/images/people/name_surname.jpg", // Can point to an image on the Internet
    "bio": "Some interesting information about the speaker", // You can write text using Markdown
    "badges": [{
        "name": "GDE",
        "description": "Cloud Google Developer Expert",
        "link": "https://developers.google.com/experts/people"
    }, {
        "name": "GDG",
        "description": "Google Developers Group",
        "link": "https://developers.google.com/groups"
    }],
    "socials": [{
        "name": "Google+",
        "icon": "gplus",
        "link": "https://plus.google.com"
    }, {
        "name": "Twitter",
        "icon": "twitter",
        "link": "https://twitter.com"
    }, {
        "name": "Facebook",
        "icon": "facebook",
        "link": "https://www.facebook.com"
    }, {
        "name": "GitHub",
        "icon": "github",
        "link": "https://github.com"
    }, {
        "name": "LinkedIn",
        "icon": "linkedin",
        "link": "https://linkedin.com"
    }, {
        "name": "Website",
        "icon": "link",
        "link": "http://developers.google.com"
    }]
}]
```


## Sessions

```
[{
    "id": 1001, // Simple session
    "title": "Registration & morning Coffee",
    "description": "Get your badge, coffee, enjoy talking with tech edicts around"
  }, {
    "id": 102, // Complex session
    "title": "Polymer Starter Kit",
    "description": "Information about the session", // You can write text using Markdown
    "speakers": [1], // 'id' of the speaker (can be several)
    "language": "en",
    "complexity": "Intermediate", // Complexity level
    "presentation": "https://speakerdeck.com",
    "video": "https://www.youtube.com",
    "tags": [
        "Web", // The first tag defines the main stream
        "Polymer"
    ]
}]
```


## Schedule

```
[{
    "date": "2015-10-23",
    "dateReadable": "October 23",
    "tracks": [{
        "title": "Expo area"
    }, {
        "title": "Conference hall"
    }, {
        "title": "Community hall"
    }],
    "timeslots": [{
        "startTime": "09:00",
        "endTime": "10:00",
        "sessions": [
            [1001] // 'id' of the session (can be several)
        ]
    }, {
        "startTime": "10:00",
        "endTime": "10:45",
        "sessions": [
            [142] // Shared session between all tracks (takes place in the first one)
        ]
    }, {
        "startTime": "11:00",
        "endTime": "11:45",
        "sessions": [
            [102], //
            [115], // One session per one track
            [128]  //
        ]
    }, {
        "startTime": "12:00",
        "endTime": "12:45",
        "sessions": [
            [103],
            [134],
            [168, 131] // Two sessions in the one track during one time slot
        ]
    }]
}]
```
