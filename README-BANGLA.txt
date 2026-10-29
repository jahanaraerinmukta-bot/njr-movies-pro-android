NJR MOVIES PRO — Android APK project
====================================

এই ZIP ফাইলটি APK নয়; এটি Android অ্যাপের source project। APK build করার জন্য GitHub Actions ব্যবহার করা হয়েছে, তাই নিজের কম্পিউটারে Android Studio লাগবে না।

অ্যাপের ফিচার:
- NJR MOVIES PRO নামে Android launcher app
- Splash/loading screen
- ওয়েবসাইটের WebView wrapper
- JavaScript ও local storage সমর্থন (Supabase/TMDB ওয়েব অ্যাপের জন্য)
- Android back button
- বাইরের HTTPS লিংক ব্রাউজারে খোলে

গুরুত্বপূর্ণ:
MainActivity.kt ফাইলে startUrl বর্তমানে https://njrmovies.jahanaraerinmukta.workers.dev/ । যদি আপনার live Cloudflare Pages URL আলাদা হয়, build করার আগে startUrl এবং internal host দুটোই আপনার সঠিক domain অনুযায়ী বদলাতে হবে।

মোবাইল দিয়ে APK বানানোর ধাপ:
1. GitHub-এ sign in করুন এবং নতুন repository তৈরি করুন; নাম দিন NJR-MOVIES-PRO-Android।
2. এই ZIP extract করুন। ভেতরের সব ফাইল/ফোল্ডার repository-র root-এ upload করুন (ZIP-টিকে শুধু ZIP হিসেবেই upload করবেন না)।
3. Commit changes করুন।
4. Repository-র Actions tab খুলুন। “Build NJR MOVIES PRO APK” workflow চলবে।
5. কাজ শেষ হলে Actions > সর্বশেষ সফল run > Artifacts > NJR-MOVIES-PRO-APK ডাউনলোড করুন।
6. ডাউনলোড করা ZIP extract করে app-debug.apk ফোনে খুলুন। Android চাইলে “Install unknown apps” অনুমতি দিন, তারপর Install চাপুন।

বিকল্প: আপনার website PWA হিসেবে install করা যায়। Android Chrome-এ live website খুলে menu > Install app / Add to Home screen চাপলে আলাদা APK ছাড়াই অ্যাপের মতো ব্যবহার করা যাবে।

নিরাপত্তা/ব্যবহার:
- অ্যাপটি আপনার ওয়েবসাইট লোড করে; ওয়েবসাইট/ইন্টারনেট না থাকলে কনটেন্ট আপডেট হবে না।
- Admin login বা Supabase security policy বদলানো হয়নি।
- শুধু নিজের/অনুমোদিত কনটেন্ট প্রকাশ করুন।
- এটি debug APK; Play Store-এর signed release build নয়।
