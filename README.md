# sweepKMKconfig
I had a lot of trouble putting thiss all together and had to modify quite a lot so I thought I would share in case anyone else is also fighting kmk demons
this firmware is specifically for use with the boardsource blok communicating over a trrs jack.

## a few tips
its always a firmware issue. I took apart and broke 3 pcbs and 1 mcu in the process just to find out every time that the firmware just literally was not working. The hardest part in my experience was getting the two halves to communicate properly and ensuring that they were in fact soundly connected. I wrote two little test scripts for this that you can upload to your mcu and in a serial terminal connected to the side A of the test you should be reading the console printing alternating "high", "low". This is a quick way to make sure that everything is soldered correctly, though if it fails I would probably still check configuration stuff before desoldering things. 
good luck

## if you are just starting the firmware flashing process
Get a serial terminal of your choice, Putty for windows works well and screen on linux. Go to https://circuitpython.org/board/boardsource_blok/ and hold down your boot button and copy the uf2 to the board which should now be named something like CIRCUITPY. Then go to or clone https://github.com/KMKfw/kmk_firmware, copy the kmk folder to the board. delete the default code file and then copy the kb and main.py file to the board and repeat for the other half of the board. BEFORE YOU TEST BOTH TOGETHER, unplug them, connect the trrs cable, and then plug in the usb-c. Plugging in the trrs while the keyboard has power is risky for a reason I dont full understand but just dont do it to be safe I think lol. If one half works but not the other, the the part A and B tests as described.
