# Playing online (Firebase, free plan)

The game works offline as it is. These steps turn on multiplayer. It takes about 10 minutes and needs no credit card.

## 1. Create the Firebase project
1. Go to https://console.firebase.google.com and sign in with a Google account.
2. **Add project** (any name). You can switch Google Analytics off.
3. In the project, add a **Web app** (the `</>` icon). Skip "Firebase Hosting". Firebase shows a `firebaseConfig` block.

## 2. Turn on the two services
1. **Authentication → Sign-in method → Anonymous → Enable.**
2. **Realtime Database → Create database.** Pick the region closest to you and start in *locked mode*. Copy the database URL it shows (it looks like `https://your-project-default-rtdb.europe-west1.firebasedatabase.app`).

## 3. Paste the rules
In **Realtime Database → Rules**, replace everything with the contents of `database.rules.json` from this folder and press **Publish**. The rules let signed-in players read riders in a room, and each player write only their own rider.

## 4. Put the config into the game
Open `firebase-config.js` and fill in the values from your `firebaseConfig`. Make sure `databaseURL` is included (copy it from step 2 if the config snippet does not show it).

## 5. Play
Open the game (double-click `index.html` or run `python serve.py`). A "PLAY ONLINE?" screen appears. Enter a name and choose PLAY ONLINE. Everyone who uses the same Firebase project and the same location sees each other.

To let friends play, give them this whole folder (with your `firebase-config.js`), or put the folder on any web host. The keys in the config are meant to be public: the rules in step 3 are what protect your database.

## Trying it without Firebase
Open `index.html` through `python serve.py` in two tabs of the same browser and add `?local=1` to the address (for example `http://127.0.0.1:8000/index.html?local=1`). Both tabs can join and see each other, with no internet.

## Good to know
- Free plan limits for the Realtime Database are 100 simultaneous connections and 10 GB of downloads a month. A few friends fit easily. Check the Firebase pricing page for the current numbers.
- Everyone gets about 10 updates a second while moving, and 1 a second while standing still.
- Kickers you move are only moved on your own screen for now.
- Riders can pass through each other.
