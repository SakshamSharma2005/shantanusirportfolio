# Professor Portfolio Website

A modern, professional portfolio website designed for academics, professors, and researchers. Features a dark theme with purple accents, fully responsive design, and smooth animations.

## 🎨 Design Features

- **Dark Theme**: Elegant dark background (#0a0a0a) with purple accents (#8b5cf6)
- **Responsive Design**: Mobile-first approach, works on all devices
- **Smooth Animations**: Fade-in effects, hover states, animated counters
- **Modern Typography**: Inter and Poppins fonts for clean readability
- **Accessibility**: ARIA labels, keyboard navigation, proper contrast

## 📂 Project Structure

```
skportfolio/
├── index.html          # Main HTML file
├── css/
│   └── styles.css      # All styles including responsive design
├── js/
│   └── main.js         # JavaScript functionality
├── images/             # (Add your images here)
└── README.md           # This file
```

## 🚀 Getting Started

### Option 1: Open Directly
Simply double-click `index.html` to open in your browser.

### Option 2: Use Live Server (Recommended)
1. Install VS Code extension "Live Server"
2. Right-click on `index.html` → "Open with Live Server"
3. The site will auto-refresh on changes

### Option 3: Python Server
```bash
# Navigate to the project folder
cd skportfolio

# Python 3
python -m http.server 8000

# Then open http://localhost:8000
```

## ✏️ Customizing Content

### 1. Personal Information (index.html)

**Hero Section - Update your details:**
```html
<!-- Line ~55: Profile Image -->
<img src="YOUR_PHOTO_URL" alt="Your Name" class="profile-image">

<!-- Line ~61: Name -->
<h1 class="hero-name">Your Name</h1>

<!-- Line ~62: Title -->
<p class="hero-title">Your Academic Title</p>

<!-- Line ~64: Institution -->
<p class="hero-institution">
    <i class="fas fa-university"></i>
    Your University, Location
</p>
```

**Statistics (Line ~79):**
```html
<span class="stat-number" data-target="15">0</span>  <!-- Years -->
<span class="stat-number" data-target="120">0</span> <!-- Publications -->
<span class="stat-number" data-target="45">0</span>  <!-- Students -->
```

**Social Links (Line ~69-75):**
Update the `href` attributes with your profiles.

### 2. Research Projects (Line ~160-220)

Each project card:
```html
<article class="research-card">
    <div class="card-image">
        <img src="YOUR_PROJECT_IMAGE" alt="Project Name">
        <div class="card-overlay">
            <span class="card-category">Category</span>
        </div>
    </div>
    <div class="card-content">
        <h3>Project Title</h3>
        <p>Project description...</p>
        <a href="PROJECT_LINK" class="card-link">
            <span>Learn More</span>
            <i class="fas fa-arrow-right"></i>
        </a>
    </div>
</article>
```

### 3. Publications (Line ~280-340)

Each publication:
```html
<article class="publication-item">
    <div class="publication-year">2024</div>
    <div class="publication-content">
        <div class="publication-venue">Conference/Journal Name</div>
        <h3>"Paper Title"</h3>
        <p class="publication-authors">Author1, Author2, & Author3</p>
        <div class="publication-links">
            <a href="PDF_LINK" class="pub-link">
                <i class="fas fa-file-pdf"></i> PDF
            </a>
            <a href="DOI_LINK" class="pub-link">
                <i class="fas fa-link"></i> DOI
            </a>
        </div>
    </div>
</article>
```

### 4. Courses (Line ~420-470)

Each course card:
```html
<div class="course-card">
    <div class="course-code">CS XXX</div>
    <h3>Course Name</h3>
    <p>Course description...</p>
    <div class="course-meta">
        <span><i class="fas fa-calendar"></i> Semester Year</span>
        <span><i class="fas fa-users"></i> Level</span>
    </div>
</div>
```

### 5. Testimonials (Line ~350-400)

```html
<div class="testimonial-card">
    <div class="testimonial-content">
        <p>"Testimonial text..."</p>
    </div>
    <div class="testimonial-author">
        <img src="AUTHOR_PHOTO" alt="Author Name">
        <div class="author-info">
            <h4>Author Name</h4>
            <span>Author Role/Title</span>
        </div>
    </div>
</div>
```

### 6. FAQ Section (Line ~480-530)

```html
<div class="faq-item">
    <button class="faq-question">
        <span>Your Question?</span>
        <i class="fas fa-plus"></i>
    </button>
    <div class="faq-answer">
        <p>Your answer text...</p>
    </div>
</div>
```

### 7. Contact Information (Line ~540-580)

```html
<div class="contact-item">
    <i class="fas fa-envelope"></i>
    <span>your.email@university.edu</span>
</div>
<div class="contact-item">
    <i class="fas fa-map-marker-alt"></i>
    <span>Your Office, Building<br>University Address</span>
</div>
```

## 🎨 Customizing Colors (css/styles.css)

Change the color scheme by editing CSS variables (Line ~10-20):

```css
:root {
    /* Background Colors */
    --bg-primary: #0a0a0a;      /* Main background */
    --bg-secondary: #111111;    /* Section backgrounds */
    --bg-card: #161616;         /* Card backgrounds */
    
    /* Accent Colors - Change these for different themes */
    --purple-primary: #8b5cf6;  /* Main accent */
    --purple-secondary: #a78bfa; /* Lighter accent */
    --purple-dark: #7c3aed;     /* Darker accent */
    
    /* Text Colors */
    --text-primary: #ffffff;    /* Main text */
    --text-secondary: #a1a1aa;  /* Secondary text */
    --text-muted: #71717a;      /* Muted text */
}
```

### Alternative Color Schemes

**Blue Theme:**
```css
--purple-primary: #3b82f6;
--purple-secondary: #60a5fa;
--purple-dark: #2563eb;
```

**Green Theme:**
```css
--purple-primary: #10b981;
--purple-secondary: #34d399;
--purple-dark: #059669;
```

**Orange Theme:**
```css
--purple-primary: #f97316;
--purple-secondary: #fb923c;
--purple-dark: #ea580c;
```

## 📱 Responsive Breakpoints

- **Desktop**: > 1024px
- **Tablet**: 768px - 1024px
- **Mobile**: < 768px
- **Small Mobile**: < 480px

## 🔧 Adding Your Own Images

1. Create an `images` folder in the project root
2. Add your photos (recommended sizes):
   - Profile photo: 400x400px
   - Project thumbnails: 600x400px
   - Testimonial avatars: 100x100px
3. Update image `src` attributes in HTML

### Using Placeholder Images

The template uses Unsplash images. Replace with your own:
```html
<!-- Current placeholder -->
<img src="https://images.unsplash.com/..." alt="...">

<!-- Your image -->
<img src="images/your-photo.jpg" alt="...">
```

## 🚀 Deployment Options

### GitHub Pages (Free)
1. Create a GitHub repository
2. Push your code
3. Go to Settings → Pages
4. Select source branch
5. Your site will be at: `username.github.io/repo-name`

### Netlify (Free)
1. Create account at netlify.com
2. Drag & drop your project folder
3. Get instant deployment URL

### Vercel (Free)
1. Create account at vercel.com
2. Import your GitHub repository
3. Automatic deployments on push

### University Hosting
Contact your IT department for hosting options on university servers.

## 📋 Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers

## 🔍 SEO Optimization

The template includes:
- Semantic HTML5 elements
- Meta description and keywords
- Proper heading hierarchy
- Alt text for images
- Fast loading with lazy images

**Add more SEO (index.html head section):**
```html
<meta property="og:title" content="Dr. Your Name - Professor">
<meta property="og:description" content="Your description">
<meta property="og:image" content="URL to share image">
<meta property="og:url" content="Your website URL">
```

## 📞 Support

For customization help or questions:
1. Check the code comments
2. Refer to CSS class names for styling
3. JavaScript is modular and well-documented

## 📄 License

This template is free to use for personal and commercial projects.

---

**Happy customizing! 🎉**
