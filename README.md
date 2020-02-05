# Flixter
Flixter is an app that allows users to browse movies from the [The Movie Database API](http://docs.themoviedb.apiary.io/#).

📝 `NOTE - PASTE PART 2 SNIPPET HERE:` Paste the README template for part 2 of this assignment here at the top. This will show a history of your development process, which users stories you completed and how your app looked and functioned at each step.

---

## Flix Part 1

### User Stories


#### REQUIRED (10pts)
- [X] (10pts) User can view a list of movies (title, poster image, and overview) currently playing in theaters from the Movie Database API.

#### BONUS
- [X] (2pts) Views should be responsive for both landscape/portrait mode.
   - [X] (1pt) In portrait mode, the poster image, title, and movie overview is shown.
   - [X] (1pt) In landscape mode, the rotated alternate layout should use the backdrop image instead and show the title and movie overview to the right of it.

- [ ] (2pts) Display a nice default [placeholder graphic](https://guides.codepath.org/android/Displaying-Images-with-the-Glide-Library#advanced-usage) for each image during loading
- [X] (2pts) Improved the user interface by experimenting with styling and coloring.
- [ ] (2pts) For popular movies (i.e. a movie voted for more than 5 stars), the full backdrop image is displayed. Otherwise, a poster image, the movie title, and overview is listed. Use Heterogenous RecyclerViews and use different ViewHolder layout files for popular movies and less popular ones.

### App Walkthough GIF

<img src= 'https://i.imgur.com/KBlQEqY.gifv'https://i.imgur.com/KBlQEqY.gifvhttps://i.imgur.com/KBlQEqY.gifvhttps://i.imgur.com/KBlQEqY.gifv width=250><br>

### Notes
Describe any challenges encountered while building the app.

Line 58 under MainActivity.java
When debuging with emulator under variables I had
Connected to the target VM, address:'localhost:8600', transport:'socket' 
and under console in MainActivity I get
Hit json exception
org.json JSONException: No value for results
Fixed by changing .getJsonmArray from "Results" to "results"

Line 58 under MainActivity.java
When debuging with real device after second thttps://portal-prd.humboldt.edu/psp/PAHUMPRD/EMPLOYEE/EMPL/h/?tab=DEFAULTry at debuging under variables I had
this = {MainActivity$1@10261}https://portal-prd.humboldt.edu/psp/PAHUMPRD/EMPLOYEE/EMPL/h/?tab=DEFAULTr
call = {RealCall@10312}
e = {UnknownHOstExcep:Unable@1013} "java.net.UnknownHOstException:Unable to resolve host "api.themoviedb.org": No address associated with hostname"
INTERNAL_ERROR = 500
Fixed by changing .getJsonmArray from "Results" to "results"

When using the Glide library I had 
"error: no suitable method found for into(TextView)method RequestBuilder"
for this line:
Glide.with(context).load(movie.getPosterPath()).into(ivPoster);
"ivPoster" is underlined in red.
Fixed problem by changing ivPoster datatype from textView to imageView


### Open-source libraries used

- [Android Async HTTP](https://github.com/codepath/CPAsyncHttpClient) - Simple asynchronous HTTP requests with JSON parsing
- [Glide](https://github.com/bumptech/glide) - Image loading and caching library for Androids
