J&H&S Smart Study V4 — AI Image Import

1. Upload all extracted files to the ROOT of your existing GitHub repository. Do not upload the ZIP itself.
2. Existing data uses the same localStorage key as V3 and is not intentionally reset. Make a backup first.
3. Open the AI assistant tab and configure an HTTPS endpoint to your own secure image-analysis backend.
4. This package does NOT include an AI backend. The import cannot analyze images until you connect one.
5. Never embed provider API keys in public GitHub Pages HTML/JS or enter secrets in the endpoint field.
6. The endpoint must accept POST JSON {image_base64,mime_type,kid,type,instruction} and respond with JSON {items:[{kid,type,title,subject,date,notes,score,total}]}. Types: homework,exam,activity,grade. Date: YYYY-MM-DD or empty.
7. Configure CORS to permit your GitHub Pages origin. Protect the backend with authentication, usage limits, and image deletion/no retention.
8. The browser reads the image temporarily and does not store it in localStorage. The image is transmitted to the configured backend, whose retention policy must be checked separately.
9. Check extracted fields carefully before approval; unclear dates should be empty.
