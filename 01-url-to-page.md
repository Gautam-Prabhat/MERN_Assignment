# Assignment 1 – What happens between typing a URL and seeing the page?

When I enter a URL into the browser and press Enter, the following steps take place before the page is displayed on the screen:

1. **DNS Resolution:** The browser first checks its local cache for the domain's IP address. If not found, it queries a DNS server to translate the domain name (e.g., `example.com`) into a numerical IP address.
2. **TCP Connection & TLS Handshake:** Using the IP address, the browser establishes a TCP connection with the target server. For secure `HTTPS` websites, it also performs a TLS handshake to encrypt the communication.
3. **HTTP Request:** Once connected, the browser sends an HTTP request (such as `GET /index.html`) asking the server for the webpage's content.
4. **Server Response:** The web server processes the request and sends back an HTTP response containing a status code (like `200 OK`) along with the requested HTML document.
5. **Parsing & Building Trees (DOM & CSSOM):** The browser parses the HTML to construct the DOM (Document Object Model) tree. As it encounters linked assets (CSS, JavaScript, images, fonts), it requests them from the server and builds the CSSOM (CSS Object Model) from the stylesheets.
6. **Rendering, Layout & Painting:** Finally, the browser combines the DOM and CSSOM into a Render Tree, calculates the exact layout (size and position of elements), paints the pixels onto the screen, and executes JavaScript to make the page interactive.