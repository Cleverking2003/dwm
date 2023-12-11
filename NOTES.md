# DWM notes

## dwm.exe

### Init sequence

* App host
    * Create window
    * Init session port
        * Create `\Sessions\{SessionId}\BaseNamedObjects\Dwm-XXXX-ApiPort-YYYY`
        * Start port thread
        * Register session port
    * Connect to `\UxSmsApiPort`
    * Send the session port name
* Ghost manager
    * Set wndproc of `Ghost` class to our own func

### Main loop

* Process window messages `¯\_(ツ)_/¯`

### Port thread

* Wait for multiple objects on port (`DwmRedirectionManagerWaitForMultipleObjects`)
* If 0, receive the message and handle it

### Port messages

### Window messages

### Ghost windows

