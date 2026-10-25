# Jahangeer's Math Calculator – Android APK

`app/src/main/assets/index.html` hi poori app hai (WebView me chalti hai).
Push karte hi GitHub Actions APK bana deta hai.

## GUIDE (Hinglish)

### 1. GitHub repo banao
1. github.com par login karo -> **+** -> **New repository**
2. Name: `Calculator-APK` -> **Public/Private** -> **Create repository**

### 2. Files upload karo (browser se)
1. Is zip ko **unzip** karo.
2. Repo page par **Add file -> Upload files**.
3. Unzip kiye hue folder ke **andar ki sab files/folders** drag karo
   (`.github`, `app`, `build.gradle`, `settings.gradle`, `gradle.properties`, `.gitignore`, `README.md`).
   - Dhyan: `.github` hidden folder hota hai. Agar file manager me nahi dikhe to "Show hidden files" ON karo.
   - Agar `.github` upload na ho paaye: **Add file -> Create new file** -> naam likho
     `.github/workflows/build.yml` aur `build.yml` ka content paste karo.
4. **Commit changes** dabao.

### 3. APK build hone do
1. Repo me **Actions** tab kholo -> "Build APK" run chalega (3-5 min).
2. Green tick aaye to us run par click karo.
3. Neeche **Artifacts** me **Calculator-APK** download karo -> zip ke andar `app-debug.apk`.
   (Manual run: Actions -> Build APK -> **Run workflow**.)

### 4. Phone me install
1. `app-debug.apk` phone me bhejo -> tap karo.
2. "Install unknown apps" allow karo -> **Install**.

## Aage update kaise karein
- **index.html badalna**: repo me `app/src/main/assets/index.html` kholo -> pencil (Edit) ->
  paste -> Commit. Naya APK khud ban jayega.
- **Icon badalna**: `app/src/main/res/mipmap-*/ic_launcher.png` replace karo
  (sizes: mdpi 48, hdpi 72, xhdpi 96, xxhdpi 144, xxxhdpi 192 px).
- **App ka naam**: `app/src/main/res/values/strings.xml`.

## Notes
- Download = `Pictures/MathCalculator` me save hota hai; Share = Android share sheet.
- Fonts Google Fonts se aate hain, isliye pehli baar internet chahiye; warna default font dikhega.
- Ye **debug APK** hai (Play Store ke liye nahi). Play Store ke liye signed release build alag se banti hai.

## Agar build fail ho
Actions -> failed run -> red step kholo -> error copy karke bhej do.
