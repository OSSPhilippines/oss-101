# OSS 101 - Introduction to Open Source Software

A beginner-friendly web presentation about Open Source Software (OSS) for students and newcomers.

**Presented by:** [Joff Tiquez](https://jofftiquez.dev)
**Community:** 🇵🇭 Open Source Software PH (OSSPH)

## 🎯 Overview

This presentation covers:
- What is OSS and why it matters
- Real-world examples of OSS you use daily
- Why OSS matters (innovation, security, accessibility, community, transparency)
- Understanding OSS licenses (MIT, Apache, GPL, BSD)
- Hands-on exercise: Creating and reviewing pull requests

**Key Feature:** Each example and topic is broken down into individual slides (~30 slides total), allowing you to:
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
├── README.md               # This file
├── assets/
│   ├── fonts/
│   │   └── Molot.otf      # OSSPH brand font
│   └── images/
│       └── ossph-logo-main-transparent.png
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
- **Scroll Within Slide**: Arrow Down/Up (scrolls content first, then navigates when at top/bottom)

### View Options
- **Overview Mode**: Press `ESC` or `O` to see all slides at once
- **Fullscreen**: Press `F`
- **Speaker Notes**: Press `S` (if available)
- **Zoom**: Alt+Click on any element

### Other Controls
- **Slide Number**: Displayed in bottom-right corner
- **Progress Bar**: Shows at bottom of screen
- **Scrolling**: Slides with overflow content are scrollable

## 📋 Presentation Structure

**Total Slides: ~30 slides**

The presentation is divided into the following sections:

### 1. Introduction
- Title slide with OSSPH branding
- Presenter slide (Joff Tiquez bio)
- What is OSS? (1 slide)

### 2. You Already Use OSS (6 slides)
- Topic introduction
- Individual slides for:
  - Linux - Operating system kernel
  - Firefox - Privacy-focused browser
  - WordPress - Website builder and CMS
  - Visual Studio Code - Code editor
  - Git - Version control system

### 3. Why Open Source Matters (6 slides)
- Topic introduction
- Innovation Through Collaboration
- Enhanced Security
- Cost-Effective & Accessible
- Global Community & Learning
- Transparency & Trust

### 4. Understanding OSS Licenses (7 slides)
- Topic introduction
- How to Tell if Software is Open Source
- MIT License - Simple and permissive
- Apache License 2.0 - With patent protection
- GNU GPL - Copyleft license
- BSD License - Very permissive
- Choosing a License - Quick guide

### 5. Hands-On Exercise (7 slides)
- Topic introduction
- Contribution Workflow - 9-step flowchart
- Creating a Pull Request - Step-by-step guide
- Writing a Good PR Description
- Reviewing a Pull Request
- PR Review Best Practices
- Practice Time - First Contributions repo

### 6. Conclusion
- Q&A slide
- Thank you slide with OSSPH branding

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
The presentation includes official OSSPH branding:

- **Logo**: `assets/images/ossph-logo-main-transparent.png` - Blue fist design with transparent background
- **Font**: `assets/fonts/Molot.otf` - Custom brand font used for all headings (H1, H2, H3)

The logo appears:
- Title slide - 200px width, centered
- As a watermark - Fixed background on content slides (subtle, 5% opacity)
- Watermark is hidden on topic title slides for cleaner presentation

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
  - "Who has used Linux/Firefox/VS Code/Git?" - build on their experience
  - Share local success stories from Philippines OSS community
- **Hands-On Exercise**:
  - Guide participants through the First Contributions repo exercise
  - Live demo: fork, clone, branch, commit, push, create PR
  - Show real PR reviews and how to respond to feedback
  - Use github.com/OSSPhilippines/first-contribution for practice

### Interactive Elements
Consider incorporating:
- Live exploration of OSS projects on GitHub
- Real-time pull request creation demo
- Show actual PR reviews with constructive feedback examples
- Share local OSSPH community success stories
- Live license exploration (show LICENSE files in popular repos)

## 📚 Additional Resources to Share

Referenced in the presentation:
- **Practice PR**: github.com/OSSPhilippines/first-contribution
- **License Guide**: choosealicense.com
- **GitHub Profiles**: github.com/jofftiquez
- **Personal Sites**: jofftiquez.dev

## 🛠️ Technical Details

- **Framework**: Reveal.js 4.6.0
- **No Build Process**: Pure HTML/CSS/JS
- **Content System**: JSON-based dynamic slide loading
- **Font**: Molot.otf (OSSPH brand font) loaded from `assets/fonts/`
- **Logo**: ossph-logo-main-transparent.png from `assets/images/`
- **Features**:
  - Smart scrolling with arrow keys
  - Watermark background (toggles on/off for different slide types)
  - Centered topic title slides
  - Organized assets folder structure
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
1. Edit `slides.json` for content changes
2. Edit `index.html` for layout/styling changes
3. Test your changes in a browser
4. Share your improvements!

## 📧 Support

If you have questions or suggestions, feel free to open an issue or reach out to the community.

---

**Happy Presenting! 🚀**

Remember: The goal is to inspire newcomers to take their first step in open source. Keep it encouraging, welcoming, and fun!
