# simplest-browser-p2p-example

When I first started working with peer to peer web RTC (even using the simple peer library) this is what I needed.

To run, navigate to the project folder and execute:
```
python -m SimpleHTTPServer
```

Then, load http://localhost:8000/index.html#init.  In the "your id" text area it should give some "sdp" (session description protocol) information.  Open a second tab, and load http://localhost:8000/index.html.  Copy and paste the sdp information from the first tab into the "Other id" section of the second tab.  Then take the new sdp information from the second tab and put it in the "Other id" section of the first tab.  Click connect.

Now try typing text into the message box, and click send.  Check the other tab - the message arrived and the peers are connected.

An example with audio and video can be found in the with-audiovideo branch.  Be warned - running two tabs will cause an audio feedback loop if you're running them from the same computer!

Hope this helps!