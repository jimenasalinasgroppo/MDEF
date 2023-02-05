---
hide:
    - toc
---

# Prototyping For Design

## Week 1 - Day 1

Today Victor told us about microchips and the specific parts behind it. The highlight for me was learning that there were layers of communication that could be closest to the hardware and therefore most technical and then there were others that are closest to the user and therefore more accessible to humans, such as the chat prompts of GPT-3.


###**Micro challenge 1** Learning to activate music with a buzzer using our electronic kit.

This was my first time operating Arduino by myself. In Tech beyond the myth I worked with experts on my team so I was in charge of the communications aspect. Wen lent me here Arduino Uno which was a great starting point because its especially designed to teach children in high school to approach Arduino.

I started looking at open source libraries with different music tracks, such as Harry Potter, Ed Sheeran songs and The Pink Panther theme song. Marielle helped me iterate certain numbers on the code to get the code tu run properly on my computer.

> This is the code I inputted into Arduino. Saving it for future documentation.
// Copyright (c) 2022 HiBit <https://www.hibit.dev>
// -------------------------------------------------#include "pitches.h" #define BUZZER_PIN 8
int REST = 0;
int melody[] = {
  REST, REST, REST, NOTE_DS4,
  NOTE_E4, REST, NOTE_FS4, NOTE_G4, REST, NOTE_DS4,
  NOTE_E4, NOTE_FS4,  NOTE_G4, NOTE_C5, NOTE_B4, NOTE_E4, NOTE_G4, NOTE_B4,   
  NOTE_AS4, NOTE_A4, NOTE_G4, NOTE_E4, NOTE_D4,
  NOTE_E4, REST, REST, NOTE_DS4,
    NOTE_E4, REST, NOTE_FS4, NOTE_G4, REST, NOTE_DS4,
  NOTE_E4, NOTE_FS4,  NOTE_G4, NOTE_C5, NOTE_B4, NOTE_G4, NOTE_B4, NOTE_E5,
  NOTE_DS5,   
  NOTE_D5, REST, REST, NOTE_DS4,
  NOTE_E4, REST, NOTE_FS4, NOTE_G4, REST, NOTE_DS4,
  NOTE_E4, NOTE_FS4,  NOTE_G4, NOTE_C5, NOTE_B4, NOTE_E4,…
[1:57 p. m., 2/2/2023] Jimena: 2, 16, 16, 16, 16,
  4, 4,
  4, 8, 8, 8, 8, 8, 8,
  16, 8, 16, 8, 16, 8, 16, 8,   
  16, 16, 16, 16, 16, 2
};
void setup()
{
  pinMode(BUZZER_PIN, OUTPUT);
}
void loop()
{
  int size = sizeof(durations) / sizeof(int);
  for (int note = 0; note < size; note++) {
    //to calculate the note duration, take one second divided by the note type.
    //e.g. quarter note = 1000 / 4, eighth note = 1000/8, etc.
    int duration = 1000 / durations[note];
    tone(BUZZER_PIN, melody[note], duration);
  //to distinguish the notes, set a minimum time between them.
    //the note's duration + 30% seems to work well:
    int pauseBetweenNotes = duration * 1.30;
    delay(pauseBetweenNotes);
      //stop the tone playing:
    noTone(BUZZER_PIN);
  }
}

## Week 1 - Day 2

Today Eduardo taught us more about modelling and 3D models. He started by introducing terminology such as pixels vs vectors and going to basics allowed all of us to start with a clear mind.

One of the technical highlights for me was learning the importance of reducing image file sizes when uploading them to a website and being mindful of the ecological impact of not doing this.

###**Micro challenge 2.1** Parametrizing a croissant

I asked Chat GPT3 to parametrize a croissant since I have zero experience with modeling and 3D software besides 3Ds max when I was doing an animation class on product advertising.

First I used Noun Project to look for 2D croissant vectors. I then looked for open Rhino libraries that would allow me to look for different croissant models. I downloaded one that looked the most simple and opened it up on Rhino.

###**Micro challenge 2.2** Create a 3D design based on algorithmic thinking of any object or concept you like.

This was very exciting for me because I have zero experience modelling but the tools are very accesible. I was interested in exploring how to do 3D models of illustrations and deep dive on that a bit more. I really like the work of Cabeza Patata, an illustration collective that does 3D renderings of illustrations.
