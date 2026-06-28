Prayas One Student App - Split Files Exporter (Cloudflare R2 Storage Edition)
========================================================================

FILES LIST IN THIS BUNDLE:
1. index.html                   - Main student testing portal (configured to dynamically fetch DB chunks + students database from R2 Storage).
2. 404.html                     - SPA clean-path router fallback redirect (with prayasone.in/Blackbook/A-Word-Test support!).
3. sitemap.xml                  - Automatically compiled XML Sitemap listing all deep URLs for high SEO rank!
4. robots.txt                   - Robots file explicitly linking the Sitemap location to Google crawler bots.
5. students_db.txt              - SEPARATE student authentication database. You can edit/upload this independently anytime!
6. config_part_1.txt, _2.txt... - Database fragment plain text files (to be uploaded to Cloudflare R2).
7. test_questions_*.txt         - Individual exam questions split files (to be uploaded to Cloudflare R2).
8. README.txt                   - This instruction file.

Note: All database fragments (config_part_*.txt files), student accounts (students_db.txt), and questions (test_questions_*.txt files) must be uploaded to Cloudflare R2 Storage so they are accessible at:
https://pub-dc360536e4fb46baa3e3e8719d01793e.r2.dev/students_db.txt
and
https://pub-dc360536e4fb46baa3e3e8719d01793e.r2.dev/config_part_*.txt
and
https://pub-dc360536e4fb46baa3e3e8719d01793e.r2.dev/test_questions_*.txt

HOW TO DEPLOY:
1. Extract/Unzip all files in this ZIP archive.
2. Upload the HTML & XML/TXT files (index.html, 404.html, sitemap.xml, robots.txt) directly into your GitHub repository root.
3. Upload 'students_db.txt', all 'config_part_*.txt' AND 'test_questions_*.txt' files directly into your Cloudflare R2 bucket: 'mocktest-data' (making them public).
4. Enable GitHub Pages in your Repository Settings pointing to the main root folder.

HOW TO USE CLEAN DYNAMIC TEST URLs (prayasone.in/Blackbook/A-Word-Test):
Since GitHub Pages is a static site host, direct refreshes on routes like /Blackbook/A-Word-Test normally throw a 404. 
But thanks to the included '404.html' file, it automatically redirects requests back to index.html with query parameters, which then reinstates the pristine URL in the student's address bar without any error! 
Just make sure '404.html' is uploaded next to 'index.html'!

GOOGLE SITE RANKING & SITEMAP:
The 'sitemap.xml' dynamically indexes all your exams, categories, subcategories, and topics.
When uploaded, submit 'https://prayasone.in/sitemap.xml' in Google Search Console to successfully crawl and index all your testing pages!

The application dynamically fetches and reassembles all segments into memory upon startup via Cloudflare R2 Storage fetches!
