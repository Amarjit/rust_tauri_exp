A simple Rust application with Tauri added after using `cargo tauri init`. This allows you to implement Tauri into an existing project. This project shows you that a vanilla webstack (HTML, CSS, JavaScript) can be used to render a frontend with a backend language, like Rust. Compilation results in a single executable file. e.g. on Windows, this would be an `exe` file.
Tauri can be use with an existing webserver or internally. This project encompasses the whole site does NOT use a webserver (no exposed ports) to connect the frontend and backend together.

## Folders
* src - The static HTML website to compile into the Rust application
* src/main.js - Tauri will inject a JS object into `__TAURI__` that allows this connection to take place. Notice there are no AJAX calls. The `invoke` function is used to call a Rust function.
* src-tauri - The auto-generated folder using thet Tauri application. This contains everything required to render a static website inside a Rust app
* src-tauri/src - Contains the Rust applicaiton itself. Note that `main.rs` should not be modified, which is the entry point of the application. `lib.ts` should be used for code. This file also contains the `command` to allow JavaScript from your static website to talk to Rust.

## More Information
[Tauri] https://v2.tauri.app/
