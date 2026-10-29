HOLOLAB V15 --- Iron Projection Deck
A browser-based 3D hologram and simulation workspace with a sci-fi
projection-deck interface. HOLOLAB brings interactive 3D scenes,
hologram-style visual effects, hand-gesture controls,
assembly/exploded-view tools, and project save/restore features into a
single HTML experience.
Project type: Single-file browser application
Cost: Free to run locally; optional online features may require
external services or API keys
Status: Personal/experimental project --- test on your own device
before relying on it

✨ Features
3D hologram workspace
- Interactive 3D scene powered by Three.js.
- Hologram/projection-deck styling with sci-fi overlays and visual
  effects.
- Object manipulation controls, including position, rotation, and
  scale on X/Y/Z axes.
- Render/display modes and visual controls for opacity, glow, and
  related effects.
- Assembly and exploded-view controls for inspecting model components.
Hand-gesture controls
- Webcam-based hand tracking using MediaPipe Hands loaded from a CDN.
- SLOW and FAST rotation sensitivity modes.
- Adjustable smoothing to make hand-controlled rotation feel steadier.
- One-hand rotation and pinch-based zoom.
- Two-hand gestures for zoom/orbit interactions.
- Gesture controls require camera permission and a browser that
  supports webcam access.
Graphics and performance
- LOW / BALANCED / HIGH graphics profiles.
- Frame pacing adjustments intended to improve smoothness while
  preserving visual detail.
- Actual performance depends on your GPU, browser, scene complexity,
  and available memory. No device can be guaranteed to have zero lag.
Save, restore, and model workflow
- Save project settings locally in the browser.
- Restore a previously saved scene/settings state.
- Export and import project settings as JSON.
- Existing model/scene workflow and local model-memory tools are
  included in the HTML.
Optional online integrations
Some assistant/model features in the application may depend on external
libraries, online CDNs, provider configuration, or API keys. These are
optional integrations rather than a requirement for opening the basic
HTML interface. Never publish API keys in the HTML file or in a public
repository.
🧰 Tech stack
- HTML5, CSS, and JavaScript
- Three.js for 3D rendering
- MediaPipe Hands for
  browser-based hand tracking
- External CDN assets/libraries and web fonts
Because some dependencies are loaded online, an internet connection may
be needed for all features to load.
🚀 Run locally
1. Download or clone this repository.
2. Keep the HTML file and its filename unchanged unless you also update
   any links or instructions.
3. Open the HTML file in a modern browser such as Chrome or Edge.
For webcam hand tracking, browsers commonly require a secure
context. If direct file:// opening does not allow camera access,
serve the file from localhost or use HTTPS hosting.
Simple local server (optional)
If Python is installed, open a terminal in the folder containing the
HTML file and run:
python -m http.server 8000
Then open:
http://localhost:8000/HOLOLAB_SMOOTH_RENDER_NO_DETAIL_LOSS.html
If you rename the HTML file, use the new filename in the address.
🖐️ Using hand controls
1. Open the project in a supported browser.
2. Allow camera access when prompted.
3. Start/enable hand control in the hand-control panel.
4. Choose SLOW for more controlled rotation or FAST for more
   responsive rotation.
5. Adjust the Smoothing slider to tune the response.
6. Try one-hand rotation, pinch zoom, and two-hand gestures.
Lighting, camera quality, background applications, and device
performance can affect tracking smoothness. Camera input is processed in
the browser; check the page's camera permission if tracking does not
start.
💾 Save and restore
- Use SAVE LOCAL to save supported project settings in the current
  browser.
- Use RESTORE to load the saved local state.
- Use EXPORT JSON to keep a portable backup.
- Use IMPORT JSON to load a previously exported project JSON.
Local browser storage is specific to that browser/profile and can be
cleared by browser settings. Export JSON backups for anything you do not
want to lose. Do not import JSON files from sources you do not trust.
💻 Performance notes
The project is designed to be usable on everyday hardware, but 3D
rendering and webcam tracking are resource-intensive. For a laptop with
4 GB RAM:
- Close unused browser tabs and heavy applications.
- Plug in the laptop when testing longer sessions.
- Start with the BALANCED profile if the browser becomes unstable;
  try LOW if needed.
- Keep the scene complexity reasonable.
- For phones, use a current browser and allow sufficient memory;
  behavior varies by device.
The smooth-render update is intended to improve frame scheduling without
intentionally reducing geometry, textures, shaders, or visual detail. It
cannot eliminate bottlenecks caused by hardware or browser limits.
🔐 Privacy and security
- Webcam hand tracking requires camera permission.
- Do not commit API keys, passwords, personal tokens, or private
  project data to GitHub.
- If using an optional AI provider, configure its key locally in the
  app rather than hardcoding it into a public HTML file.
- Review external CDN/library dependencies before using the project in
  sensitive environments.
🧪 Testing status
The updated HTML file received a JavaScript syntax check for its inline
scripts, and duplicate HTML IDs were checked. A full live browser test
of webcam access, MediaPipe initialization, every 3D interaction, mobile
behavior, and all save/restore paths has not been completed.
Contributions and bug reports should include the browser, device, and
steps to reproduce the issue.
📂 Repository structure
HOLOLAB/
├── README.md
└── HOLOLAB_SMOOTH_RENDER_NO_DETAIL_LOSS.html
🛠️ Troubleshooting
The page opens but the 3D scene is missing - Check your internet
connection because Three.js and some effects are loaded from CDNs. - Try
a current version of Chrome or Edge. - Check the browser console for
load errors.

Hand tracking does not start - Allow camera permission. - Try
localhost or HTTPS instead of opening the file directly. - Check that
the browser can reach the MediaPipe CDN.

The hologram stutters - Close other tabs/apps and test the BALANCED
or LOW profile. - Large scenes, integrated graphics, and camera tracking
can all affect frame rate.

Saved settings are missing - Restore uses the same browser profile's
local storage. - Import your previously exported JSON backup if
available.
🤝 Contributing
Suggestions, bug reports, and improvements are welcome. Please
describe: - Your browser and operating system - Whether you tested on
laptop or mobile - The steps to reproduce the issue - Any console error
message (remove private keys/tokens before sharing)
📜 License
No license has been specified yet. Unless a license is added to this
repository, reuse, redistribution, and modification permissions are not
explicitly granted. Add a license file if you want to define how others
may use the project.
HOLOLAB V15 --- Iron Projection Deck
Explore. Manipulate. Project.
