HISTORY HERO (CLASSROOM EDITION): putting the game online for class games

Class games only work from the game's own web address. Inside Claude, the game
can only play against the computer. Hosting it on GitHub Pages is free and takes
about five minutes, the same way you set up the Hidden Words app.

1. On github.com, make a new public repository named "history-hero-classroom".
2. Choose "uploading an existing file". Drag in index.html from this folder,
   then click "Commit changes".
3. Open Settings, then Pages. Under "Branch", choose "main", then "/ (root)",
   then Save.
4. After about a minute your game is at
   https://YOUR-USERNAME.github.io/history-hero-classroom/

Running a class game
- On the projector computer, open the address and click
  "Teachers: host a class game on this screen". A 5-letter class code appears.
- Students open the same address on their phones or laptops, pick a hero,
  type the code and tap "Join a class game".
- Tip: https://YOUR-USERNAME.github.io/history-hero-classroom/?join=CODE fills in the
  code for them, which is handy for a QR code.
- Choose how many computer rivals to add, then press "Start the game".
- The projector shows the whole map and a live leaderboard. Scroll or press
  +/- to zoom, and drag or use the arrow keys to pan.
- At the end the projector crowns the winner, then shows the final standings
  and the terms the class missed most.

Notes
- No accounts and no server to run. Devices connect directly to each other using
  the free PeerJS service. A few school networks block these direct
  connections. If students can't join, try a phone hotspot or ask IT to allow
  WebRTC.
- If a student's device drops out, the computer plays their hero until they
  come back.
- Keep the projector tab open during the game. It is the referee.

Teacher units (your own questions)
- On the title screen under "Topics in play", choose "+ Write a unit". Write terms
  and definitions, or questions with a correct answer (plus up to 3 wrong ones).
  You can paste a list straight from a spreadsheet.
- Tick only your units for a game on just them, or tick them with the eras to mix
  them in.
- Units are saved in the browser on the computer where you write them. In a class
  game the projector sends them to every student, so students don't need them.
- "Share with another teacher" gives a code that a colleague can paste into
  "Import a unit".

Shared units (load on every device)
- Units listed in the file units.json, next to index.html, load automatically for
  everyone who opens the site, including on school Chromebooks that wipe their
  data. They show up under "Teacher units" marked "Shared".
- Shared units can only be changed by editing units.json on GitHub. Students
  can't change or delete them. Anyone can tap "Shared" to make their own
  editable copy.
- To add one: write the unit in the game, choose Edit, then "Share with another
  teacher", and send the code to Claude to add it. Or edit units.json on
  GitHub yourself (click the file, then the pencil icon). The format is:

  {
    "units": [
      {
        "name": "Mesoamerica Review",
        "kind": "terms",
        "items": [
          ["Tenochtitlan", "Aztec capital built on an island in Lake Texcoco"],
          ["Chinampas", "Floating gardens the Aztecs used to farm"]
        ]
      },
      {
        "name": "Quick Quiz",
        "kind": "qa",
        "items": [
          ["Who wrote the 95 Theses?", "Martin Luther", "John Calvin", "Henry VIII", "Erasmus"]
        ]
      }
    ]
  }

  "terms" items are [term, definition]. "qa" items are [question, correct
  answer, then up to 3 wrong answers]. Each unit needs at least 4 items. Keep
  the commas and brackets exactly as shown. If the file has a mistake, the
  shared units won't load, but the rest of the game still works.
- The Claude artifact version can't read this file, so shared units only appear
  on the GitHub site.

