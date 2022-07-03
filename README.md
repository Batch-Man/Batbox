
# Batbox - by darkbatcher
## Description
BATBOX is an external command that allows using console graphically, but not only. It enables also user interactions such as mouse.
For example, BATBOX allows console cursor position to be changed, change locally console's colors, or even get user mouse inputs.

Author: darkbatcher

## Usage
​		BATBOX [/d Text] [/g X Y] [/c Color] [/m] [/k[\_]]  [/a Character] [/w Duration] [/f State] [/s File] [/o OffsetX OffsetY] [/h Mode] [/p Mode] 
​		BATBOX [/disp text] [/goto X posY] [/color col] [/mouse] [/key[\_]] 
​      :: Old deprecated function names

     Allows user to manage console.
    
        - /D : Prints text. See BatBox (/d) (-> ``_batbox/disp'') .
    
        - /G : Changes cursor position. See BatBox (/g) (-> ``_batbox/goto'') 
          .
    
        - /C : Changes console's color . See BatBox (/c) (-> 
          ``_batbox/color'') .
    
        - /M : Get a user click. See BatBox (/m) (-> ``_batbox/mouse'') .
    
        - /K[_] : Get a user keystroke. See BatBox (/k) (-> ``_batbox/key'') .
    
        - /A : Prints character associated with a code. See BatBox (/a) (-> 
          ``_batbox/ascii'') . Since version 2.4, BatBox (-> ``../batbox'') 
          also supports character encoded using multibyte characters set, 
          especially UTF-8.
    
        - /W : Make a delay. See BatBox (/w) (-> ``_batbox/wait'') .
    
        - /F : Change console's window mode. See BatBox (/f) (-> 
          ``_batbox/fullscr'') .
    
        - /S : Plays a .WAV file. This command is avaliable, since version 
          2.4. See BatBox (/s) (-> ``_batbox/sound'') . Before the command 
          used to play a song. See BatBox (/s) (OLD) (-> 
          ``_batbox/sound_old'') .
    
        - /O : Moves origin of console. This command is usefull to make 
          sprites via BATBOX. See BatBox (/o) (-> ``_batbox/offset'') .
    
        - /H : Hides or show the console's cursor. See BatBox (/h) (-> 
          ``_batbox/cursor'') .
    
        - /P : Changes the console's window mode. See BatBox (/p) (-> 
          ``_batbox/console'') .
    
     If you want create graphisms using BATBOX, you can generate a BatBox 
     command line from a text file containing an ASCII-ART using SpriteBox (-> 
     ``spritebox'') tool.

NOTES

     You can mix several options on only one BATBOX command line, as shown by 
     ....
    
     Thus, the following script:
    
         BATBOX /g 10 10
         BATBOX /d "Hello world"
         BATBOX /g 0 0
    
     Can be shortened like this:
    
         BATBOX /g 10 10 /d "Hello world" /g 0 0
    
     You can specify numbers in BATBOX's parameter using three different 
     bases, for any option that require numbers. Firstly, you can specify 
     DECIMAL numbers, just write it as usual. You can also specify 
     HEXADECIMAL numbers, to do so, just add the prefix 0X. Finally you can 
     specify OCTAL numbers, you just have to add the prefix 0. The OCTAL 
     numbers are not recommended because their use is very restricted.
     
## Screenshot
**Example of displaying a text at desired coordinates and changing consoles color**
![image](https://user-images.githubusercontent.com/82807654/166758482-1aa8060c-01ce-4f66-8cde-29642ca4d80f.png)
     
**Example of getting user input through mouse using left and right click**
<!-- wp:image {"align":"center","id":3356,"style":{"color":{}}} -->
<div class="wp-block-image"><figure class="aligncenter"><img src="https://batch-man.com/wp-content/uploads/2022/04/example5-1-edited-2.png" alt="" class="wp-image-3356"/></figure></div>
<!-- /wp:image -->

**Example of getting user input through keyboard and displaying ASCII value corrosponding to entered character**
![image](https://user-images.githubusercontent.com/82807654/166781445-f7b99b95-e57a-4349-ae0c-2fb81045e518.png)

**Example of creating a delay in commands**
<!-- wp:image {"id":3373,"sizeSlug":"full","linkDestination":"none"} -->
<figure class="wp-block-image size-full"><img src="https://batch-man.com/wp-content/uploads/2022/04/1.gif" alt="" class="wp-image-3373"/></figure>
<!-- /wp:image -->

COMPATIBILITY

     Fully compatible with CMD.EXE. However BATBOX isn't a native command for 
     WINDOWS, so that you must use the following code to generate it 
     dynamically.
    
         for %%b in ( 
         4D5343460000000073030000000000002C000000000000000301010001000000
         00000000470000000100010000060000000000000000FE4259B5200062617462
         6F782E657865003FD9412724030006434BB5545F485361143F5737F0CF726B3A
         102ABB528B1EC24813421026D3529AB59C184460D7ED6EF7CE79EFB8F74A562F
         0B1D543EF5143DC60483C27AF0C14248B18710A4979ECA40426A0329A1B21ECA
         AF73EE9D4E21B287FAB6DF77CFF99DF37DDFEF3B3B779D1752C001800D5CC018
         808F1C1C3ED879A41015FB9F56C064E942ED141758A8ED96649D4F6A6A4C1306
         F8B0A028AAC1F789BC36A8F0B2C2B79E0DF1036A44ACDB557670638F601B4080
         E3A0C3FBFDDC06B7044EAE9CE34EA2283041C3B505A48E9E450079B99B69C05B
         FC4B1457BC75DD6666DECD8F981BE02EF71797FDC7A32E9A100C7C1EB1E505D9
         2CDD5BC7252AC57F1E92ABCA0771EB21D968029C98E76125D25F9967D1ED838C
         8372D6F24E093AD9175832FFADCAD43C7F8C459F9442D39D1E8C3947C6913F15
         7BB79A7BCD18CBA6D10BB24687B9E33226E4E6904E5DE37A9DE90A3C9C7926F1
         98F48C73E401F2CC731FBD66BAB2335D6E8689B0336A13E6798C76B601772CB6
         F7E2565EEAD64C1589A931C93092B34B2ECE4E1C6BB466EBE82C1DDD4E8A3ED3
         5ED25137B163B861AE9ED8B7D452F182D42F945F4D111213920E14F28B908D57
         B3C61233710903560539A9DA3CD0E257901F6EA600D664019744879B295EE44C
         3F43EF9BFD303A3FD172A61FE13CDABC17FD9BEBB39F5CD7DFD3BDEEF155565D
         6E63B4D8CC0E9EEF910E15745C5D47755EAB32AB245726A20A890C55275B4616
         952417A44035BA71FC8498670A970F3F77CCCD7E2862E3F524D44EBFBB6D741F
         3D46F7A4DF3847E885988B835574AF0EDE4893F9056F1874970F26101F111711
         B6DD3EA8411C472C20A611FD31211C8D0CA89737DAEC4665A1E532F8CA8DA13F
         ED2E7013682FBA7FDFA29DA11E7F57775D6B2000A7DBBACEB4051AEA4D077EE0
         02076E54833881E846488864FEB09DE2D8AAA2113222ED82124988E48744C3AF
         2ABA9A103BF17F6A3BD32D0E192D86A1C97D8386B82DE21FD474550BAABA6CC8
         AA42ABBA4421920F7628C941A385F213A298DCB6AE55D69309E18A79D40C6A9A
         47BC422C2356106B799D7F8AE16D345931A264F5C644232C9916990382AC085A
         4C475F1C920D93EFEF932C4B3734434D00FC02                          
         ) Do >>t.dat (Echo.For b=1 To len^("%%b"^) Step 2
         ECHO WScript.StdOut.Write Chr^(Clng^("&H"^&Mid^("%%b",b,2^)^)^) : 
      Next)
         Cscript /b /e:vbs t.dat>batbox.ex_
         Del /f /q /a t.dat >nul 2>&1
         Expand -r batbox.ex_ >nul 2>&1
         Del /f /q /a batbox.ex_ >nul 2>&1
    
     As BATBOX is written in assembly language, it isn't obviously not easy to 
     port to another operating systems. Therefore, it is only avaliable for 
     MS-WINDOWS.

LICENSE

     BATBOX is a free software distributed under GNU GENERAL PUBLIC LICENSE 
     VERSION 3.

AUTHOR

     BATBOX has been written by DARKBATCHER. The project is no more develloped 
     actually.
     
**Article link-** https://batch-man.com/batbox/

**Video link-** https://www.youtube.com/watch?v=yL8zNujYyMQ

