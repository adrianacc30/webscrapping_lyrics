# Lyrics scraper

A small Python notebook that uses LyricsGenius to search Genius for songs by an artist, retrieve their lyrics, clean up whitespace, and save the results to a UTF-8 text file.

Edit `artist` and `song_titles` to change the search. Song matches depend on Genius search results and should be checked for accuracy.

## Run locally

1. Install Python and the dependencies from this folder:

   ```bash
   python -m pip install -r requirements.txt
   ```

2. Get your own Genius API access token from [Genius API clients](https://genius.com/api-clients).
3. Start Jupyter:

   ```bash
   python -m notebook
   ```

4. Open `lyrics_scraper.ipynb` and run its code cell. Enter your token in the hidden prompt. If you have already set a `GENIUS_TOKEN` environment variable, the notebook reads it instead.

Do not type your token into a code cell. The hidden prompt does not save the token as notebook source or output.

The example saves its results to `xyz_lyrics.txt` in the working directory. Requests are spaced one second apart. Search failures are logged by exception type, without printing the full error message.
