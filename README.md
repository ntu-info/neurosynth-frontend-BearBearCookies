# Neuroscience Research Explorer - AJAX Frontend

## 🧠 Live Demo
[View Live Frontend](https://github.com/ntu-info/neurosynth-frontend-BearBearCookies)

## 📋 Project Description
A modern, responsive AJAX-based frontend for exploring neuroscience research terms and studies. Built with Tailwind CSS and vanilla JavaScript for real-time search without page refresh.

## 🚀 Features
- **Real-time AJAX Search**: Results update automatically as you type (no submit button needed)
- **Dual Endpoint Support**: Simultaneously queries both `/terms` and `/studies` endpoints
- **Smart Debouncing**: 500ms delay prevents server overload
- **Responsive Design**: Beautiful UI with Tailwind CSS
- **Interactive Terms**: Click any term to search for it
- **Logical Query Support**: Handles AND, OR, NOT operators for complex searches

## 🔧 Technical Implementation

### AJAX Implementation for Required Endpoints

#### 1. Terms Endpoint (`/terms/<term>`)
- **Location**: Lines 165-190 in index.html
- **Function**: `fetchTerms(term)`
- Triggered automatically on user input with debouncing
- Cancels previous requests using AbortController
- Displays results as clickable badges

#### 2. Studies Endpoint (`/query/<query_string>/studies`)
- **Location**: Lines 192-218 in index.html
- **Function**: `fetchStudies(query)`
- Handles URL encoding for logical operators
- Displays results as formatted study cards
- Shows metadata (authors, year, DOI)

### Key Requirements Satisfied
✅ **AJAX for both endpoints** - No submit button needed, updates on keyup  
✅ **Pretty UI** - Tailwind CSS with gradients, animations, and modern design  
✅ **Public availability** - Hosted on GitHub Pages  
✅ **Handles CORS** - Works with backend at https://mil.psy.ntu.edu.tw:5000  

## 📁 Project Structure
```
├── LICENSE
├── README.md
└── index.html   
```

## 🌐 API Endpoints Used
- Base URL: `https://mil.psy.ntu.edu.tw:5000`
- `/terms` - Get all available terms
- `/terms/<term>` - Get terms associated with a specific term
- `/query/<query_string>/studies` - Logical search for studies

## 💻 Local Development
1. Clone the repository
2. Open `index.html` in a web browser
3. Start typing in the search box to see real-time results

## 🎨 Technologies Used
- **Tailwind CSS** (via CDN) - Styling framework
- **Font Awesome** (via CDN) - Icons
- **Vanilla JavaScript** - No framework dependencies
- **Fetch API** - For AJAX requests
- **AbortController** - Request cancellation

## 📝 Example Queries
- Single term: `amygdala`
- Logical AND: `hippocampus and memory`
- Logical NOT: `amygdala not emotion`
- Complex: `prefrontal or frontal and executive`

## 👤 Author
BearBearCookies

## 📄 License
See LICENSE file