# servo
include "servo"
#include <Servo.h>

Servo myservo;  // إنشاء كائن للسيرفو

void setup() {
  myservo.attach(9);  // توصيل السيرفو إلى المنفذ رقم 9
}

void loop() {
  // تحريك السيرفو من 0 إلى 180 درجة
  for (int angle = 0; angle <= 180; angle++) {
    myservo.write(angle);
    delay(15); // تأخير بسيط لإعطاء الوقت للسيرفو للتحرك
  }

  // ثم الرجوع من 180 إلى 0 درجة
  for (int angle = 180; angle >= 0; angle--) {
    myservo.write(angle);
    delay(15);
  }
}

