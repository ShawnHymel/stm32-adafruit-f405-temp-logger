################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Startup/subdir.mk
-include Src/subdir.mk
-include Middlewares/Third_Party/FatFs/src/option/subdir.mk
-include Middlewares/Third_Party/FatFs/src/subdir.mk
-include Middlewares/ST/STM32_USB_Device_Library/Core/Src/subdir.mk
-include Middlewares/ST/STM32_USB_Device_Library/Class/CDC/Src/subdir.mk
-include Drivers/STM32F4xx_HAL_Driver/Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
adafruit-f405-temp-logger.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
adafruit-f405-temp-logger.list \

OBJCOPY_BIN += \
adafruit-f405-temp-logger.bin \


# All Target
all: adafruit-f405-temp-logger.elf secondary-outputs

# Tool invocations
adafruit-f405-temp-logger.elf: $(OBJS) $(USER_OBJS) C:\Users\sgmustadio\STM32CubeIDE\workspace_1.0.1\adafruit-f405-temp-logger\STM32F405RGTX_FLASH.ld
	arm-none-eabi-gcc -o "adafruit-f405-temp-logger.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"C:\Users\sgmustadio\STM32CubeIDE\workspace_1.0.1\adafruit-f405-temp-logger\STM32F405RGTX_FLASH.ld" --specs=nosys.specs -Wl,-Map="adafruit-f405-temp-logger.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

adafruit-f405-temp-logger.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "adafruit-f405-temp-logger.list"
	@echo 'Finished building: $@'
	@echo ' '

adafruit-f405-temp-logger.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "adafruit-f405-temp-logger.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
