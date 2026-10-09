Shonchoy Collection – PWA প্যাকেজ
=================================

ফাইলগুলো
  index.html            → Apps Script অ্যাপকে ফুল-স্ক্রিনে দেখায় (লিঙ্ক ভেতরেই বসানো আছে)
  manifest.webmanifest  → অ্যাপের নাম, রং, আইকন
  sw.js                 → service worker (ইনস্টলের জন্য দরকার)
  icons/                → আইকন (192, 512, maskable, apple-touch, favicon)

ধাপ ১: HTTPS-এ হোস্ট করুন (যেকোনো একটি, ফ্রি)
  • Netlify: app.netlify.com/drop খুলে পুরো ফোল্ডারটা ড্র্যাগ করে ছেড়ে দিন।
  • GitHub Pages: নতুন repo-তে সব ফাইল আপলোড → Settings → Pages → main branch।
  • Firebase Hosting / Cloudflare Pages-ও চলবে।
  ফাইলগুলো অবশ্যই ফোল্ডারের একদম রুটে থাকতে হবে (index.html সবার উপরে)।

ধাপ ২: ফোনে ইনস্টল
  Chrome-এ হোস্ট করা লিঙ্ক খুলে মেনু (⋮) → "Install app" / "Add to Home screen"।

ধাপ ৩ (ঐচ্ছিক): APK বানানো
  pwabuilder.com → হোস্ট করা লিঙ্ক বসান → Start → Package for stores → Android → Generate।
  ডাউনলোড হওয়া ZIP-এর ভেতর APK/AAB থাকবে।

মনে রাখবেন
  • Code.gs-এ ALLOWALL আগে থেকেই আছে – ঠিক আছে।
  • Apps Script নতুন করে Deploy করলে লিঙ্ক বদলাতে পারে ("Manage deployments → Edit → New version" দিলে লিঙ্ক একই থাকে)।
    লিঙ্ক বদলালে index.html-এর APP_URL লাইনটা বদলান।
