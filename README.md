# Fluffy2-PCB-Modern-CAD

And here is. Fluffy2 modern cad. Both serial and usb via ftdi TTL adapter. CAD for both and SCH is included. should be able to use any number of usb2serial-TTL adapters, just adjust header and arrangement to match pinout of what chose.

works. default of ftdi in win is 9600 and bm 16. which programmer is 115200 and the 16 is stable as but super slow. sx28 seems fine at bm 1msec but sx48 top doesnt erase. 4 seems to be sweet spot for sx48 stable and fastest. play with icprog hw settings too for io delay i just have on direct io and default io delay of 10

when fluffy2 cad sx48 seems future adding than designed round. serial is too fast with sx48 missing top. play with bios settings if possible. havent looked yet (been ages since used serial, lpt yeah but serial nah) and mix with io delay tuning. but as above how i have it stable sx48. Or pin 13 of pic is speed jumper could use for slow rate, didn't put header check fluffy2 original schematics for info. sx28 is np.

enjoy

Bom for both (drop 4x caps, db9 and Max for ftdi and get ftdi TTL adapter)

I also left r11 off as just for mclr which not used with icsp. Its dropped on board if someone wants to just did icsp header too than dip sockets for sx18 sx28.

For ice sx28 use icprog ic set sx28_a this sets the memory as needs then open hex from ice pack. For it to verify sx28 disable cp fuse as won't be able to verify till sure got stable writing, I had np with bm 1 for sx28, sx48 4 new cad duo2 or 5 old cad, sx48 has cp disabled as rls fuse set.

Sources:
https://hellspark.com/dm/ebench/sx/mirrors/www.semis.demon.co.uk/Sx/SXmain.htm

http://www.ic-prog.com/download.html
icprog i am using latest 1.06c
