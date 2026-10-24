# Lyrics scraper

A small Python notebook that uses LyricsGenius to search Genius for songs by an artist, retrieve their lyrics, clean up whitespace, and save the results to a UTF-8 text file.

The included example searches for songs by Joji. Edit `artist` and `song_titles` to change the search. Song matches depend on Genius search results and should be checked for accuracy.

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

The example saves its results to `joji_lyrics.txt` in the working directory. Requests are spaced one second apart. Search failures are logged by exception type, without printing the full error message.

## Before publishing notebook updates

- Clear all notebook outputs before saving the version you upload.
- Inspect code, markdown, outputs, and metadata for credentials and personal paths.
- Keep tokens and local `.env` files out of the repository.
- Review the actual files selected for upload. `.gitignore` helps with normal Git commands but does not sanitize a file or protect a manually selected browser upload.
- Generated lyrics are not included in this repository. The example output filename is ignored by Git.

Only publish the extracted project files, not your original uncleaned notebook.
