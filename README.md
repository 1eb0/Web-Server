# Web Server - Test Environment

A simple Node.js and Express web server designed for testing scripts and applications that require a server environment to run properly. This server provides a basic HTTP server with static file serving capabilities for development and testing purposes.

## 🚀 Features

- **Static File Serving**: Serves HTML, CSS, JavaScript, and image files
- **Express Server**: Lightweight and fast HTTP server
- **Test Environment**: Perfect for running scripts that need a server context
- **404 Handling**: Custom error page for better debugging
- **CORS Support**: Ready for cross-origin requests during testing

## 🛠️ Tech Stack

- **Backend**: Node.js with Express.js
- **Server**: Express static file server
- **Port**: 5000 (configurable)
- **Dependencies**: Express.js only

## 📁 Project Structure

```
web-server/
├── images/           # Test images and static assets
├── index.html        # Sample HTML page for testing
├── style.css         # Sample CSS for testing
├── server.js         # Express server configuration
├── package.json      # Dependencies and scripts
├── txt.txt           # Sample text file for testing
└── README.md         # Project documentation
```

## 🚀 Getting Started

### Prerequisites

- Node.js (v14 or higher)
- npm (Node Package Manager)

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd web-server
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Start the server**
   ```bash
   npm start
   ```

4. **Open your browser**
   Navigate to `http://localhost:5000`

## 📝 Available Scripts

- `npm start` - Starts the Express server on port 5000
- `npm test` - Placeholder for future tests

## 🧪 Testing Use Cases

This server is perfect for testing:

- **Web Scraping Scripts**: Test scraping tools that need a real HTTP server
- **API Testing**: Test HTTP requests and responses
- **File Upload/Download**: Test file handling scripts
- **CORS Testing**: Test cross-origin requests
- **Static Asset Loading**: Test how scripts load CSS, images, and other assets
- **HTTP Status Codes**: Test different response codes and error handling

## 📝 Sample Files

The server includes sample files for testing:
- `index.html` - Sample HTML page with various elements
- `style.css` - Sample CSS file for styling tests
- `images/` - 8 sample images for testing image loading
- `txt.txt` - Sample text file for testing file serving

## 🔧 Configuration

### Changing the Port
Edit `server.js` and modify the `PORT` variable:
```javascript
const PORT = 3000; // Change to your preferred port
```

### Adding CORS Support
If you need CORS for testing, add this to `server.js`:
```javascript
app.use((req, res, next) => {
  res.header('Access-Control-Allow-Origin', '*');
  res.header('Access-Control-Allow-Headers', 'Origin, X-Requested-With, Content-Type, Accept');
  next();
});
```

### Adding Test Endpoints
Add custom routes for specific testing needs:
```javascript
app.get('/api/test', (req, res) => {
  res.json({ message: 'Test endpoint working!' });
});
```

## 🚀 Quick Start for Testing

1. **Start the server**:
   ```bash
   npm start
   ```

2. **Test with curl**:
   ```bash
   curl http://localhost:5000
   curl http://localhost:5000/images/image1.jpg
   ```

3. **Test with your scripts**:
   ```bash
   # Your script can now make requests to http://localhost:5000
   python your_test_script.py
   node your_test_script.js
   ```

## 📄 License

This project is licensed under the ISC License.

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/test-enhancement`)
3. Commit your changes (`git commit -m 'Add test feature'`)
4. Push to the branch (`git push origin feature/test-enhancement`)
5. Open a Pull Request

## 📞 Support

For support or questions about using this test server, please open an issue in the repository.

---

**Web Server** - Simple Test Environment 🧪
