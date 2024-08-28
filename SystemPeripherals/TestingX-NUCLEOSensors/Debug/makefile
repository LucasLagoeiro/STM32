################################################################################
# Automatically-generated file. Do not edit!
# Toolchain: GNU Tools for STM32 (12.3.rel1)
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32L4xx_HAL_Driver/Src/subdir.mk
-include Drivers/BSP/IKS01A3/subdir.mk
-include Drivers/BSP/Components/stts751/subdir.mk
-include Drivers/BSP/Components/lsm6dso/subdir.mk
-include Drivers/BSP/Components/lps22hh/subdir.mk
-include Drivers/BSP/Components/lis2mdl/subdir.mk
-include Drivers/BSP/Components/lis2dw12/subdir.mk
-include Drivers/BSP/Components/hts221/subdir.mk
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


BUILD_ARTIFACT_NAME := TestingX-NUCLEOSensors
BUILD_ARTIFACT_EXTENSION := elf
BUILD_ARTIFACT_PREFIX :=
BUILD_ARTIFACT := $(BUILD_ARTIFACT_PREFIX)$(BUILD_ARTIFACT_NAME)$(if $(BUILD_ARTIFACT_EXTENSION),.$(BUILD_ARTIFACT_EXTENSION),)

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
TestingX-NUCLEOSensors.elf \

MAP_FILES += \
TestingX-NUCLEOSensors.map \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
TestingX-NUCLEOSensors.list \


# All Target
all: main-build

# Main-build Target
main-build: TestingX-NUCLEOSensors.elf secondary-outputs

# Tool invocations
TestingX-NUCLEOSensors.elf TestingX-NUCLEOSensors.map: $(OBJS) $(USER_OBJS) C:\Users\lagoeirl\STM32CubeIDE\SystemPeripherals\TestingX-NUCLEOSensors\STM32L452RETX_FLASH.ld makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-gcc -o "TestingX-NUCLEOSensors.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"C:\Users\lagoeirl\STM32CubeIDE\SystemPeripherals\TestingX-NUCLEOSensors\STM32L452RETX_FLASH.ld" --specs=nosys.specs -Wl,-Map="TestingX-NUCLEOSensors.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

TestingX-NUCLEOSensors.list: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "TestingX-NUCLEOSensors.list"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) TestingX-NUCLEOSensors.elf TestingX-NUCLEOSensors.list TestingX-NUCLEOSensors.map default.size.stdout
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST)

fail-specified-linker-script-missing:
	@echo 'Error: Cannot find the specified linker script. Check the linker settings in the build configuration.'
	@exit 2

warn-no-linker-script-specified:
	@echo 'Warning: No linker script specified. Check the linker settings in the build configuration.'

.PHONY: all clean dependents main-build fail-specified-linker-script-missing warn-no-linker-script-specified

-include ../makefile.targets
