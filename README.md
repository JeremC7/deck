# Talks · deck.marketing-makers.com

Static site. The home page lists every deck; each deck lives in its own folder.

    /                     library of decks (generated from tools/decks.json)
    /<slug>/              audience version, no speaker notes
    /<slug>/speaker/      same deck with the spoken script in its notes

Rebuild from the working folder (passation-deck-helmo):

    python3 tools/build.py . tools/engine-v2.html build/share --share
    python3 tools/build.py . tools/engine-v2.html build/presenter
    python3 tools/site.py github-pages

Then copy build/share into <slug>/ and build/presenter into <slug>/speaker/ (rewriting images/ to ../images/).
