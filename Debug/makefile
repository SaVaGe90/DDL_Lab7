################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include src/subdir.mk
-include drivers/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 

# All Target
all: DDL_Lab7.axf

# Tool invocations
DDL_Lab7.axf: $(OBJS) $(USER_OBJS)
	@echo 'Building target: $@'
	@echo 'Invoking: MCU Linker'
	arm-none-eabi-gcc -nostdlib -L"C:\Users\Conrad\Documents\LPCXpresso_6.1.2_177\workspace\CMSIS_CORE_LPC11xx\Debug" -Xlinker -Map="DDL_Lab7.map" -Xlinker --gc-sections -mcpu=cortex-m0 -mthumb -T "DDL_Lab7_Debug.ld" -o "DDL_Lab7.axf" $(OBJS) $(USER_OBJS) $(LIBS)
	@echo 'Finished building target: $@'
	@echo ' '
	$(MAKE) --no-print-directory post-build

# Other Targets
clean:
	-$(RM) $(OBJS)$(C_DEPS)$(EXECUTABLES) DDL_Lab7.axf
	-@echo ' '

post-build:
	-@echo 'Performing post-build steps'
	-arm-none-eabi-size "DDL_Lab7.axf"; # arm-none-eabi-objcopy -O binary "DDL_Lab7.axf" "DDL_Lab7.bin" ; checksum -p LPC1114_301 -d "DDL_Lab7.bin";
	-@echo ' '

.PHONY: all clean dependents
.SECONDARY: post-build

-include ../makefile.targets
