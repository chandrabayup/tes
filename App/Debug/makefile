################################################################################
# Automatically-generated file. Do not edit!
# Toolchain: GNU Tools for STM32 (10.3-2021.10)
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32G0xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
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

OPTIONAL_TOOL_DEPS := \
$(wildcard ../makefile.defs) \
$(wildcard ../makefile.init) \
$(wildcard ../makefile.targets) \


BUILD_ARTIFACT_NAME := App
BUILD_ARTIFACT_EXTENSION := elf
BUILD_ARTIFACT_PREFIX :=
BUILD_ARTIFACT := $(BUILD_ARTIFACT_PREFIX)$(BUILD_ARTIFACT_NAME)$(if $(BUILD_ARTIFACT_EXTENSION),.$(BUILD_ARTIFACT_EXTENSION),)

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
App.elf \

MAP_FILES += \
App.map \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
App.list \

OBJCOPY_BIN += \
App.bin \


# All Target
all: main-build

# Main-build Target
main-build: App.elf secondary-outputs

dependents:
	-cd /home/chandra/Chandra\ File/FOTA/Simple\ Bootloader/MyStaticLib/Debug && $(MAKE) all

# Tool invocations
App.elf App.map: $(OBJS) $(USER_OBJS) /home/chandra/Chandra\ File/FOTA/Simple\ Bootloader/MyStaticLib/Debug/libMyStaticLib.a /home/chandra/Chandra\ File/FOTA/Simple\ Bootloader/App/STM32G071RBTX_FLASH.ld makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-gcc -o "App.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m0plus -T"/home/chandra/Chandra File/FOTA/Simple Bootloader/App/STM32G071RBTX_FLASH.ld" --specs=nosys.specs -Wl,-Map="App.map" -Wl,--gc-sections -static -L"/home/chandra/Chandra File/FOTA/Simple Bootloader/MyStaticLib/Debug" --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

App.list: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "App.list"
	@echo 'Finished building: $@'
	@echo ' '

App.bin: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "App.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) App.bin App.elf App.list App.map default.size.stdout
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_BIN)

fail-specified-linker-script-missing:
	@echo 'Error: Cannot find the specified linker script. Check the linker settings in the build configuration.'
	@exit 2

warn-no-linker-script-specified:
	@echo 'Warning: No linker script specified. Check the linker settings in the build configuration.'

.PHONY: all clean dependents main-build fail-specified-linker-script-missing warn-no-linker-script-specified
/home/chandra/Chandra\ File/FOTA/Simple\ Bootloader/MyStaticLib/Debug/libMyStaticLib.a:

-include ../makefile.targets
