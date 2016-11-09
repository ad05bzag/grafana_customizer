# grafana_read_only
Hints on how to disable grafana buttons to get kiosk read-only mode.

For this we relly on the great work done by Rafael Weinstein on it's MuttationSummary library.
https://github.com/rafaelw/mutation-summary

In case you have active users add a mask in front of the iframe or load the iframe out of the view, so the user will not see a flicker of the buttons before they are hidden (happens sometimes as it's a race condition to get the Observer registred before Grafana/Angular renders), and remove the mask/move when done registering the observer.

This method was tested against grafana version 4.0.0-1476697633pre1

