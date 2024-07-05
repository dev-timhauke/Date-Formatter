# Date Formatter

Welcome to the **Date Formatter** repository! This project is a simple web application written in HTML, CSS, and JavaScript. The application allows users to format dates into various formats.

## Features

- **Date Input**: Enter a date to format.
- **Multiple Formats**: Convert dates into different formats (e.g., MM/DD/YYYY, DD-MM-YYYY, etc.).
- **Interactive Interface**: Simple and intuitive user interface for easy date formatting.
- **Responsive Design**: Optimized for both desktop and mobile devices.

## Technologies

- **Frontend**: HTML5, CSS3, JavaScript (Vanilla JS)

## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/date-formatter.git
   cd date-formatter
   ```

2. **Open the index.html file**:
   - You can open the `index.html` file directly in your web browser to use the Date Formatter.

## Usage

1. Open the Date Formatter in your web browser.
2. Enter a date in the input field.
3. Choose the desired date format.
4. The formatted date will be displayed.

## Project Structure

- `index.html`: The main HTML file for the Date Formatter.
- `style.css`: CSS file for styling the application interface.
- `script.js`: JavaScript file for handling date formatting logic.

## Example

Here’s a simple example of the JavaScript code used to format dates:

```javascript
// Example of date formatting
document.getElementById('formatButton').addEventListener('click', function() {
  const dateInput = document.getElementById('dateInput').value;
  const format = document.getElementById('formatSelect').value;

  const formattedDate = formatDate(dateInput, format);
  document.getElementById('formattedDate').textContent = `Formatted Date: ${formattedDate}`;
});

function formatDate(date, format) {
  const options = {
    year: 'numeric',
    month: '2-digit',
    day: '2-digit'
  };

  switch (format) {
    case 'MM/DD/YYYY':
      return new Date(date).toLocaleDateString('en-US', options);
    case 'DD-MM-YYYY':
      return new Date(date).toLocaleDateString('en-GB', options).split('/').reverse().join('-');
    default:
      return date;
  }
}
```

## Contributing

Contributions are welcome! If you have any suggestions or improvements, feel free to submit a pull request. Please ensure your changes align with the project goals and maintain code quality.

## License

This project is licensed under the MIT License – see the [LICENSE.md](LICENSE.md) file for details.
