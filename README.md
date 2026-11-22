# Fuel Log

A simple calorie and protein tracker for your phone. Snap a photo of your meal and Google's Gemini estimates the calories and protein. You can also type the numbers in yourself, or pick a meal you've saved before.

- **Works offline.** Logging, favourites, targets and trends don't need an internet connection. Only the photo estimates go online.
- **Private by default.** Your log is stored on your own phone, not on a server. Nobody else can see it.
- **No account, no install.** It's a single web page (`index.html`). You can add it to your home screen so it opens like an app.
- **Optional carbs and fat**, if you want more than calories and protein.
- **Activity tracking.** Log workouts and see the calories you burnt counted in your day, and whether you're in a surplus or deficit.

Live site: https://pokealimit.github.io/Fuel-Log/

---

## Getting started

### 1. Open it on your phone

Open the live site link above in your phone's browser.

To make it feel like an app, add it to your home screen:

- **iPhone (Safari):** tap the Share button → **Add to Home Screen**.
- **Android (Chrome):** tap the ⋮ menu → **Add to Home screen** (or **Install app**).

Then always open Fuel Log from that home-screen icon. Your log is saved separately for each browser, so the home-screen app and a Safari tab each keep their own copy.

### 2. Set your daily targets

Go to the **Targets** tab and enter your age, weight and height. Choose your activity level and goal, then tap **Save targets**.

Fuel Log works out a daily calorie and protein target for you. If you already know the numbers you want, open **Use my own numbers instead** and type them in.

### 3. (Optional) Turn on photo estimates

Photo estimates use a free Google Gemini API key. You only need to do this once.

1. In **Targets → Photo estimates**, tap **Get a free key**. It opens Google AI Studio.
2. Sign in with a Google account and create an API key.
3. Copy the key, paste it into the **Gemini API key** box in Fuel Log, and tap **Save & test**.

The test uses Google's cheapest model, so it's quick and doesn't use up the free replies you need for meals. The key is only stored on your phone and is never included in backups.

> **Free tier limits:** Google limits how many free estimates each model gives you per day. Fuel Log starts on **Gemini 3.5 Flash-Lite**. It and **3.1 Flash-Lite** allow far more free estimates per day (around 500 each at the time of writing) than the Flash models (around 20 each). If one model runs out or is busy, pick another in the **Model** menu when logging a meal. On the free tier, Google may use your photos and notes to improve its products.

You can skip this step and type the numbers in yourself.

### 4. (Optional) Track carbs and fat too

In **Targets**, switch on **Enable carbs and fats**. Gemini will then estimate carbs and fat as well. You'll also see carbs and fat targets, bars on the Today screen, and averages in Trends.

Meals you logged before turning this on only have calories and protein. They're shown as "not counted" until you open them and add the carbs and fat.

---

## Everyday use

### Logging a meal

On the **Today** tab:

- **Snap a meal** opens your camera. Gemini looks at the photo and fills in each item with its calories and protein. Adding a short note helps, for example "ate half the rice" or "extra egg".
- **Enter manually** (or the **+** next to a meal) opens the same screen without the camera. Type a description and tap **Estimate with Gemini**, or fill in the numbers yourself.

Check the numbers, choose Breakfast, Lunch, Dinner or Others, and tap **Save**.

Other things you can do on that screen:

- **Shared meal?** Set how many people shared the dish. Enter the whole dish, and Fuel Log logs your share.
- **🔍 next to an item** looks it up on Google if you want to double-check.
- **Model** chooses which Gemini model to use. Your choice is remembered. The two **Flash-Lite** models at the top allow far more free estimates per day. The **Flash** models below them (3.6, 3.8 and latest) may be more accurate on a tricky plate, but you only get a few free estimates a day from each.

### Favourites: log your usual meals in one tap

For meals you eat often, like your morning kopi or your usual chicken rice, save them once and reuse them instead of photographing them every time.

- **To save a favourite:** when logging a meal, tap **☆ Add to favourites** under the meal name.
- **To use one:** open **Enter manually**. Your **★ Favourites** are at the top, with your **Recent** meals below. Tap one, check the numbers, and tap **Save**.
- **To find any meal you've eaten before:** type in the **Search favourites & past meals** box. It searches meal names and the food items in them.
- **To change a favourite:** fill the form from it and change the numbers. The button changes to **★ Update favourite with these numbers**; tap it to save the new numbers. If you only change the numbers for today and don't tap it, the favourite stays as it was.
- **To remove one:** tap **★ In favourites** while it's filled in, or go to **Targets → Favourite meals → Remove**.

### Activity: calories burnt and your calorie balance

Open the **Activity** tab to log exercise.

- **Pick an activity** (running, badminton, gym…) and enter the minutes. Fuel Log estimates the calories burnt from your weight in Targets. If you have a number from your watch or the machine, type it into **Calories burnt** instead.
- For anything not in the list, type its name. It's offered as a quick pick next time.
- Tap a logged activity to edit or delete it.

Burnt calories are added to what you can eat today. The Today ring shows, for example, "823 left of 2,873 · incl. 343 burnt". The **Calorie balance** card shows **eaten − burnt = net**, and whether you're in a **surplus or deficit** against your maintenance calories (the calories you'd burn in a normal day without logged exercise). Maintenance is worked out from your details in Targets. If you haven't entered them, it uses your calorie target instead.

**Count burnt calories (100% / 75% / 50%)** sets how much of what you burn is added back. The activity level you chose in Targets already allows for your usual training, and watches often overestimate. If you log your regular workouts here, 50–75% avoids counting them twice.

> You can't out-train a bad diet. Exercise is great for your health, but it burns fewer calories than most people expect. Eating in moderation is still what makes the difference.

### Editing and past days

- Tap any logged meal to edit or delete it.
- Use the ‹ › arrows at the top of Today to go to earlier days and log meals you missed.

### Trends

The **Trends** tab shows your daily calories and protein for the last week or month against your targets. It also shows averages and how many days you hit your protein target.

### Light and dark mode

Fuel Log follows your phone's light/dark setting. Tap the ☾ / ☀ button at the top right to choose one yourself.

---

## Back up your data (important)

Your log only lives on your phone, in the browser's storage. It can be lost if you clear your browser data or switch phones. On iPhone, iOS may also clear it if you don't open the app for several weeks.

- **Targets → Your data → Export backup** saves a `.json` file. Keep it in Files, iCloud Drive or Google Drive.
- **Import backup** restores a backup file. It replaces the log on the phone with the backup.

Backups include your meals, activities, targets, favourites and settings. They don't include your Gemini key. Backups made by older versions of Fuel Log still import fine. Fuel Log reminds you on the Today screen if you haven't backed up in a while.

---

## Troubleshooting

| Message | What to do |
|---|---|
| *Taking longer than usual* | The estimate is still running, and the timer shows how long it's been. Keep waiting, or pick another **Model** and tap **Try … instead** to switch. |
| *This model is busy right now* | Google's servers are overloaded. Pick a different **Model** and tap **Re-estimate**, or try again in a minute. |
| *This model has used up its free daily limit* | Pick a different **Model**; each has its own daily limit. The Flash-Lite models have the highest limits. Or try again tomorrow. |
| *This model is not available for your key* | Google has retired that model. Pick another one. |
| *Google rejected the API key* | Check the key in **Targets → Photo estimates**, or create a new one in Google AI Studio. |
| My log is empty | Make sure you opened it the same way as before (the home-screen icon, not a browser tab). If the data is gone, use **Import backup**. |

---

## Hosting your own copy

Fuel Log is a single static file, so you can host it yourself for free on GitHub Pages:

1. **Fork** this repository on GitHub.
2. In your fork, go to **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**. Pick the branch and the **/ (root)** folder, then **Save**.
4. After a minute or two it's live at `https://<your-username>.github.io/Fuel-Log/`.

You can also download `index.html` and open it directly in a browser. Photo estimates need an internet connection; everything else works offline.

### How it works

- Everything (HTML, CSS and JavaScript) is in `index.html`. There's no build step and nothing to install.
- Data is kept in the browser's `localStorage`, with a copy in IndexedDB as a safety net.
- Photo estimates call the Gemini API (`generativelanguage.googleapis.com`) directly from your browser, using your own key. No other servers are involved.
