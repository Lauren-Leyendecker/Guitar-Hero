# Guitar-Hero-NEW
Note: This was a programming assignment completed for my introduction to programming course. I created the RingBuffer, GuitarString, and GuitarHero classes, but the Keyboard and StdAudio classes that are needed to display the piano keyboard and play the sounds of the keys pressed in the GuitarHero class were not created by me and were provided for me as part of the assignment.

This program simulates the plucking a guitar string using the Karplus-Strong algorithm. When a guitar string is plucked, The excitation of the string can contain energy at any frequency. After the string is plucked, the string vibrates. The pluck causes a displacement which spreads wave-like over time. The Karplus-Strong algorithm simulates this vibration by maintaining a ring buffer of N samples (N equals the sampling rate (44,100) divided by the fundamental frequency (rounding the quotient up to the nearest integer)): the algorithm repeatedly deletes the first sample from the buffer and adds to the end of the buffer the average of the first two samples, scaled by an energy decay factor of 0.994.

The ring buffer models the medium (a string tied down at both ends) in which the energy travels back and forth. The length of the ring buffer determines the fundamental frequency of the resulting sound. Sonically, the feedback mechanism reinforces only the fundamental frequency and its harmonics (frequencies at integer multiples of the fundamental). The energy decay factor (0.994 in this case) models the slight dissipation in energy as the wave makes a roundtrip through the string.

RingBuffer: A RingBuffer object is an array of doubles that allows access to the item that has been in the data structure the longest amount of time.

GuitarString: A GuitarString object is used to model a vibrating guitar string.

GuitarHero: The GuitarHero class allows a user to press keys on their computer keyboard and interact with a piano keyboard and play guitar hero in real time.
