##### How to install espruino on the P8 smart watch:

You will need an android smartphone, and an app called DaFlasher from the playstore, made by atc1441.

using the app, you will upload three files, 

first a custom app that will replace the bootloader of the p8, 

then a file that will upload yet another bottloader, this time compatible with the espruino image linked bellow, build by fanoush

and finally the espruino image itself. 

After the last file is uπloaded, daflasher is done, and one can connect to the p8 using the espruino webide from a chrome browser, to continue with uploading the files of this repo. 

The three files needed for the first step are the following, in this order:

1. https://github.com/atc1441/DaFlasherFiles/blob/master/DaFitBootloader23Hacked.bin
2. https://github.com/atc1441/DaFlasherFiles/blob/master/FitBootloaderDFU2.0.1.zip
3. https://github.com/fanoush/ds-d6/blob/master/espruino/DFU/P8/espruino_2v06.129_p8_SDK11_SD20.zip

the first two files are a one time process, the last file is the espruino firmware image, and one could update just that in the future.

More info on daflasher and how to use:

https://www.youtube.com/watch?v=gUVEz-pxhgg

More info on p8 and espruino:

https://github.com/fanoush/ds-d6/tree/master/espruino/DFU/P8


#
##### Use this firmware image:

~~https://github.com/fanoush/ds-d6/blob/master/espruino/DFU/P8/espruino_2v06.9_p8_SDK11_SD20.zip~~

~~https://github.com/fanoush/ds-d6/blob/master/espruino/DFU/P8/espruino_2v06.54_p8_SDK11_SD20.zip~~

~~https://github.com/fanoush/ds-d6/blob/master/espruino/DFU/P8/espruino_2v06.100_p8_SDK11_SD20.zip~~

~~https://github.com/fanoush/ds-d6/blob/master/espruino/DFU/P8/espruino_2v06.110_p8_SDK11_SD20.zip~~

https://github.com/fanoush/ds-d6/blob/master/espruino/DFU/P8/espruino_2v06.129_p8_SDK11_SD20.zip

Use latest espruino firmware image, as it provides more flash space.

#
##### Use of files in this repo:

After flashing espruino using daflasher app from atc1441, upload at least init, handler and main files to the p8 using the espruino web ide from your chrome pc/phone, by selecting web bluetooth. No need to physically connect the watch to anything during the install firmware/install system files process.   

https://www.espruino.com/ide/

Init file should be uploaded to flash(allways), all other files should be uploaded to strorage by name given here, using the webide. 

do not rename them to .js, just copy paste the content of each file to right side of the web ide and upload. 


init (which will be renamed to .bootrst by the webide when you select to upload to flash-always) and handler files are system files, they take care of p8 hardware and general functions and are required. 

All other files are optional:

atc is to provide support for the d6Notification android app by atc1441, the app can set the time and some more advanced things, for now support is basic,

main provides for a clock face,

settings provides for a settings face, it can be accessed by a swipe up from bottom.

alarm provides three settable alarms,

calc is a simple calculator, 

euc and euc.md provides a dashboard for an ninebot one electric unicycle, 

hid provides music controll over bluetooth, 

repellent is a way to check medicine/battery/state of a xiaomi insect repellent,

One can leave out any files that he don't need, but it is best to upload all to get the feeling of the interface, and then delete the ones that are not wanted. 

Select Pretokenise, Mangle and Minification(online-simple) in the webide settings to save on ram/flash space. 

Change the 'type' variable inside the handler file to match the touch controller and accelerometer on your p8. All types are emulated as an 816(TEH) (gestures happen before finger leaves the screen) by the handler. Change the set.name variable inside the handler file to match your desired name, this will be broadcasted by the bt module.

Type reset() and press enter in the webide left hand side, after last file is uploaded. 

#

#### wip (the inteface on this video is dated, it now looks a lot nicer, will upload a new one sometime in the future)

[![Watch the video](https://img.youtube.com/vi/4hs8I65Fz5g/maxresdefault.jpg)](https://youtu.be/4hs8I65Fz5g)

![](https://i.ibb.co/PMW1tRP/IMG-20200921-105336078.jpg)

![](https://i.ibb.co/yVMrSps/Annotation-2020-08-21-044342.png)

![](https://i.ibb.co/bdRTMmV/Annotation-2020-08-21-044441.png)

![](https://user-content.gitter-static.net/dc3962ecf16c55a92544be663a21291f98842aa2/68747470733a2f2f692e6962622e636f2f506a4d6e72794c2f494d472d32303230303831392d3139333133343530372d4844522e6a7067)




