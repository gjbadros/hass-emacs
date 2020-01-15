# hass-emacs
Tools for Home Assistant that work with GNU Emacs

Right now this is just auto completion support for entity names.

You either need to put the JSON contents of your Home Assistant's /api/states
API output in a file (probably called api_states.txt in your config directory)
or you need to populate a file hass-mode-secrets.el with your server name
and an authentication token (gotten from HomeAssistant's UI).

If you do the former, you need to pass the name of the file to hass-setup-completion
(possibly just by using a prefix-arg before calling the function interactively:

C-u M-x hass-setup-completion

Will prompt you for the filename that has the contents of /api/states from
your server.

It's easier to just use hass-mode-secrets.el unless you have another reason
to have api_states.txt lying around (I do, and I like this completion being
able to work without the live server running, which is why I support the file
version in addition to accessing via a live server).
