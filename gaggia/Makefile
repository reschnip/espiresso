gaggia: gaggia.cpp settings.h \
	pwm.o inputs.o timing.o pid.o gpio.o temperature.o boiler.o keyboard.o \
	gpiopin.o ranger.o flow.o system.o pump.o display.o regulator.o adc.o tsic.o \
	pigpiomgr.o hcsr04.o pressure.o
	g++ -o gaggia gaggia.cpp \
	pwm.o inputs.o timing.o pid.o gpio.o temperature.o boiler.o keyboard.o \
	gpiopin.o ranger.o flow.o system.o pump.o display.o regulator.o adc.o tsic.o \
	pigpiomgr.o hcsr04.o pressure.o \
	-lrt -lpthread -std=c++0x -lSDL \
	-lSDLmain -lSDL_ttf -lSDL_image \
	-lpigpiod_if

pwm.o: pwm.h pwm.cpp settings.h
	g++ -c pwm.cpp

temperature.o: temperature.h temperature.cpp tsic.h tsic.o settings.h
	g++ -c temperature.cpp -std=c++0x

timing.o: timing.h timing.cpp
	g++ -c timing.cpp

pid.o: pid.h pid.cpp
	g++ -c pid.cpp

gpio.o: gpio.h gpio.cpp
	g++ -c gpio.cpp

boiler.o: boiler.h boiler.cpp settings.h
	g++ -c boiler.cpp

keyboard.o: keyboard.h keyboard.cpp
	g++ -c keyboard.cpp

inputs.o: inputs.h inputs.cpp
	g++ -c inputs.cpp -std=c++0x

gpiopin.o: gpiopin.h gpiopin.cpp
	g++ -c gpiopin.cpp -std=c++0x

ranger.o: ranger.h ranger.cpp settings.h
	g++ -c ranger.cpp -std=c++0x

hcsr04.o: hcsr04.h hcsr04.cpp settings.h
	g++ -c hcsr04.cpp -std=c++0x

flow.o: flow.h flow.cpp settings.h
	g++ -c flow.cpp -std=c++0x

pump.o: pump.h pump.cpp settings.h
	g++ -c pump.cpp -std=c++0x

system.o: system.h system.cpp
	g++ -c system.cpp

display.o: display.h display.cpp
	g++ -c display.cpp -std=c++0x

regulator.o: regulator.h regulator.cpp
	g++ -c regulator.cpp -std=c++0x

adc.o: adc.h adc.cpp
	g++ -c adc.cpp -std=c++0x

tsic.o: tsic.h tsic.cpp pigpiomgr.h
	g++ -c tsic.cpp -std=c++0x

pigpiomgr.o: pigpiomgr.h pigpiomgr.cpp
	g++ -c pigpiomgr.cpp

pressure.o: pressure.h pressure.cpp
	g++ -c pressure.cpp -std=c++0x
