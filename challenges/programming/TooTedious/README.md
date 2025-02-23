# TooTedious

## Question Text

We have managed to intercept the following images of stolen card numbers from a hacker.The flag seems to one of the card numbers.However it seems like they are encrypted. 

Things to note:There are no spaces in the flag & all letters of the flag must be entered in caps.

*Creator - kon8387*

### Hints (Optional)
1. The flag is within the range of 60 - 90 

## Distribution
- CardNumbers.png
    - SHA1: `BBECF0C604E77275D34F51475607CC0BF7C4E706`
    - An Image of all 120 encrypted cards

## Solution
Optical Character Recognition aka OCR is a widely used technology that translate text in images into machine readable text.

Instead of typing each letter out manually,use OCR(online/offline) software to translate the card numbers into machine readable text.

The flag is in the 67th row. `OKBN{KWUXC73Z_3G3}`

Offline method:solve.py uses pytesseract which needs to be installed before using.The script will tanslate any text on the image into machine readable text, decode the letters with a shift of -8 and search through the entire string for a substring starting with "GCTF{" and ending with "}".

Online method:Use the site https://www.onlineocr.net/ to translate the image to text and use https://cryptii.com/pipes/caesar-cipher (or any other caeser cipher decoder) to decode the flags with a shift of -8, the flag can be easily found using a simple search (ctrl + f).

### Flag
`GCTF{COMPU73R_3Y3}`

## Recommended Reads
* https://docparser.com/blog/what-is-ocr/
* https://pypi.org/project/pytesseract/
