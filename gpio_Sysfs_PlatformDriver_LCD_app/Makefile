obj-m := gpio-sysfs.o
CROSS_COMPILE=arm-linux-gnueabihf-
app: lcd_app.o lcd.o gpio.o lcd_app.elf

lcd_app.o: lcd_app.c
	$(CROSS_COMPILE)gcc -c -o $@ $^

lcd.o: lcd.c
	$(CROSS_COMPILE)gcc -c -o $@ $^

gpio.o: gpio.c
	$(CROSS_COMPILE)gcc -c -o $@ $^

lcd_app.elf: lcd_app.o lcd.o gpio.o
	$(CROSS_COMPILE)gcc -o $@ $^
