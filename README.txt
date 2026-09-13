CAMBRIDGE PINT FINDER V8 — COMMUNITY MODE

V8 turns “Save the Pub” into a real shared community feature.

WHAT IT DOES
- Users can log a pub visit and optional spend.
- Each visit is stored with an anonymous Supabase user ID.
- The app shows aggregate community visits and reported spend by pub.
- Individual transactions/spend are not shown publicly.
- If Supabase is not configured, the app still works in Personal Mode using local phone storage.

SETUP
1. Create a Supabase project.
2. Enable Anonymous Sign-Ins under Authentication > Providers.
3. Open SQL Editor and run supabase_schema.sql.
4. Copy supabase-config.example.js to supabase-config.js.
5. Put your project URL and anon/publishable key into supabase-config.js.
6. Add this line before the app's main script if your host requires explicit config loading:
   <script src="supabase-config.js"></script>
   (Place it after the Supabase CDN script and before the app script.)
7. Host the folder on a HTTPS web host.
8. Open it on iPhone and use Safari > Share > Add to Home Screen.

IMPORTANT
- Do not use a service_role key in the browser.
- This is a prototype community backend. Before public launch, add abuse/rate limiting, pub IDs instead of names, admin moderation, data retention rules, and monitoring.
- The current pub data remains the Cambridge starter dataset from V7.
