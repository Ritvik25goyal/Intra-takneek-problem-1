This is basically Steganography question of Capture the flag .
we got a image and audio .they dont reveal anything by simple preview anything .
first i used basic forensics skills on kali linux.
use strings , exiftools .
got this which does not help anything.
Software                        : gnome-screenshot
Creation Time                   : Friday 17 March 2023 06:32:17 PM

then i tried to change bit colors by stegosolve and there i find code looking like braillie,
 i tried to decode it but it also didn't work it doesnot making any sense .

tried to extract hidden file if any but that also didnt work .

then i tried google search the image and then i found cipher looking similar to image which hexahue cipher.

by google hexahue decoder it says:
KSHATRIYATAKNEEK

now i started audio steganography ,
first i tried sonic-visualiser to see spectrogram but it doesnt reveal anything . 
by closely listening i was thinking it was morse code . but it also didnt seem to reveal anything .

then i tried hiddenwave github repo to get  any secret message and finally it reveals :

Your Secret Message is: 7ECDB1519CC075C6631CAE5DAD922C5C

it was not base64 , i used hash-identifier and it says md5 .

i tried to decode it with hashcat and rockyou.txt and seclists but that hash didnt solved  .

