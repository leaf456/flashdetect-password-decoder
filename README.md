# flashdetect-password-decoder
Decode the password stored in FreeMEG's flashdetect settings.ini file. Can be used to unlock the panel.

How this works:

FlashDetect stores the password in this form:
`119168175167176169167167176`

Every 3 numbers is a character, with an additional "character" at the start which is an offset number. For each character, ignoring the first one, take the three numbers (which represent a character) and take away the offset to get an ASCII character code. For example:

119 168 175 167 176 169 167 167 176  
(take 119 from every character)  
    049 056 (etc)  
Then, get the ascii character codes from them.  
    1   8 (etc)  

And there you go, you've decoded the password!

This repo also contains the flashDetectBeta folder that I've obtained from FreeMEG's website, for historial purposes.
