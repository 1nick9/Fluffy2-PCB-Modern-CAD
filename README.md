# Fluffy2-PCB-Modern-CAD

And here is. Fluffy2 modern cad. Both serial and usb via ftdi TTL adapter. CAD for both and SCH is included. should be able to use any number of usb2serial-TTL adapters, just adjust header and arrangement to match pinout of what chose.

works. default of ftdi in win is 9600 and bm 16. which programmer is 115200 and the 16 is stable as but super slow. sx28 seems fine at bm 1msec but sx48 top doesnt erase. 4 seems to be sweet spot for sx48 stable and fastest. play with icprog hw settings too for io delay i just have on direct io and default io delay of 10

enjoy

Bom for both (drop 4x caps, db9 and Max for ftdi and get ftdi TTL adapter)

I also left r11 off as just for mclr which not used with icsp. Its dropped on board if someone wants to just did icsp header too than dip sockets for sx18 sx28.

Update so had some bits to get from wholesaler so got couple PIC16F84A-04/P in. and perfect with these both com/ftdi at full speed 115200 and usb/ftdi bm1. had originally just got 16F84-10/P off aliexpress as figure was eol mcu and cheaper as had nothing to get from wholesaler at time to make up for free post, which makes it real dear exercise. but yeah highly recommend getting 16F84A-04/P from legit wholesaler as much more stable and no issues with speed etc. could be difference between the a to non a also the 04 vs 10 or just straight up fake pic from china that worked but not up to speed. either way worth not cheaping out on the pic, though usb will work just slower speed.

For ice sx28 use icprog ic set sx28_a this sets the memory as needs then open hex from ice pack. For it to verify sx28 disable cp fuse as won't be able to verify till sure got stable writing, I had np with bm 1 for sx28, sx48 4 new cad duo2 or 5 old cad, sx48 has cp disabled as rls fuse set.

Sources:
https://hellspark.com/dm/ebench/sx/mirrors/www.semis.demon.co.uk/Sx/SXmain.htm

update.. randomly got bored n decided to run icprog 1.05 off the fluffy2 site than latest from icprog. and what do know is pretty stable with the sx48. odd time doesnt erase right on bm 1 but just erase again n try writing. drops the writting panel for verify if not full erased. there go, best to use the icprog from the fluffy2 mirror than the latest icprog. serial of fluffy2 should be same too. no need for slow writting. likely could get more stable erasing messing with io delay in icprog.
