# PocketHelp

A fully functional web-based platform developed with Calude to support teachers' emotional well-being and foster community connection. PocketHelp provides emotional assessment tools, somatic exercise recommendations, and a Reddit-style community forum where educators can connect, share, and support each other.

## 🚀 Getting Started

### **Installation**
No installation required! This is a standalone web application that runs entirely in your browser.

### **How to Open**

1. **Double-click method:**
   - Navigate to the `2 PocketHelp` folder
   - Double-click `index.html`
   - The app opens in your default browser

2. **Drag & drop method:**
   - Open any modern web browser
   - Drag `index.html` into the browser window

3. **From file menu:**
   - Open your browser
   - File → Open File
   - Select `index.html`

## 👤 Demo Accounts

Try the platform immediately with these pre-configured accounts:

| Role    | Email                      | Password   |
|---------|----------------------------|------------|
| Admin   | admin@pockethelp.com       | admin123   |
| Teacher | teacher@pockethelp.com     | teacher123 |

**Admin privileges:**
- Can delete any post in the community hub
- All standard teacher features

![Main Color: #89cff0](https://via.placeholder.com/100x30/89cff0/ffffff?text=PocketHelp)

## 🌟 Features

### **✅ SECTION 1: Main Page (Home Page)**
After logging in, users see two main options:
- **Emotional Assessment** - Quick mental health check-in
- **Community Hub** - Professional advice and peer support
- Plus a link to **Personal Account**

### **✅ SECTION 2: Emotional Assessment Flow**
When selected, displays:
- Short emotional assessment using **sliders** and **multiple choice** questions
- Based on results, shows one of two outputs:
  - **Somatic exercise suggestions** (breathing, body scan, grounding techniques)
  - **Peer support suggestion** with link to Community Hub

### **✅ SECTION 3: Community Hub (Mock Reddit-Style)**
Lightweight forum using front-end state only:
- ✅ Display posts from mock dataset
- ✅ Create new posts
- ✅ Reply to posts
- ✅ Admin users can delete posts
- ✅ Data stored in localStorage
- 6 specialized categories:
  - 📚 Classroom Management
  - 💪 Student Motivation
  - 💙 Emotional Support
  - 💡 Lesson Ideas
  - 🤝 Staff Relationships
  - 🔥 Burnout Prevention

### **✅ SECTION 4: Account System (Mock Only)**
Simulates two account types:
- **Admin** - Can delete any post
- **Teacher** - Standard user

**Signup collects:**
- ✅ Role selection (Admin or Teacher)
- ✅ Profile picture upload (mock preview only)
- ✅ Background info:
  - Position at school
  - Subject (if relevant)
  - Favorite teaching method
  - Why they joined
- ✅ Login matches stored mock user data

### **✅ SECTION 5: Technical Requirements**
- ✅ Runs in web browser
- ✅ No native iOS code
- ✅ Front-end technology (HTML/CSS/JavaScript)
- ✅ SPA-style navigation
- ✅ Mobile layout styling (max-width: 480px)
- ✅ Front-end state for login, roles, posts, replies, assessment

## ✅ Requirements Verification

## 📱 User Flow

```
Login/Signup
    │
    ├── Sign Up (New User)
    │   └── Account Setup
    │       ├── Profile Picture Upload
    │       ├── Background Information
    │       └── Why You Joined
    │
    └── Login (Existing User)
        │
        └── Main Page
            ├── Emotional Assessment
            │   └── Assessment Results
            │       ├── Somatic Exercises
            │       └── Peer Support Suggestions
            │
            ├── Community Hub
            │   ├── Browse by Category
            │   ├── Create New Post
            │   └── View & Reply to Posts
            │
            └── Personal Account
                └── View Profile Information
```

## 💻 Technical Details

### **Technology Stack**
- Pure HTML5
- CSS3 (embedded)
- Vanilla JavaScript (ES6+)
- No external dependencies
- No backend required

### **Data Persistence**
- Uses browser `localStorage` for all data storage
- Persists between sessions
- Mock database functions for CRUD operations

### **Supported Operations**
- User authentication (login/signup)
- Profile creation and management
- Post creation and viewing
- Reply functionality
- Category filtering
- Admin post deletion
- Emotional assessment with result calculation

### **Browser Compatibility**
Works on all modern browsers:
- Chrome/Edge (v90+)
- Safari (v14+)
- Firefox (v88+)

## 📂 Project Structure

```
2 PocketHelp/
├── index.html          # Complete application (HTML + CSS + JS)
└── README.md           # This file
```

## 🎨 Design Specifications

- **Primary Color:** `#89cff0` (Sky Blue)
- **Layout:** Mobile-first, card-based design
- **Max Width:** 480px
- **Typography:** System fonts for optimal performance
- **UI Components:** Custom buttons, forms, cards, and navigation

## 🔧 Customization

### **Adding Categories**
Edit the `categories` array in the following functions:
- `renderCommunityHubScreen()` (line ~461)
- `renderCreatePostScreen()` (line ~531)

### **Adding Mock Data**
Edit the `initializeData()` function (line ~139) to add more:
- Mock user accounts
- Sample posts
- Sample replies

## 📊 Sample Data Included

- **2 Mock Users** (1 Admin, 1 Teacher)
- **6 Sample Posts** across different categories
- **2 Sample Replies** to demonstrate conversation threads

## 🎬 Feature Demonstration

### **Test the Emotional Assessment:**
1. Log in as `teacher@pockethelp.com`
2. Click "Emotional Assessment."
3. **Try high stress scenario**: Set stress to 8+, energy to 3 or less
   - Result: You'll see **somatic exercise suggestions**
4. **Try support scenario**: Select "Yes, I could use some suppor.t"
   - Result: You'll see **peer support recommendation** with link to Community Hub

### **Test the Community Hub:**
1. Click "Community Hub" from the Main Page
2. **Filter by category**: Click any category button (e.g., "Emotional Support")
3. **View a post**: Click on any post card
4. **Add a reply**: Type in the reply box and submit
5. **Create new post**: Click "+ Create New Post", fill form, submit

### **Test Admin Features:**
1. Log out and log in as `admin@pockethelp.com`
2. Go to Community Hub
3. Click any post
4. **Notice**: A red "Delete Post" button appears (admin only)
5. Click to delete (with confirmation)

### **Test Account Creation:**
1. Log out
2. Click "Sign Up."
3. Fill in basic info (name, email, password, role)
4. **Account Setup Page**:
   - Click "Choose Profile Picture" to uploadan  image (preview only)
   - Fill in position, subject, teaching method
   - Write why you joined
5. Complete setup to access the platform

### **Test Data Persistence:**
1. Create a new post in Community Hub
2. Close the browser tab
3. Reopen `index.html.`
4. Log back in
5. **Verify**: Your post is still there (localStorage persistence)

## 🔐 Security Notes

⚠️ **This is a front-end only demonstration app for MVP purpose:**
- No real authentication security
- Data stored in browser localStorage (unencrypted)
- Passwords stored in plain text
- **Not suitable for production use without a proper backend**

For production deployment, consider:
- Backend authentication (JWT, OAuth)
- Encrypted database storage
- Input sanitization and validation
- HTTPS deployment
- Rate limiting and security headers

## 🎯 Use Cases

- **Teacher Wellbeing Programs:** Provide emotional support resources to educators
- **School District Initiatives:** Foster community among staff members
- **Professional Development:** Share teaching strategies and classroom management tips
- **Mental Health Support:** Offer self-assessment tools and coping strategies
- **Peer Support Networks:** Create safe spaces for teacher conversations

## 📝 Features Roadmap

Potential future enhancements:
- [ ] Private messaging between users
- [ ] Push notifications for replies
- [ ] Advanced post search and filtering
- [ ] User reputation/karma system
- [ ] Favorite/bookmark posts
- [ ] Rich text editor for posts
- [ ] Image uploads in posts
- [ ] Weekly wellness challenges
- [ ] Resource library
- [ ] Integration with professional development tracking

## 📄 License

This project is provided as-is for educational and demonstration purposes.

---

**Built with ❤️ for educators everywhere**

*Remember: Your wellbeing matters. Take care of yourself so you can take care of others.*
