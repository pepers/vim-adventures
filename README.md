# vim-adventures
solutions to puzzles in Vim Adventures

---

### Readme
[Vim Adventures](http://vim-adventures.com/) is an excellent educational game by Doron Linder.  It focuses on teaching many popular commands and motions used in the [Vim](http://www.vim.org/) text editor.  Here are a few disclaimers: 
- My solutions may not be the only way, and may not even be the optimal way to solve the puzzles.
- I strongly suggest you attempt all levels on your own before turning to the following spoilers.

---

### Levels
#### Level 8
- last puzzle: 
   - start on first twin brother, `j # E # n n ^ k $ * j j`, end on second brother

#### Level 9
- puzzle to the right: 
   - start on 'N' `$ j j j` end on 'd', get key
   - to go back, start on 'd' `gg`
- use key to enter house and get ability to use all numbers
- puzzle below the house (with 11 key presses):
   - start on 'n', which is numbered with a red '1'
   - you should visit the blocks in numerical order
   - `4j` → `b` → `2k` → `3w` → `4$` → `Tu`, you are now at the space on the other side
   - the key has appeared at the beginning of this puzzle, lets go back to get it
   - starting at the space, `5G` → `to` → `4k` 
   - now we have the key and can go back again to the bottom side of this puzzle, using the original way we came
- puzzle down and to the right of the last puzzle (with 8 key presses):
   - start on the 'f', which is numbered with a red '1', and we will again go in numerical order
   - `fi` → `3*` → `Fu` → `2*`
   - we are now at the other side on the 's' of 'sum', follow the path down to the '.' on the morse code looking puzzle
- morse code puzzle (spells out 'VIM ADVENTURES' in morse code):
   - `3e` gets directly to the other side
   - go down to lolcat sounding puzzle
- lolcat puzzle (16 key presses)
   - starting on 'W', `3x  ~  j  5~  5j  d4j  fC  2rG`
   - the key appears at the beginning of the puzzle, `6k` to go back up to get it
   - go back up through the morse code puzzle, `3e  k  5f.`
   - starting on 's' of 'sum', go back through this puzzle, `2G`
   - go left to '.' of next puzzle
- puzzle left of pink haired girl in bush (4 key presses)
   - starting on '.', `16b` (probably not the best answer to this puzzle)
   - go up to puzzle with a whole lot of numbers (actually just one number, Pi, to a whole lot of decimal places)
- Pi number puzzle (7 key presses)
   - start on '8', `9G  2f8  4k`, end on broken '5' tile
   - key appears on last '8', get there with `11G  6l  4j  3l`, we now have 3 keys
   - and back to the start of the puzzle with `3h`
   - go down to previous puzzle on 'k'
- puzzle below Pi puzzle (4 key presses)
   - start on 'k' of 'keep', `3$` to get to '.' on right side
   - `l h` to exit and re-enter puzzle from right side
   - `b Fa` to end on the 'a' above the locked gate
   - go down, unlock gate, and go to next puzzle
- deleting puzzle
   - go to start of 'not so ' → `d2w`
   - go to start of 'e22' → `3x`
   - go to start of '(C) Writes serverd ''s' → `d3W x`
   - go to start of 'XOOOO XOOOOO O' → `d2fX`
   - go to start of 'word1 w2 word1 w2 ''1' → `d4W x`
   - go to start of `bye bye` → `d2fe`
   - grab the new key (have 3 keys again)
   - go down and use all keys to open three locked gates to end of level

#### Level 10
- paste puzzle
   - go down and grab the 'p' command
   - delete a word with the red box around it, starting with cursor on first letter of that word
      - 'you' → `dw`
      - 'delet' → `5x`
      - 'real' → `4x`
   - paste those deleted words from the buffer, to where the corresponding purple bubbles show
      - 'P' for pasting before cursor, 'p' for pasting after cursor
   - grab the key after you pasted the correct word for each purple bubble
   - move to the 't' and use `x` to save it to the register for the next puzzle
   - go down and open locked gate
   - go to the right
- t puzzle
   - paste that 't' using `p` in all the spots that it indicates
   - go left and down to the line delete puzzle below the house
- line delete puzzle below house (7 key presses)
   - start on 'd' of 'round', `j  dj  k  P  G  p`
   - grab the '"' register specification
   - go up to the house and save the 't' character into another register (such as "a) `"ax`
   - go down, right, and up to the 't and x puzzle' above the 't puzzle'
- t and x puzzle (7 key presses)
   - start and red boxed 'x'
   - `"x  gg  $  "ap` (the `"ap` pastes from the "a register, if that is where you saved 't' to)
   - a key has appeared, `3j  2Fl` to get it
   - go down, right, and down to the 'tweedle beetle puzzle'
- tweedle beetle puzzle (98 key presses)
   - start on 3rd 'e' of 'beetles' → `G  3j  b  "bdw  b  "adw  b  "Bde  j  "Adw  "Ade  k  "aP  G  "bP`
   - a small brown key appears, grab it
   - go back to the house at the beginning and use the small brown key on the chest
   - the chest gives you the 'y' yank operator
   - go back to the 'tweedle beetle puzzle' and head down to the 'one ring puzzle'
- one ring puzzle
   - go to start of 'One ring to ' → `3yw` to yank the text
   - paste where the two purple bubbles tell you to, using 'p' or 'P'
   - key appears, grab it (now you have 2)
   - go down to 'Hip, Hip, Hooray! puzzle'
- Hip, Hip, Hooray! puzzle
   - delete the two red boxed lines using `dd` on each
   - move to the 'Hip, Hip, Hooray!' line and yank it using `yy`
   - paste it where the purple bubbles are → `2P  3j  3p`
   - key appears, grab it (you now have 3)
   - go all the way back to the house at the beginning, and go down to the 'Delete me! puzzle'
- Delete me! puzzle (7 key presses)
   - start on 't' of 'Delete' → `G  dd  dd  dd`
   - go down to '99 bottles puzzle'
- 99 bottles puzzle (15 key presses)
   - check `:reg` to see which registers you will need to use for pasting the text from
   - start on 'h' of 'the' → `"0P  j  "0p  j  p  j  "2p`
   - go down to next, and last puzzle
- last puzzle
   - check `:reg` to see which text you have saved to registers
   - you need the following lines of text saved to registers:
      - 'Betty rules'
      - 'tweedle beetle'
      - 'on the wall'
      - 'One Ring'
   - go back to the previous puzzles and save each to a different register using yank
      - I saved each, in order, from registers a-d, starting on the first character of each phrase:
         - 'Betty rules' → `"ayw` for 'betty ' + `"Aye` for 'rule' + `"Ay$` for 's' (on the last 's' of 'darkness', because it was the last character on the line)
         - 'tweedle beetle' → `"b2ye` for 'tweedle beetle'
         - 'on the wall' → `"c3ye` for 'on the wall'
         - 'One Ring' → `"d2ye` for 'One Ring'
   - go back to this puzzle and past the phrases in the right spot, using the right registers
      - for me, starting on the first space → `"aP  6l  "bP  l  "cp  $  "dp`
   - a new island appears, follow the path left and up and unlock the 3 gates to the end of the level

#### Level 11
