
# BatBox - by DarkBatcher
## Description
BatBox is an external command that allows using console graphically. Furthermore, it enables also user interactions such as mouse and keyboard input.
BatBox is an extremely small program (2 kilobytes) yet powerful and fast utility with with 11 switches.

Author: DarkBatcher

## Usage
`batbox [/d Text] [/g X Y] [/c Color] [/m] [/k[\_]]  [/a Character] [/w Duration] [/f State] [/s File] [/o OffsetX OffsetY] [/h Mode] [/p Mode]`

Allows user to manage console.
 
- /A : Prints character associated with a code.
- /C : Changes the color of the text that will be written (unlike cmd's `color` command, it doesn't change all the color)
- /D : Prints text.
- /F : Change console's window mode
- /G : Changes cursor position. S
- /H : Hides or show the console's cursor.
- /K[_] : Get a user keystroke. If `/k_` is used, it won't wait for input and returns 0 if no key is pressed.
- /M : Get a user click.
- /O : Moves the origin of console. The default origin is (0,0) at the top corner left. This command is useful to make 
- /P : Changes the console's window mode.
- /S : Plays a .WAV file.
- /W : Make a delay. The unit for this switch are milliseconds.
- /Y : Same as `/y`, but will detect any mouse action, including movement. It can be used for text hovering.
sprites via BatBox. 
 
If you want create graphisms using BatBox, you can generate a BatBox 
command line from a text file containing an ASCII art using SpriteBox (-> 
`spritebox`) tool.

# Notes

You can use multiple options on a single BatBox command line, so the following script:
 
```cmd
batbox /g 10 10
batbox /d "Hello world"
batbox /g 0 0
```
 
Can be shortened like this:
 
```cmd
batbox /g 10 10 /d "Hello world" /g 0 0
```
 
You can specify numbers in BatBox's parameter using decimal, hexadecimal and octal bases. For hexadecimal, add "0x" at the beginning of the number and for octal add a "0" also at the beginning.

## Screenshot
###### Example of displaying a text at desired coordinates and changing consoles color**
![image](https://user-images.githubusercontent.com/82807654/166758482-1aa8060c-01ce-4f66-8cde-29642ca4d80f.png)

###### Example of getting user input through mouse using left and right click**
<!-- wp:image {"align":"center","id":3356,"style":{"color":{}}} -->
<div class="wp-block-image"><figure class="aligncenter"><img src="https://batch-man.com/wp-content/uploads/2022/04/example5-1-edited-2.png" alt="" class="wp-image-3356"/></figure></div>
<!-- /wp:image -->

###### Example of getting user input through keyboard and displaying ASCII value corrosponding to entered character**
![image](https://user-images.githubusercontent.com/82807654/166781445-f7b99b95-e57a-4349-ae0c-2fb81045e518.png)

###### Example of creating a delay in commands**
<!-- wp:image {"id":3373,"sizeSlug":"full","linkDestination":"none"} -->
<figure class="wp-block-image size-full"><img src="https://batch-man.com/wp-content/uploads/2022/04/1.gif" alt="" class="wp-image-3373"/></figure>
<!-- /wp:image -->

# Compatibility

BatBox is fully compatible with `cmd.exe`. However, BatBox isn't a native command for Windows, so you have to use the following code to generate it dynamically:
```cmd
for %%B in (
TVNDRgAAAABzAwAAAAAAACwAAAAAAAAAAwEBAAEAAAAAAAAARwAAAAEAAQAABgAAAAAAAAAA
/kJZtSAAYmF0Ym94LmV4ZQA/2UEnJAMABkNLtVRfSFNhFD9XN/DPcms6ECq7UosewkgTQhAm
01KatZwYRGDX7W73znnvuPdKVi8LHVQ+9RQ9xgSDwnrwwUJIsYcQpJeeykBCagMpobIeyq9z
7p1OIbKH+rbfd8/5nfN93+87O3edF1LAAYANXMAYgI8cHD7YeaQQFfufVsBk6ULtFBdYqO2W
ZJ1PampMEwb4sKAoqsH3ibw2qPCywreeDfEDakSs21V2cGOPYBtAgOOgw/v93Aa3BE6unONO
oigwQcO1BaSOnkUAebmbacBb/EsUV7x13WZm3s2PmBvgLvcXl/3Hoy6aEAx8HrHlBdks3VvH
JSrFfx6Sq8oHcesh2WgCnJjnYSXSX5ln0e2DjINy1vJOCTrZF1gy/63K1Dx/jEWflELTnR6M
OUfGkT8Ve7eae80Yy6bRC7JGh7njMibk5pBOXeN6nekKPJx5JvGY9Ixz5AHyzHMfvWa6sjNd
boaJsDNqE+Z5jHa2AXcstvfiVl7q1kwViakxyTCSs0suzk4ca7Rm6+gsHd1Oij7TXtJRN7Fj
uGGunti31FLxgtQvlF9NERITkg4U8ouQjVezxhIzcQkDVgU5qdo80OJXkB9upgDWZAGXRIeb
KV7kTD9D75v9MDo/0XKmH+E82rwX/Zvrs59c19/Tve7xVVZdbmO02MwOnu+RDhV0XF1HdV6r
MqskVyaiCokMVSdbRhaVJBekQDW6cfyEmGcKlw8/d8zNfihi4/Uk1E6/u210Hz1G96TfOEfo
hZiLg1V0rw7eSJP5BW8YdJcPJhAfERcRtt0+qEEcRywgphH9MSEcjQyolzfa7EZloeUy+MqN
oT/tLnATaC+6f9+inaEef1d3XWsgAKfbus60BRrqTQd+4AIHblSDOIHoRkiIZP6wneLYqqIR
MiLtghJJiOSHRMOvKrqaEDvxf2o70y0OGS2Gocl9g4a4LeIf1HRVC6q6bMiqQqu6RCGSD3Yo
yUGjhfITopjctq5V1pMJ4Yp51Axqmke8QiwjVhBreZ1/iuFtNFkxomT1xkQjLJkWmQOCrAha
TEdfHJINk+/vkyxLNzRDTQD8Ag==
)do echo:%%B>>"%tmp%\x.dat"
certutil -f -decode "%tmp%\x.dat" "%tmp%\b.dat">nul
del "%tmp%\x.dat" /q>nul
expand "%tmp%\b.dat" "%cd%\batbox.exe" >nul
del "%tmp%\b.dat" /q>nul
```
As BatBox is written in assembly language, porting it to other operating systems is hard. Therefore, it is only avaliable for Windows. If you're looking for a cross-platform alternative, take a look at [DarkBox](https://github.com/TSnake41/darkbox), made by [TSnake41](https://github.com/TSnake41).

# License

BatBox is distributed under GNU GPL version 3.

# Article and video demonstration
**Article:** https://batch-man.com/batbox/  

**Video:** https://www.youtube.com/watch?v=yL8zNujYyMQ

