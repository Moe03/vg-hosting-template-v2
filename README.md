## Example hosting VG script files on github pages
Use the template then it automatically should deploy a github pages then you should be able to access the script files through 
https://yourdomain/assets/styles.css

This repo's link:
https://moe03.github.io/vg-hosting-template-v2/assets/styles.css

Then you replace in the script the root url with your github pages one:
```html
   <script>
        function initVG() {
            window.VG_CONFIG = {
                ID: "YOUR_ID
                region: 'eu', // 'eu' or 'na'corresponding to Europe and North America
                render: 'popup', // popup or full-width
                stylesheets: [
                    // Base Voiceglow CSS
                    "https://moe03.github.io/vg-hosting-template-v2/assets/vg_live_build/styles.css",
                    // Add your custom css stylesheets, Can also add relative URL ('/public/your-file.css)
                ],
                // autostart: true
                // userID: 'USER_ID', // If you want to use your own user_id
                // autostart: true, // Whether to autostart the chatbot with the proactive message
            }
            var VG_SCRIPT = document.createElement("script");
            VG_SCRIPT.src = "https://moe03.github.io/vg-hosting-template-v2/assets/vg_live_build/vg_bundle.js";
            document.body.appendChild(VG_SCRIPT);
        }
        initVG()
    </script>
```

Generated from:
This is a template and some instructions for running Github Pages with the [`minima` theme][minima]. This repo has what I consider the minimum pieces for a personal blog using [Jekyll][jk] and [Github Pages][gh-site]:
