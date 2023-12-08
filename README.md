import time
import RPi.GPIO as GPIO

GPIO.setmode(GPIO.BCM)
GPIO.setwarnings(False)
GPIO.setup(16, GPIO.OUT)

my_pwm = GPIO.PWM(16, 300)
my_pwm.start(100)

try:
    while True:
        dutycycle = input("Enter duty cycle (0 to QUIT): ")
        
        if dutycycle == '0':
            break

        my_pwm.ChangeDutyCycle(int(dutycycle))
        time.sleep(0.03)

except KeyboardInterrupt:
    pass

my_pwm.stop()
GPIO.cleanup()
