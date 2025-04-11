# Basic Node.js HTTP Server

This is a simple Node.js script that creates an HTTP server responding with "Hello World" to all incoming requests.

## 📦 Requirements

- [Node.js](https://nodejs.org/) installed on your machine

## 🚀 Getting Started

1. Create a file named `server.js` and paste the following code:

    ```js
    const { createServer } = require('http');

    const hostname = '127.0.0.1';
    const port = 3000;

    const server = createServer((req, res) => {
      res.statusCode = 200;
      res.setHeader('Content-Type', 'text/plain');
      res.end('Hello World');
    });

    server.listen(port, hostname, () => {
      console.log(`Server running at http://${hostname}:${port}/`);
    });
    ```

2. Open a terminal and navigate to the directory containing `server.js`.

3. Run the server with:

    ```bash
    node server.js
    ```

4. Open your browser and go to [http://127.0.0.1:3000](http://127.0.0.1:3000)

5. You should see:

    ```
    Hello World
    ```

## 🧾 Code Explanation

- Uses Node's built-in `http` module to create a server
- Listens on `127.0.0.1:3000`
- Sends a plain text response `"Hello World"` to every request

## 📜 License

This project is licensed under the [MIT License](LICENSE).
