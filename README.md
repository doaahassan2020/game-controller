
  
#include <Keyboard.h>

#define upArrow 3
#define rightArrow 12
#define leftArrow 13
#define control 7
#define space 10
#define downArrow 5

void setup() {
  pinMode(upArrow, INPUT_PULLUP);
  pinMode(rightArrow, INPUT_PULLUP);
  pinMode(leftArrow, INPUT_PULLUP);
  pinMode(downArrow, INPUT_PULLUP);
    pinMode(control, INPUT_PULLUP);
    pinMode(space, INPUT_PULLUP);

  Keyboard.begin();
}

void loop() {
  if (digitalRead(upArrow) == LOW)
  {
    Keyboard.press(KEY_UP_ARROW);
   delay(500);
    Keyboard.releaseAll();
  }
  else if (digitalRead(downArrow) == LOW)
  {
    Keyboard.press(KEY_DOWN_ARROW);
    delay(500);
    Keyboard.releaseAll();
  }
  else if (digitalRead(leftArrow) == LOW)
  {
    Keyboard.press(KEY_LEFT_ARROW);
    delay(500);
    Keyboard.releaseAll();
  }
  else if (digitalRead(rightArrow) == LOW)
  {
    Keyboard.press(KEY_RIGHT_ARROW);
    delay(500);
    Keyboard.releaseAll();
  }
  else if (digitalRead(space) == LOW)
  {
    Keyboard.press(0x20);
    delay(500);
    Keyboard.releaseAll(); 
  }
 else if (digitalRead(control) == LOW)
  {
    Keyboard.press(KEY_LEFT_CTRL);
   
    delay(500);
    Keyboard.releaseAll(); 
  }

}
