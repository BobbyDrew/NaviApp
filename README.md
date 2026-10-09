# Wake-Up Travel Alarm (Android)

Pick a destination city, set how far away you want to be woken, and lock your phone.
A foreground location service keeps tracking with the screen off or the app in the
background, and rings an alarm notification when you are within your chosen distance.

## Get the APK (no Android Studio needed)

1. Create a new GitHub repository and upload everything in this folder
   (keep the `.github/workflows` folder).
2. Open the **Actions** tab. The **Build APK** workflow runs on every push to `main`.
   You can also run it by hand with **Run workflow**.
3. When it finishes, open the run and download the `wake-up-travel-alarm` artifact (a zip containing the APK).

### Public download link for users
Create a tag; the workflow then attaches the APK to a GitHub Release:

    git tag v1.0.0
    git push origin v1.0.0

Users download `wake-up-travel-alarm.apk` from the repo's **Releases** page,
allow "install unknown apps" for their browser, and install it.

## First-run setup on the phone (important)
- Allow **location** and **notifications** when asked.
- Turn **battery optimization off** for the app (Settings > Apps > Wake-Up Travel Alarm > Battery > Unrestricted).
  Some brands (Xiaomi, Oppo, Vivo, Samsung, OnePlus) kill background apps unless you do this.
- Keep the phone's volume up and Do Not Disturb off, or allow this app's "Arrival alarm" channel to bypass it.

## Notes
- This builds a **debug-signed** APK, which is fine for sharing and sideloading. For the Play Store you need a release keystore.
- Test on a real phone before relying on it for a trip.
