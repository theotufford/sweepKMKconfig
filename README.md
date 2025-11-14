# sweepKMKconfig
I had a lot of trouble putting thiss all together and had to modify quite a lot so I thought I would share in case anyone else is also fighting kmk demons
this firmware is specifically for use with the boardsource blok communicating over a trrs jack.

## a few tips
its always a firmware issue. I took apart and broke 3 pcbs and 1 mcu in the process just to find out every time that the firmware just literally was not working. The hardest part in my experience was getting the two halves to communicate properly and ensuring that they were in fact soundly connected. I wrote two little test scripts for this that you can upload to your mcu and in a serial terminal connected to the side A of the test you should be reading the console printing alternating "high", "low". This is a quick way to make sure that everything is soldered correctly and save yourself the insanity of taking everything a part and breaking it and then waiting a week for a replacement just to realize you just wasted a few late nights of work. 
good luck
