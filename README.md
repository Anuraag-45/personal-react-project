# DevConnector 2.0 🚀

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:667eea,100:764ba2&height=200&section=header&text=DevConnector%202.0&fontSize=60&fontColor=fff&animation=twinkling" />

### 🌐 **Professional Social Network for Developers**
*Built with Modern MERN Stack Architecture*

<br/>

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)](https://choosealicense.com/licenses/mit/)
[![MERN Stack](https://img.shields.io/badge/Stack-MERN-blue?style=for-the-badge&logo=react&logoColor=white)](https://reactjs.org/)
[![Node.js](https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white)](https://nodejs.org/)
[![MongoDB](https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white)](https://www.mongodb.com/)

**Developed by [Anuraag Koyalkar](https://github.com/anuraagkoyalkar) | Software Engineer**

</div>

---

## 🎯 **Project Overview**

DevConnector 2.0 is a comprehensive social networking platform designed specifically for developers to connect, share experiences, and showcase their professional journey. This full-stack application demonstrates advanced MERN stack development with modern best practices, including JWT authentication, Redux state management, and responsive design.

<div align="center">

### 🔥 **Key Features Showcase**

</div>

<table width="100%">
<tr>
<td width="50%">

### 👤 **User Management System**
- 🔐 **JWT Authentication** with secure token management
- 👨‍💻 **Developer Profiles** with GitHub integration
- 📧 **Gravatar Integration** for profile pictures
- 🔒 **Protected Routes** and authorization

### 💼 **Professional Networking**
- 📝 **Experience & Education** timeline management
- 🏢 **Company Profiles** and professional history
- 🌐 **Social Media Links** integration
- ⭐ **Skills & Technologies** showcase

</td>
<td width="50%">

### 💬 **Community Features**
- 📱 **Discussion Forum** with threaded comments
- 👍 **Like & Comment System** for engagement
- 📊 **Real-time Updates** and notifications
- 🗑️ **Content Management** (CRUD operations)

### 🛠️ **Technical Excellence**
- ⚡ **Responsive Design** across all devices
- 🔄 **Redux State Management** for scalability
- 🎨 **Modern UI/UX** with Bootstrap styling
- 🚀 **Optimized Performance** and loading states

</td>
</tr>
</table>

---

## 🏗️ **Architecture & Technology Stack**

<div align="center">

### **Frontend Architecture**
<img src="https://skillicons.dev/icons?i=react,redux,html,css,bootstrap,js&theme=dark" />

### **Backend Architecture** 
<img src="https://skillicons.dev/icons?i=nodejs,express,mongodb,jwt&theme=dark" />

### **Development Tools**
<img src="https://skillicons.dev/icons?i=git,github,vscode,postman&theme=dark" />

</div>

<table width="100%">
<tr>
<td width="33%" valign="top">

### **🎨 Frontend Technologies**

```yaml
Core Framework:
  - React 18+ with Hooks
  - Redux for State Management
  - React Router v6 for Navigation
  - Axios for API Communication

UI & Styling:
  - Bootstrap 5 for Responsive Design
  - Custom CSS3 Animations
  - FontAwesome Icons
  - Modern JavaScript (ES6+)

Developer Experience:
  - Component-based Architecture
  - Custom Hooks Implementation
  - Error Boundary Components
  - Performance Optimization
```

</td>
<td width="33%" valign="top">

### **⚙️ Backend Technologies**

```yaml
Server Architecture:
  - Node.js Runtime Environment
  - Express.js Web Framework
  - RESTful API Design
  - Middleware Integration

Database & Authentication:
  - MongoDB with Mongoose ODM
  - JWT Token-based Authentication
  - bcrypt Password Hashing
  - Input Validation & Sanitization

External Integrations:
  - GitHub API for Repository Data
  - Gravatar API for Profile Images
  - Email Validation Services
  - Normalize-URL for Link Processing
```

</td>
<td width="33%" valign="top">

### **🚀 DevOps & Deployment**

```yaml
Development Workflow:
  - Git Version Control
  - Environment Configuration
  - Concurrent Development Server
  - API Testing with Postman

Production Deployment:
  - Heroku Cloud Platform
  - MongoDB Atlas Integration
  - Environment Variables Management
  - Production Build Optimization

Security Measures:
  - CORS Configuration
  - Rate Limiting Implementation
  - Data Validation & Sanitization
  - Secure Header Management
```

</td>
</tr>
</table>

---

## 💡 **Advanced Implementation Features**

<div align="center">

### 🔧 **Modern Development Practices**

</div>

<table width="100%">
<tr>
<td width="50%" valign="top">

### **🏆 Redux State Management Excellence**

```javascript
// Advanced Redux Implementation
const store = createStore(
  rootReducer,
  initialState,
  composeWithDevTools(applyMiddleware(...middleware))
);

// Redux Subscription for Local Storage Management
store.subscribe(() => {
  const { auth } = store.getState();
  if (auth.token) {
    setAuthToken(auth.token);
  } else {
    setAuthToken();
  }
});

// Pure Reducer Functions with Immutable State
const authReducer = (state = initialState, action) => {
  switch (action.type) {
    case LOGIN_SUCCESS:
      return {
        ...state,
        token: action.payload.token,
        isAuthenticated: true,
        loading: false,
        user: action.payload.user
      };
    default:
      return state;
  }
};
```

**Key Features:**
- 🔄 **Predictable State Updates** with pure reducers
- 💾 **Persistent Authentication** via localStorage
- 🎯 **Action Creators** with error handling
- 📊 **DevTools Integration** for debugging

</td>
<td width="50%" valign="top">

### **🔐 Advanced Authentication System**

```javascript
// JWT Token Management with Axios Interceptors
const api = axios.create({
  baseURL: '/api',
  headers: {
    'Content-Type': 'application/json'
  }
});

// Automatic Token Expiration Handling
api.interceptors.response.use(
  (res) => res,
  (err) => {
    if (err.response?.status === 401) {
      store.dispatch(logout());
    }
    return Promise.reject(err);
  }
);

// Secure Route Protection
const PrivateRoute = ({ children }) => {
  const { isAuthenticated, loading } = useSelector(state => state.auth);
  
  return !isAuthenticated && !loading ? 
    <Navigate to="/login" /> : children;
};
```

**Security Features:**
- 🛡️ **Automatic Token Refresh** handling
- 🚫 **Route Protection** for authenticated users
- 🔒 **Secure Password Hashing** with bcrypt
- ⏰ **Session Timeout Management**

</td>
</tr>
</table>

---

## 📊 **Performance Optimizations & Updates**

<div align="center">

### ⚡ **Latest Enhancements & Modernizations**

</div>

<table width="100%">
<tr>
<td width="50%" valign="top">

### **🔄 API & Integration Updates**

#### **GitHub API Authentication**
- ✅ **Migrated from deprecated URL query parameters** to token-based authentication
- 🔐 **Secure token management** with environment variables
- 📝 **Enhanced error handling** for API rate limits

#### **Package Modernization**
```bash
# Replaced deprecated packages
npm uninstall request moment react-moment
npm install axios uuid normalize-url
```

#### **UUID Implementation**
```javascript
// Updated to modern UUID v4 syntax
import { v4 as uuidv4 } from 'uuid';
const id = uuidv4();
```

</td>
<td width="50%" valign="top">

### **🎨 UI/UX Improvements**

#### **Date Formatting with Intl API**
```javascript
// Replaced Moment.js with native browser API
function formatDate(date) {
  return new Intl.DateTimeFormat().format(new Date(date));
}
```

#### **React Router v6 Migration**
- 🧭 **Updated to Routes/Route syntax** from Switch
- 🎯 **useNavigate and useParams hooks** replacing history/match
- 🛡️ **Simplified PrivateRoute** component implementation

#### **Enhanced Component Architecture**
- ♻️ **Component reusability** with ProfileForm consolidation
- 📱 **Responsive design** improvements
- 🎨 **Fixed positioning** for alert notifications

</td>
</tr>
</table>

---

## 🚀 **Getting Started**

<div align="center">

### **Quick Setup Guide**

</div>

### **📋 Prerequisites**

```bash
Node.js >= 14.x
npm >= 6.x
MongoDB Atlas Account (or local MongoDB)
GitHub Personal Access Token
```

### **⚙️ Installation**

1. **Clone the repository**
   ```bash
   git clone https://github.com/anuraagkoyalkar/devconnector-2.0.git
   cd devconnector-2.0
   ```

2. **Install server dependencies**
   ```bash
   npm install
   ```

3. **Install client dependencies**
   ```bash
   cd client
   npm install
   cd ..
   ```

4. **Configure environment variables**
   ```bash
   # Create config/default.json
   {
     "mongoURI": "your_mongodb_atlas_uri",
     "jwtSecret": "your_jwt_secret_key",
     "githubToken": "your_github_access_token"
   }
   ```

### **🏃‍♂️ Running the Application**

```bash
# Development mode (runs both client and server)
npm run dev

# Production build
cd client && npm run build

# Production server
NODE_ENV=production node server.js
```

---

## 📁 **Project Structure**

```
devconnector-2.0/
├── client/                 # React frontend application
│   ├── public/            # Static assets
│   ├── src/
│   │   ├── components/    # Reusable React components
│   │   ├── actions/       # Redux action creators
│   │   ├── reducers/      # Redux reducers
│   │   ├── utils/         # Utility functions
│   │   └── App.js         # Main App component
├── config/                # Configuration files
├── middleware/            # Express middleware
├── models/               # Mongoose data models
├── routes/               # Express API routes
├── server.js             # Express server entry point
└── package.json          # Server dependencies
```

---

## 🔧 **API Endpoints**

<div align="center">

### **RESTful API Documentation**

</div>

<table width="100%">
<tr>
<td width="50%" valign="top">

### **🔐 Authentication Routes**

```http
POST   /api/auth/login          # User login
POST   /api/auth/register       # User registration
GET    /api/auth/user          # Get current user
```

### **👤 User Profile Routes**

```http
GET    /api/profile/me         # Current user profile
POST   /api/profile           # Create/Update profile
DELETE /api/profile           # Delete profile
GET    /api/profile/users     # All user profiles
GET    /api/profile/user/:id  # Profile by user ID
```

</td>
<td width="50%" valign="top">

### **💼 Experience & Education**

```http
PUT    /api/profile/experience    # Add experience
DELETE /api/profile/experience/:id # Delete experience
PUT    /api/profile/education     # Add education
DELETE /api/profile/education/:id  # Delete education
```

### **💬 Posts & Comments**

```http
GET    /api/posts             # Get all posts
POST   /api/posts             # Create post
DELETE /api/posts/:id         # Delete post
PUT    /api/posts/like/:id    # Like/Unlike post
POST   /api/posts/comment/:id # Add comment
```

</td>
</tr>
</table>

---

## 🚀 **Deployment**

<div align="center">

### **Production Deployment Guide**

</div>

### **🌐 Heroku Deployment**

```bash
# Create production branch (local only)
git checkout -b production

# Add production config (DO NOT COMMIT TO MAIN)
git add -f config/production.json
git commit -m "Production build ready"

# Deploy to Heroku
heroku create your-app-name
git push heroku production:main

# Clean up local production branch
git checkout main
git branch -D production
```

### **📊 Production Checklist**

- ✅ MongoDB Atlas whitelist configuration
- ✅ Environment variables properly set
- ✅ JWT secret key configured
- ✅ GitHub token added to production config
- ✅ CORS settings for production domain
- ✅ Build optimization completed

---

## 🤝 **Contributing**

Contributions are welcome! This project demonstrates modern full-stack development practices and is continuously improved with the latest technologies.

### **Development Guidelines**

1. 🌿 **Branch Strategy**: Create feature branches from `main`
2. 📝 **Code Style**: Follow ESLint and Prettier configurations
3. 🧪 **Testing**: Ensure all features work in both development and production
4. 📖 **Documentation**: Update README for any new features

---

## 📄 **License**

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:667eea,100:764ba2&height=120&section=footer" />

### 🌟 **Built with ❤️ by [Anuraag Koyalkar](https://github.com/anuraagkoyalkar)**

**Software Engineer | Full Stack Developer | MERN Stack Specialist**

[![Portfolio](https://img.shields.io/badge/Portfolio-FF5722?style=for-the-badge&logo=firefox&logoColor=white)](https://anuraag-portfolio.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/anuraag-koyalkar)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:koyalkaranurag45@gmail.com)

> *"Connecting developers through innovative technology solutions"*

</div>
