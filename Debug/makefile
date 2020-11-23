################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Middlewares/Third_Party/FatFs/src/option/subdir.mk
-include Middlewares/Third_Party/FatFs/src/subdir.mk
-include FATFS/Target/subdir.mk
-include FATFS/App/subdir.mk
-include Drivers/STM32F7xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(S_DEPS)),)
-include $(S_DEPS)
endif
ifneq ($(strip $(S_UPPER_DEPS)),)
-include $(S_UPPER_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
F767ZIFSUnitTest.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
F767ZIFSUnitTest.list \

OBJCOPY_BIN += \
F767ZIFSUnitTest.bin \


# All Target
all: F767ZIFSUnitTest.elf secondary-outputs

# Tool invocations
F767ZIFSUnitTest.elf: $(OBJS) $(USER_OBJS) G:\GitHubSharing\F767ZI_SDCARD\F767ZIFSUnitTest\STM32F767ZITX_FLASH.ld
	arm-none-eabi-gcc -o "F767ZIFSUnitTest.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m7 -T"G:\GitHubSharing\F767ZI_SDCARD\F767ZIFSUnitTest\STM32F767ZITX_FLASH.ld" --specs=nosys.specs -Wl,-Map="F767ZIFSUnitTest.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv5-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

F767ZIFSUnitTest.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "F767ZIFSUnitTest.list"
	@echo 'Finished building: $@'
	@echo ' '

F767ZIFSUnitTest.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "F767ZIFSUnitTest.bin"
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
