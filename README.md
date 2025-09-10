# Copy to Clipboard

A simple, lightweight web application that demonstrates how to implement copy-to-clipboard functionality using modern JavaScript APIs.

![Copy to Clipboard Demo](https://github.com/user-attachments/assets/fdea3d58-279d-4d41-b2fa-6bc6516a3632)

## Features

- ✨ **Simple Interface**: Clean, user-friendly design with a textarea and copy button
- 📋 **Modern Clipboard API**: Uses the latest `navigator.clipboard.writeText()` method
- 📱 **Mobile Friendly**: Responsive design that works on both desktop and mobile devices
- 🎨 **Styled UI**: Attractive styling with hover effects and rounded corners
- ⚡ **Fast & Lightweight**: Pure HTML, CSS, and JavaScript - no dependencies required
- 🔔 **User Feedback**: Alert notification confirms successful copy operation

## How to Use

1. **Type or paste text** into the textarea
2. **Click the "Copy to Clipboard" button**
3. **Receive confirmation** via an alert message
4. **Paste the text** anywhere you need it (Ctrl+V or Cmd+V)

## Demo

You can try the application by opening `index.html` in any modern web browser. The interface includes:

- A textarea with placeholder text "Type something here..."
- A green "Copy to Clipboard" button
- Automatic text selection and copying functionality
- Success/error feedback through browser alerts

## Technical Details

### Technologies Used
- **HTML5**: Semantic structure and accessibility
- **CSS3**: Modern styling with flexbox layout
- **Vanilla JavaScript**: Copy functionality using Clipboard API

### Browser Compatibility

This application uses the modern [Clipboard API](https://developer.mozilla.org/en-US/docs/Web/API/Clipboard_API) which is supported in:

- ✅ Chrome 66+
- ✅ Firefox 63+
- ✅ Safari 13.1+
- ✅ Edge 79+

**Note**: The Clipboard API requires a secure context (HTTPS) in production environments.

### Key Functions

```javascript
function copyToClipboard() {
    var textBox = document.getElementById("textBox");
    textBox.select();
    textBox.setSelectionRange(0, 99999); // For mobile devices
    navigator.clipboard.writeText(textBox.value).then(function() {
        alert("Copied the text: " + textBox.value);
    }, function(err) {
        alert('Could not copy text: ', err);
    });
}
```

## Setup & Installation

### Option 1: Direct Browser Usage
1. Download or clone this repository
2. Open `index.html` in your web browser
3. Start using the copy-to-clipboard functionality immediately

### Option 2: Local Development Server
```bash
# Clone the repository
git clone https://github.com/DipeshDronaHQ/copyToClipboard.git

# Navigate to the project directory
cd copyToClipboard

# Start a local server (Python 3)
python3 -m http.server 8000

# Or using Node.js
npx http-server

# Open http://localhost:8000 in your browser
```

## File Structure

```
copyToClipboard/
├── index.html          # Main application file
└── README.md          # Project documentation
```

## Use Cases

This project is perfect for:

- 📚 **Learning**: Understanding modern clipboard functionality
- 🔧 **Integration**: Copying code snippets for use in larger projects
- 🎯 **Reference**: Example of clean, accessible web development
- 🚀 **Prototyping**: Quick copy-paste functionality for web applications

## Browser Security Notes

- The Clipboard API requires user interaction (clicking a button)
- HTTPS is required for production deployments
- Some browsers may show permission prompts for clipboard access

## Contributing

Feel free to submit issues, fork the repository, and create pull requests for any improvements.

## License

This project is open source and available under the [MIT License](LICENSE).

---

**Made with ❤️ by [Dipesh](https://github.com/DipeshDronaHQ)**