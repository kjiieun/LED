import time
import RPi.GPIO as GPIO

GPIO.setmode(GPIO.BCM)
GPIO.setwarnings(False)
GPIO.setup(16, GPIO.OUT)

my_pym = GPIO, PWM(16, 300)
my_pwm.start(100)

try:
while True:
dutycycle == '0':
break

my,pwm.ChangeDutyCycle(int(dutycycle))
time.sleep(0.03)

except KeyboardInterrupt:
pass

my_pwm.(stop)
GPIO.cleanup()
