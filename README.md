Esprerial 🔌⚡
-----------------
A Javascript Library to interact with a microcontroller using USB (WebSerial)   
Check the example here : [https://usini.github.io/esprerial](https://usini.github.io/esprerial)

# Add libraries
In your HTML file add the libraries (you can either download it here, or use JSDelivr CDN)
```html
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/usini/esprerial/dist/esprerial.min.js"></script>
```
# Create Esprerial object
```js
// Create Esprerial with baudrate 115200 / endline= "\r\n"
serial = new Esprerial();
// Custom baudrate / endline
serial = new Esprerial(baudrate=9600, endline="\n")
```

# Add a connection button
```html
<button onclick="serial.begin()">Connect</button>
```

# Read a message (microcontroller --> web browser)
```js
function serial_read(message){
  console.log(message);
}
serial.setRead(serial_read);
```
## Write a message on serial (web browser --> microcontroller)
```js
serial.write("Hello World");
```

## Other callbacks
You can also set a callback when the connection is established or if an error occurred
```js
serial.setStart(serial_start);
serial.setError(serial_error);
```



