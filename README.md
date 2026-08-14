This is a alert system, which triggers a buzzer (Piezo Element), by interrupting the laser that points to the phototransistor.

Contained Main Elements:
- Piezo Element
- 555 timer
- Phototransistor
- Comparator
- Battery Cell
- Battery
- BJT

Side Elements:
- 3x10k Resistor
- 2x1uf Capacitor

How it works:

First of all the Battery is responsible for:
- powering the Comparator
- collector current for the Phototransistor in combination with a 10k resistor for a voltage divider for the reference voltage for the comparator
- collector current for the BJT
- a voltage divider for the variable voltage of the comparator
- putting the 555 timer in astable mode

The idea behind it:

Setting the variable voltage of the comparator to a constant value and setting the reference voltage of the comparator to a variable value!!!

Normaly you would use the phototransistor combined in a voltage divider for setting a variable voltage at the comparator.
And you would use the constant voltage divider to create a reference voltage for the comparator.

In this case, the comparator would give us a positive output if the laser shines on the phototransistor.

So my idea was to flip it around!!!

When the laser on the phototransistor now gets interrupted the output of the comparator is positive,
therefore it sends the interruption signal to the BJT which activates the 555 timer in astable mode to trigger a Piezo Element.

Problems:
The alarm works as long as the laser is interrupted, but when it got only short interrupted it instantly stops again.

Future:
Add a second 555 timer in monostable mode to set a period of time in where the alarm goes off.
