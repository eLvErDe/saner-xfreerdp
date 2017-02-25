# saner-xfreerdp
Wrapper around xfreerdp to enhance default behavior (because nobody wants to configure a RDP client, it should just work)

It will extract current active display size and will compute 90% of this size for the remote one.
It will also detect your X keyboard layout and pass the appropriate one to the remonte endpoint.

`saner-xfreerdp [-h] [-d <domain>] [-u <username>] [-p <password>] [-f] -a <address>`

-h for help, -f for fullscreen mode

The following options default may by set in "${HOME}/.saner-xfreerdp":
*  DOMAIN="domain"
*  USERNAME="username"
*  PASSWORD="password" (probably not a good idea to store password here)
*  KEYMAP="keymap name" (check available with xfreerdp /kbd-list, otherwise will be detected by the script)
*  DO_RESIZE=0 (do not automatically resize screen to 90% of current active display)
*  RESIZE_PERCENT=70 (resize screen to nn% instead of 90% of current active display)
*  ADD_OPTS=+clipboard +home-drive (additional xfreerdp arguments, defaults enable clipboard and home disk sharing)

You need to logout from the remote session to get keymap updated

