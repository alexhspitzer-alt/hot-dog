# Hot Dog

A static experiment in unlocking sample data by picking a dog. The demo uses a beagle as the correct choice. Wrong picks reshuffle the nine tiles. Lock again clears the revealed message.

Serve the folder over HTTPS, or run `python3 -m http.server 8000` here and open `http://localhost:8000`. No build or dependencies are required. Dog API provides photos, with breed labels available if images fail to load.

The page ships an AES-256-GCM ciphertext and one candidate key per dog. Selecting a tile tries that key with browser Web Crypto. Only the correct key authenticates and decrypts the sample.

The browser receives all nine keys, so anyone who can fetch the page can decrypt the sample. Treat this as a visual puzzle and use sample data.
