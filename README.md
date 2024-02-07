# ASCII ART CONVERTER

## DESCRIPTION
This small personal project turns any picture of any format into ASCII art.
It is intended for all ages, or who has nostalgic about the retro style in 80's.

My converter takes this image:

![image](/src/resources/shibeIcon.jpeg)

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

<!-- ## Compiling the code
Use java xyz to ... -->

## Running the binary
You put any image under resources, and call command to console to begin turning the image into ASCII art.

```
$JAVA -cp $PATH_TO_CLASS_FILE 'Main'
```

## Code details

The main works happens in `convertToAscii()` in `Main.java`. 

It works by first dividing the image into pixel blocks, and iterate through every pixel blocks using 2D for loop. Each pixel block will then converted into gray based on the RGB sum calculation and then divided by 3.0 (double value). Next step is grayness index checking, using `Math.min` between [the **gray** value and the ASCII_CHARS divided by 255 which is the max range for color], and [the ASCII_CHARS.length()-1].
```
private static final String ASCII_CHARS = "@%#*+=-:. ";
```
this results a certain special character to be placed on each of the blocks, from darkest to lightest. Those characters are then appended together and printed out using `toString()` method

Before running `convertToAscii()`, you may adjust the size of the image and the ratio of the special character.
for instance


To change how the ASCII art printed out (if it appears elongated in some form) do:
```
double aspectRatioCorrection = x; 
// replace the x with your own value in double
// compared to an ASCII image without correction :

        ===                    ===
        == ==                  == ==
        =   ==                ==   =
        =    ==              ==    =
        =.   :==  :======:  ==:    =
        =    .================     =
        =.    .==============:     =
        =     -==============-     =
        =    .================     =
        =    +=================    =
        =   -===================   =
        ============================
        ============================
        ============================
        ============================
      :============================:
      =======%#%#========##%%-======
      =======##%#%======%%###=======
      -     ==+###======###+=-     -
              ================
              ==============.
              =============+
                ====  . ====
                =  %###  =
                  #%###%
                  %%####:
              %   %#####:: %:
              #    *%%*::::%::.
                %    -:::::#::::
                ##  %%%%::%#::::.
                #%======##:::::
                .#%-=====##::::
                  @%-===#%::::
                  :%%%#.:::
                    -:::::
```

To change how big an ASCII art (the smaller canvas is, the fewer special characters are needed to complete the image) do:
```
BufferedImage resizedImage = resizeImage(image, x, y);
// replace the x and y with your own value
// compared to the above ASCII result, this one is made on smaller size:

        =====                  =====
          =   .==              -=.   =
          =    .================.    =
          =      ==============      =
          =    ==================.   =
          ==.====================== ==
          ============================
          ============================
        =======##.#=======-##%#=======
        .     :==---=======--==:.
                =============-
                  ===.    .===
                    %%####:
                %    %###::::#.
                  #     :::::#::::
                  #%-=====#%:::::
                    #--=-%:::.
                      ::.
```

Thank you for reading and enjoy creating your own ASCII arts !

## LICENSE
This project has a MIT license.