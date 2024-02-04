# ASCII ART CONVERTER

### DESCRIPTION
This small personal project turns any picture of any format into ASCII art.
It is intended for all ages, or who has nostalgic about the retro style in 80's.

My converter takes this image:

![image](/ascii-art-converter/src/resources/shibeIcon.jpeg)

And converts it to:
```
                       +======                                        +======
                      -==: .+===                                    -===  :==-
                      ==     .====                                ===-      ==
                      ==        ====                            ====        ==
                      ==         +====     -=-==========-     =====         ==
                      ==          ================================          ==
                      ==           ==============================           ==
                      ==          .==============================.          ==
                      ==          ================================.         ==
                      ==.       =-==================================       .==
                      ===    -========================================-    ===
                      ========================================================
                      ========================================================
                      ========================================================
                     .========================================================
                     ==========================================================
                    -=============+##%@#%%==============-=%#%%#%%+=============-
                    ==============-%%%%%%##==============%%%%#%##============-==
                    +           ===+-%##%##+============+###%#%=====           =
                                 .================================.            .
                                   :============================:
                                     ==========================
                                      ========       .========
                                        -=.  :%#%####%   .=-
                                            #%%#######%%:
                                            %%%#########::.
                                   @%.       ##########::::::  #%:
                                    +%..      .%%%%##:::::::::#*::::
                                     .%@         :::::::::::@#-:::::::
                                     .*##%    @%#%%#%%:.::%#%*::::::::::
                                       +##%%============%###*:::::::::
                                         ###--=========+##%:::::::::
                                         .:##---======+%#--::::::.
                                             =##%%%%%#=:::::::
                                              .::::::::::.
```

### USAGE

## Compiling the code
Use java xyz to ...

## Running the binary
You put any image under resources, and call command to console to begin turning the image into ASCII art.

```
$JAVA -cp $PATH_TO_CLASS_FILE 'Main'
```

### Code details

The main works happens in `convertToAscii()` in `Main.java`. It works by .... (This is the interesting part of your program, you should describe how it works.)

Before running `convertToAscii()`, you may adjust the size of the image and the ratio of the special character.
for instance

NOTE: How are the two settings different?

To change .... do:
```
double aspectRatioCorrection = x; 
// replace x with your own value in double
```

To change .... do:
```
BufferedImage resizedImage = resizeImage(image, x, y);
// replace x and y with your own value
```

### LICENSE
This project has a MIT license.