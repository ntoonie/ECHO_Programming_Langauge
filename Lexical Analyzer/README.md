# E.C.H.O Lexical Analyzer

A web-based lexical analyzer (tokenizer) for the E.C.H.O (Executable Code, Human Output) programming language. This React application provides an interactive interface to analyze E.C.H.O source code and visualize the resulting tokens with color-coded categorization.

## Features

- **Interactive Code Editor**: Enter or paste E.C.H.O source code directly in the browser
- **Real-time Token Analysis**: Analyze code and view all tokens with their types and line numbers
- **Color-coded Token Types**: Visual categorization of keywords, identifiers, literals, operators, and more
- **Sample Code Loader**: Quick access to example E.C.H.O code for testing
- **Responsive Design**: Works seamlessly on desktop, tablet, and mobile devices
- **Token Type Legend**: Reference guide for all supported token types

## Supported Token Types

### Keywords
- **Program Keywords**: `function`, `start`, `end`, `echo`, `input`, `return`
- **Data Types**: `number`, `decimal`, `string`, `boolean`, `list`
- **Loop Keywords**: `for`, `while`, `do`
- **Conditional Keywords**: `if`, `else`, `switch`, `case`, `default`
- **Reserved Words**: `null`, `true`, `false`, `continue`, `break`, `new`, `this`
- **Noise Words**: `with`, `to`, `by`

### Literals
- **Number Literals**: Integer numbers (e.g., `10`, `42`)
- **Decimal Literals**: Floating-point numbers (e.g., `3.14`, `20.5`)
- **String Literals**: Text enclosed in double quotes (e.g., `"Hello World"`)
- **Boolean Literals**: `true`, `false`

### Operators
- **Arithmetic**: `+`, `-`, `*`, `/`, `%`, `^`, `//`
- **Assignment**: `=`, `+=`, `-=`, `*=`, `/=`, `%=`
- **Relational**: `<`, `>`, `<=`, `>=`, `==`, `!=`
- **Logical**: `&&`, `||`, `!`
- **Unary**: `++`, `--`

### Special
- **String Insertion**: `@` symbol for string interpolation
- **Comments**: Single-line (`//`) and multi-line (`/* */`)
- **Delimiters**: `{`, `}`, `(`, `)`, `[`, `]`, `,`

## Prerequisites

Before you begin, ensure you have the following installed on your system:

- **Node.js** (version 16 or higher recommended)
- **npm** (comes with Node.js) or **yarn** or **pnpm**

You can verify your installation by running:
```bash
node --version
npm --version
```

## Installation

1. **Clone or download this repository**
   ```bash
   cd echo-analyzer
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```
   
   This will install all required packages including React, Vite, Tailwind CSS, and other dependencies.

## Running the Application

### Development Mode

To start the development server with hot module replacement:

```bash
npm run dev
```

The application will be available at `http://localhost:5173` (or another port if 5173 is occupied). The page will automatically reload when you make changes to the source code.

### Production Build

To create an optimized production build:

```bash
npm run build
```

This creates a `dist` folder with optimized files ready for deployment.

### Preview Production Build

To preview the production build locally:

```bash
npm run preview
```

This serves the production build locally so you can test it before deploying.

## Usage

1. **Start the application** using `npm run dev`
2. **Enter E.C.H.O code** in the source code input area, or click "Load Sample" to load example code
3. **Click "Analyze Code"** to tokenize the source code
4. **View the results** in the token analysis table, which shows:
   - Line number where each token appears
   - Token type (color-coded)
   - Lexeme (the actual text of the token)
5. **Use the legend** at the bottom to understand the color coding for different token types

### Example E.C.H.O Code

```echo
start
number x = 10
decimal y = 20.5
string name = "Alice"
boolean flag = true

if x > 5
    echo "x is greater than 5"
end if

for i = 1 to 10
    echo "Count: @i"
end for

function number add(number a, number b)
    return a + b
end function

echo "Result: @x"
end
```

## Project Structure

```
echo-analyzer/
├── public/              # Static assets
│   └── vite.svg        # Favicon
├── src/
│   ├── App.jsx         # Main application component
│   ├── EchoLexicalAnalyzer.jsx  # Core lexical analyzer component
│   ├── index.css       # Global styles with Tailwind CSS
│   └── main.jsx        # Application entry point
├── index.html          # HTML template
├── package.json        # Project dependencies and scripts
├── vite.config.js      # Vite configuration
├── tailwind.config.cjs # Tailwind CSS configuration
├── postcss.config.cjs  # PostCSS configuration
└── eslint.config.js   # ESLint configuration
```

## Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build
- `npm run lint` - Run ESLint to check code quality

## Technologies Used

- **React 19** - UI library
- **Vite 7** - Build tool and dev server
- **Tailwind CSS 4** - Utility-first CSS framework
- **Lucide React** - Icon library
- **ESLint** - Code linting

## Browser Support

This application works in all modern browsers that support ES6+:
- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## Troubleshooting

### Port Already in Use
If port 5173 is already in use, Vite will automatically try the next available port. Check the terminal output for the actual URL.

### Dependencies Installation Issues
If you encounter issues installing dependencies:
1. Delete `node_modules` folder and `package-lock.json`
2. Run `npm install` again
3. If problems persist, try `npm cache clean --force` before reinstalling

### Build Errors
If the build fails:
1. Ensure all dependencies are installed: `npm install`
2. Check for syntax errors: `npm run lint`
3. Clear the build cache: Delete the `dist` folder and rebuild

## Contributing

This is a lexical analyzer tool for educational and development purposes. Feel free to extend it with additional features or improvements.

## License

This project is provided as-is for educational and development use.

---

**Note**: This lexical analyzer is designed specifically for the E.C.H.O programming language syntax. It performs tokenization only and does not include parsing or semantic analysis.
