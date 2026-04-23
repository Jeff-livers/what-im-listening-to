# Design Spec Questionnaire
## "See What I'm Listeneing To" — Personal Music Page

Fill out every answer below. Once complete, hand this doc to Claude Code and it will build the entire project in one shot.

---

## PAGE

1. **Background color?**
   > white

2. **Max content width, or full bleed edge to edge?**
   > boxed width. standard for each viewport

3. **Page padding** (space around the edges on desktop)?
   > standard padding. let it breathe

---

## TYPOGRAPHY

4. **Font?** (Georgia is the default — keeping it, or something different?)
   > Roboto mono

5. **Page title** — font size and weight? ("See What I'm Listeneing To" — keeping the typo?)
   > 64px. regular weight

6. **Page title alignment** — left, center, or right?
   > center

7. **Song title** — font size and weight?
   > 40px regular

8. **Artist name** — font size? Same as album title, smaller, italic?
   > light italic 20px

9. **Font color** (all text, or specify per element)?
   > black

---

## CARD

10. **Card background color?** (teal in your mockup)
    > #2BCEBE

11. **Card border** — color and thickness?
    > black 5px

12. **Card border radius?** (your mockup has rounded corners — keeping them, or hard edges?)
    > 21px

13. **Card drop shadow** — hard neobrutalist (no blur) or soft?
    > 20px x, 20px y, 0 blur

14. **Shadow color?**
    > black_

15. **Shadow offset** — how far does it shift (e.g. 4px, 6px, 8px)?
    > 20px x, 20px y, 0 blur

16. **Padding inside the card?**
    > 40px 20px

17. **Gap between cards?**
    > 40px

---

## ALBUM ART

18. **Image size** — fixed dimensions, or does it scale with the card?
    > 180 x 180 px

19. **Image border** — yes/no, and if yes: color and thickness?
    > white border, 4px stroke.

20. **Image border radius** — rounded corners or hard edges?
    > 14px

---

## LISTEN BUTTON

21. **Button background color?**
    > white

22. **Button text color?**
    > black

23. **Button border** — color and thickness?
    > black 2px

24. **Button border radius** — rounded or hard edges?
    > 10px

25. **Button shadow** — yes/no? If yes, same style as card or different?
    > no shadow

26. **Button font size?**
    > 16px

27. **Button padding** (inside the button — top/bottom and left/right)?
    > 10px, 40px

28. **Where does the button link?** Spotify, Apple Music, YouTube — or does it vary per album?
    > this will be filled out in the json iguess. It would be spotify

---

## LAYOUT

29. **Card layout** — image on the left, then title/artist/button to the right? (confirming your mockup)
    > yes

30. **Mobile layout** — does the image stack on top of the text, or does the card collapse differently?
    > image on top, then normal order. song, album, button

31. **Mobile breakpoint** — at what screen width does it switch to mobile? (default: 600px)
    > default

32. **Header or nav** above the title, or just the title straight at the top?
    > keep it

33. **Footer?** Or does the page just end when the cards end?
    > no footer. jusrt ends

---

## DATA FORMAT

34. **How will you add new albums?** (This determines the data structure Claude Code builds)
    - [ ] Edit a JSON file directly
    - [ ] Edit an array at the top of the HTML file
    - [ ] Other: _______________
    > For this one idk what the best option would be. I want it to be as simple as possible. whatever is easiest to do quickest. 

35. **Sort order** — newest on top, oldest at the bottom. Confirmed?
    > newwest on top yes

36. **Starting songs** — list each one you want to launch with:

```
Song 1:
  Title:Stormy Night
  Artist:Roland Burrell
  Image filename:Images/Stormy Night - Roland Burrell.jpeg
  Listen link:https://open.spotify.com/track/3cQ6hoLs6nN9iRIbSmkIVs
```

---

## TECHNICAL

37. **Deployment target** — Cloudflare Pages. Confirmed?
    > yes

38. **File structure** — standard personal website skill structure:
    ```
    index.html
    albums.json
    Images/
    ```
    Any changes to this?
    > no. I have a notes file with a gitignore in it

39. **JavaScript** — only for reading the JSON file and building the cards. No other JS needed. Confirmed?
    >I think so. as far as I know im not really sure

---

## ANYTHING ELSE

40. **Anything not covered above?** Edge cases, special behavior, notes for Claude Code?
    > Make it just as I say to spec. I was planning on using 11ty. 

---

_Once all fields are filled in, paste this entire document into a Claude Code session and say: "Build this project exactly to spec."_