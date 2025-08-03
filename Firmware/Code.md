keyboard.debug_enabled //shows debug stuff

from kmk.kmk_keyboard import KMKKeyboard
from kmk.scanners.keypad import KeysScanner
from kmk.keys import KC
from kmk.modules.macros import Press, Release, Tap, Macros

keyboard.tap_time = 75 

keyboard = CAD_PAD()


macros = Macros()
keyboard.modules.append(macros)


PINS = [board.1, board.2, board.3, board.4, board.5, board.6, board.7, board.8, board.9, board.10]

coord_mapping = [
1, 2, 3,
4, 5, 6, 7,
8,       9,
         10,    
]
keyboard.matrix = KeysScanner(
    pins=PINS,
    value_when_pressed=False,
)

]


if __name__ == 'CAD_Pad':
    keyboard.go()
