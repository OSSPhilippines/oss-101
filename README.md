# OSS 101 - Introduction to Open Source Software

A beginner-friendly web presentation about Open Source Software (OSS) for students and newcomers.

**Presented by:** [Joff Tiquez](https://jofftiquez.dev)
**Community:** 🇵🇭 Open Source Software PH (OSSPH)

## 🎯 Overview

This 30-minute presentation covers:
- What is OSS and why it matters
- **Why OSS is perfect for new developers** (portfolio building, learning, networking)
- How to get started contributing
- OSS licenses and governance
- Popular OSS projects and communities
- Career benefits and opportunities

**Key Feature:** Each example and topic is broken down into individual slides (100+ slides total), allowing you to:
- Explain each point thoroughly with dedicated time
- Skip slides if you're running short on time
- Deep-dive into specific areas based on audience interest
- Use examples as conversation starters

## 📁 Project Structure

The presentation uses a **JSON-based content system** for easy editing:

```
oss-101/
├── index.html              # HTML template with styles and JavaScript
├── slides.json             # Presentation content (EDIT THIS!)
├── ossph-logo-main-transparent.png
├── Molot.otf
├── README.md
└── index-backup.html       # Original static version (backup)
```

**Key Benefits:**
- ✅ **Separation of Concerns**: Content (JSON) vs Layout (HTML)
- ✅ **Easy Editing**: Edit content without touching HTML/CSS
- ✅ **No Conflicts**: Multiple agents can edit separately
- ✅ **Version Control Friendly**: Clean diffs for content changes

## 🚀 Quick Start

### Option 1: Open Locally with File Protocol
1. Simply open `index.html` in your web browser
2. **Note:** Some browsers block loading JSON files via `file://` protocol
3. If slides don't load, use Option 2 below

### Option 2: Using a Local Server
If you prefer using a local server:

```bash
# Using Python 3
python -m http.server 8000

# Using Python 2
python -m SimpleHTTPServer 8000

# Using Node.js (http-server)
npx http-server

# Using PHP
php -S localhost:8000
```

Then visit: `http://localhost:8000`

## ✏️ Editing Content

### Quick Guide

**To edit presentation content:**
1. Open `slides.json` in your editor
2. Find the topic or slide you want to edit
3. Modify the content following the JSON structure
4. Save and refresh your browser

**To edit layout/styles:**
1. Open `index.html` in your editor
2. Modify CSS in the `<style>` section
3. Modify JavaScript rendering in `<script>` section
4. Save and refresh

### JSON Structure

#### Topic with Slides
```json
{
  "id": "unique-id",
  "title": "Topic Title",
  "slides": [
    {
      "type": "topic-title",  // Section divider
      "title": "Why OSS Matters"
    },
    {
      "type": "content",      // Content slide
      "emoji": "🚀",
      "title": "Innovation",
      "box": {
        "content": "Main message here",
        "list": ["Point 1", "Point 2"]
      },
      "list": [
        {
          "emoji": "💡",
          "text": "Key point with emoji"
        }
      ],
      "note": {
        "text": "Small text at bottom"
      }
    }
  ]
}
```

#### Slide Types

**1. Topic Title Slide** (Section divider)
```json
{
  "type": "topic-title",
  "title": "Section Name",
  "box": {
    "content": "Optional description"
  },
  "note": {
    "text": "Optional note"
  }
}
```

**2. Content Slide** (Regular slide with details)
```json
{
  "type": "content",
  "emoji": "🎯",           // Optional emoji before title
  "title": "Slide Title",
  "box": {                 // Optional box with main content
    "title": "Box title",  // Optional
    "content": "Text here",
    "list": [              // Optional list inside box
      {"emoji": "✅", "text": "Item"},
      "Or just text"
    ]
  },
  "list": [                // Optional list outside box
    {"emoji": "📝", "text": "Point 1"},
    {"emoji": "🔥", "text": "Point 2"}
  ],
  "note": {                // Optional small text at bottom
    "text": "Additional info"
  }
}
```

### Adding a New Topic

```json
{
  "id": "my-new-topic",
  "title": "My New Topic",
  "slides": [
    {
      "type": "topic-title",
      "title": "My New Topic"
    },
    {
      "type": "content",
      "title": "First Point",
      "box": {
        "content": "Explanation here"
      }
    }
  ]
}
```

Add this object to the `topics` array in `slides.json`.

## 🎮 Presentation Controls

### Navigation
- **Next Slide**: Arrow Right, Space, or N
- **Previous Slide**: Arrow Left or P
- **First Slide**: Home
- **Last Slide**: End

### View Options
- **Overview Mode**: Press `ESC` or `O` to see all slides at once
- **Fullscreen**: Press `F`
- **Speaker Notes**: Press `S` (if available)
- **Zoom**: Alt+Click on any element

### Other Controls
- **Slide Number**: Displayed in bottom-right corner
- **Progress Bar**: Shows at bottom of screen

## 📋 Presentation Structure

**Total Slides: 100+ (30-minute presentation)**

The presentation is divided into detailed sections with each topic broken down into individual slides:

### 1. Introduction (~5 min)
- Title slide with OSSPH branding
- What is OSS?
- **You Already Use OSS** (9 slides)
  - Individual slides for: Linux, Android, Firefox, WordPress, VS Code, React/Vue, Python/Node.js, Git

### 2. Why It Matters (~8 min)
- **Why Open Source Matters** (6 slides)
  - Innovation, Security, Cost, Community, Transparency
- **Why Perfect for New Developers** (6 slides)
  - Learn from Real Code, Build Portfolio, Gain Experience, Network & Mentorship, Low Barrier

### 3. Getting Started (~15 min)
- **Step 1: Choose a Project** (1 slide)
- **Step 2: Understand the Project** (6 slides)
  - README.md, CONTRIBUTING.md, CODE_OF_CONDUCT.md, Issues/PRs, Dev Environment
- **Step 3: Make First Contribution** (9 slides)
  - Fork, Clone, Branch, Changes, Commit, Push, Create PR, Respond to Feedback

### 4. Types of Contributions (~12 min)
- **Non-Code Contributions** (5 slides)
  - Documentation, Translations, Design/UX, Bug Reports, Community Support
- **Code Contributions** (5 slides)
  - Bug Fixes, New Features, Tests, Performance, Code Reviews

### 5. Licenses & Governance (~6 min)
- Understanding OSS Licenses (1 slide)
- **Individual License Types** (4 slides)
  - MIT, Apache 2.0, GPL, BSD
- Project Governance (1 slide)

### 6. Popular Projects (~8 min)
- **Beginner-Friendly Projects** (7 slides)
  - freeCodeCamp, First Contributions, Django, React, VS Code, MDN Web Docs
- OSS Communities & Programs (1 slide)

### 7. Career Benefits (~4 min)
- How OSS boosts career
- Real impact statistics
- Career paths

### 8. Best Practices (~3 min)
- Best practices
- Common mistakes to avoid

### 9. Conclusion (~3 min)
- Next steps
- Resources
- Q&A
- Thank you slide

## 🎨 Customization

### Theme
The presentation uses a **clean light theme** with OSSPH brand colors. The light background makes it easier to read in various lighting conditions and looks great when projected.

### Colors
The presentation uses OSSPH brand colors with gradient accents:

```css
:root {
    /* OSSPH Brand Colors */
    --ossph-primary: #0060a0;        /* Primary blue */
    --ossph-purple: #6f42c1;         /* Gradient purple */
    --ossph-pink: #cb6ce6;           /* Gradient pink */
    --ossph-dark: #2c3e50;           /* Dark text */
    --ossph-light: #ffffff;          /* Light backgrounds */
    --ossph-bg-light: #f8f9fa;       /* Subtle background */
    --ossph-text-dark: #2c3e50;      /* Main text color */
}
```

**Visual Elements:**
- **H1 Titles**: Gradient text (blue → purple → pink)
- **H2 Headings**: Primary blue (#0060a0)
- **H3 Subheadings**: Purple (#6f42c1)
- **Boxes**: Subtle gradient backgrounds
- **Code blocks**: Light blue background with purple text

### Logo & Typography
The presentation now includes the official OSSPH branding:

- **Logo**: `ossph-logo-main-transparent.png` - Blue fist design with transparent background
- **Font**: `Molot.otf` - Custom brand font used for all headings (H1, H2, H3)

The logo appears on:
- Title slide (200px width)
- Q&A slide (80px width)
- Thank you slide (80px width)

### Theme
To change the reveal.js theme, replace this line in `index.html`:

```html
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/reveal.js/4.6.0/theme/black.min.css">
```

Available themes: `black`, `white`, `league`, `beige`, `sky`, `night`, `serif`, `simple`, `solarized`, `blood`, `moon`

### Content
Edit the HTML directly to modify slides. Each slide is wrapped in a `<section>` tag:

```html
<section>
    <h2>Slide Title</h2>
    <p>Slide content...</p>
</section>
```

## 💡 Tips for Presenters

### OSSPH Brand Voice
This presentation embodies OSSPH's friendly, approachable style:
- **Be that helpful dev friend** - Explain things like you're helping a friend debug
- **Keep it fun** - Don't be afraid to share memes, jokes, or relatable dev stories
- **Stay encouraging** - We're here to inspire, not intimidate
- **Be genuine** - Show excitement about OSS and first PRs
- **No gatekeeping** - Every question is valid, every contribution matters

Think: *"Bringing snacks to hackathons and staying up late to help debug weird issues"*

### Before the Presentation
- [ ] Test the presentation in your browser
- [ ] Practice navigation controls
- [ ] Check that all links work (if you add any)
- [ ] Prepare examples from your local OSS community
- [ ] Have GitHub.com ready in another tab for live demos

### During the Presentation
- **Pace**: Each example/topic has its own slide for detailed explanation
  - Major sections have intro slides - use these to set context
  - Detail slides allow 1-2 minutes per topic for deep dives
  - You can skip slides if running short on time
- **Engagement**: Ask questions, encourage discussion
  - Each slide is self-contained - easy to pause for questions
  - Use the examples to relate to audience experience
- **Examples**: Use local or relevant examples for your audience
  - "Who has used Linux/Android/VS Code?" - build on their experience
  - Share local success stories from Philippines OSS community
- **Demos**: Consider showing:
  - GitHub project exploration (live demo during "Choose a Project")
  - How to find "good first issue" labels (show real examples)
  - Making a fork and clone (walk through the actual steps)
  - Creating a simple pull request (use First Contributions repo)

### Interactive Elements
Consider adding:
- Live GitHub project exploration
- Show a real pull request workflow
- Demonstrate finding beginner-friendly issues
- Share success stories from your community

## 📚 Additional Resources to Share

Mentioned in the presentation:
- **Find Projects**: github.com/topics, firsttimersonly.com, goodfirstissue.dev
- **Learn More**: opensource.guide, github.com/skills, freecodecamp.org
- **Programs**: Google Summer of Code, Outreachy, Hacktoberfest

## 🛠️ Technical Details

- **Framework**: Reveal.js 4.6.0
- **No Build Process**: Pure HTML/CSS/JS
- **Font**: Molot.otf (OSSPH brand font) loaded locally
- **Logo**: ossph-logo-main-transparent.png (transparent PNG)
- **No External Dependencies**: Font and logo are local files
- **Works Offline**: Fully self-contained presentation
- **Mobile Friendly**: Responsive design
- **Print Friendly**: Use browser print (Ctrl/Cmd + P) to create PDF

## 📝 License

This presentation is open source. Feel free to:
- Use it for your own presentations
- Modify it for your audience
- Share it with others
- Contribute improvements

## 🤝 Contributing

Found a typo or want to improve the content?
1. Edit the `index.html` file
2. Test your changes
3. Share your improvements!

## 📧 Support

If you have questions or suggestions, feel free to open an issue or reach out to the community.

---

**Happy Presenting! 🚀**

Remember: The goal is to inspire newcomers to take their first step in open source. Keep it encouraging, welcoming, and fun!
