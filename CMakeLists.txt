#THIS FILE IS AUTO GENERATED FROM THE TEMPLATE! DO NOT CHANGE!
cmake_minimum_required(VERSION 3.14)

    SET(CMAKE_SYSTEM_NAME Generic)

    SET(CMAKE_SYSTEM_VERSION 1)

    # specify cross compilers and tools
    SET(GCCPATH /Applications/STM32CubeIDE.app/Contents/Eclipse/plugins/com.st.stm32cube.ide.mcu.externaltools.gnu-arm-embedded.7-2018-q2-update.macos64_1.0.0.201904031358/tools/bin)
    SET(CMAKE_C_COMPILER_WORKS 1)
    SET(CMAKE_C_COMPILER ${GCCPATH}/arm-none-eabi-gcc)
    SET(CMAKE_CXX_COMPILER_WORKS 1)
    SET(CMAKE_CXX_COMPILER ${GCCPATH}/arm-none-eabi-g++)
    SET(CMAKE_ASM_COMPILER  ${GCCPATH}/arm-none-eabi-gcc)
    SET(CMAKE_AR ${GCCPATH}/arm-none-eabi-ar)
    SET(CMAKE_OBJCOPY ${GCCPATH}/arm-none-eabi-objcopy)
    SET(CMAKE_OBJDUMP ${GCCPATH}/arm-none-eabi-objdump)
    SET(SIZE ${GCCPATH}/arm-none-eabi-size)

    SET(LINKER_SCRIPT ${CMAKE_SOURCE_DIR}/STM32F103C8Tx_FLASH.ld)

    SET(COMMON_FLAGS "
        -mcpu=cortex-m3 \
        -mthumb \
        -ffunction-sections \
        -fdata-sections \
        -g \
        -fno-common \
        -fmessage-length=0 \
        -specs=nosys.specs \
        -specs=nano.specs \
        -fstack-usage \
        -Wall \
        -O2")

    SET(CMAKE_CXX_FLAGS_INIT "
        ${COMMON_FLAGS} \
        -std=c++14 \
        -fno-rtti \
        -fno-exceptions \
        -fno-threadsafe-statics \
        -fno-use-cxa-atexit")

    SET(CMAKE_C_FLAGS_INIT "${COMMON_FLAGS} -std=gnu99")

    SET(CMAKE_EXE_LINKER_FLAGS_INIT "-u _printf_float -Wl,-gc-sections,--print-memory-usage -T ${LINKER_SCRIPT}")

    PROJECT(UltrasonicSensor C CXX ASM)
    set(CMAKE_CXX_STANDARD 11)

    add_definitions(-D__weak=__attribute__\(\(weak\)\) -D__packed=__attribute__\(\(__packed__\)\) -DUSE_HAL_DRIVER -DSTM32F103xB)

    SET(SOURCES
            startup_stm32f103xb.s
            Src/main.c 
    Src/stm32f1xx_it.c 
    Src/stm32f1xx_hal_msp.c 
    Drivers/STM32F1xx_HAL_Driver/Src/stm32f1xx_hal_gpio_ex.c 
    Drivers/STM32F1xx_HAL_Driver/Src/stm32f1xx_hal_tim.c 
    Drivers/STM32F1xx_HAL_Driver/Src/stm32f1xx_hal_tim_ex.c 
    Drivers/STM32F1xx_HAL_Driver/Src/stm32f1xx_hal.c 
    Drivers/STM32F1xx_HAL_Driver/Src/stm32f1xx_hal_rcc.c 
    Drivers/STM32F1xx_HAL_Driver/Src/stm32f1xx_hal_rcc_ex.c 
    Drivers/STM32F1xx_HAL_Driver/Src/stm32f1xx_hal_gpio.c 
    Drivers/STM32F1xx_HAL_Driver/Src/stm32f1xx_hal_dma.c 
    Drivers/STM32F1xx_HAL_Driver/Src/stm32f1xx_hal_cortex.c 
    Drivers/STM32F1xx_HAL_Driver/Src/stm32f1xx_hal_pwr.c 
    Drivers/STM32F1xx_HAL_Driver/Src/stm32f1xx_hal_flash.c 
    Drivers/STM32F1xx_HAL_Driver/Src/stm32f1xx_hal_flash_ex.c 
    Drivers/STM32F1xx_HAL_Driver/Src/stm32f1xx_hal_exti.c 
    Src/system_stm32f1xx.c 
    Src/freertos.c 
    Src/usb_device.c 
    Src/usbd_conf.c 
    Src/usbd_desc.c 
    Src/usbd_cdc_if.c 
    Src/stm32f1xx_hal_timebase_tim.c 
    Drivers/STM32F1xx_HAL_Driver/Src/stm32f1xx_hal_pcd.c 
    Drivers/STM32F1xx_HAL_Driver/Src/stm32f1xx_hal_pcd_ex.c 
    Drivers/STM32F1xx_HAL_Driver/Src/stm32f1xx_ll_usb.c 
    Middlewares/Third_Party/FreeRTOS/Source/croutine.c 
    Middlewares/Third_Party/FreeRTOS/Source/event_groups.c 
    Middlewares/Third_Party/FreeRTOS/Source/list.c 
    Middlewares/Third_Party/FreeRTOS/Source/queue.c 
    Middlewares/Third_Party/FreeRTOS/Source/stream_buffer.c 
    Middlewares/Third_Party/FreeRTOS/Source/tasks.c 
    Middlewares/Third_Party/FreeRTOS/Source/timers.c 
    Middlewares/Third_Party/FreeRTOS/Source/CMSIS_RTOS_V2/cmsis_os2.c 
    Middlewares/Third_Party/FreeRTOS/Source/portable/MemMang/heap_4.c 
    Middlewares/Third_Party/FreeRTOS/Source/portable/GCC/ARM_CM3/port.c 
    Middlewares/ST/STM32_USB_Device_Library/Core/Src/usbd_core.c 
    Middlewares/ST/STM32_USB_Device_Library/Core/Src/usbd_ctlreq.c 
    Middlewares/ST/STM32_USB_Device_Library/Core/Src/usbd_ioreq.c 
    Middlewares/ST/STM32_USB_Device_Library/Class/CDC/Src/usbd_cdc.c
)

    include_directories(
            Inc 
    Drivers/STM32F1xx_HAL_Driver/Inc 
    Drivers/STM32F1xx_HAL_Driver/Inc/Legacy 
    Drivers/CMSIS/Device/ST/STM32F1xx/Include 
    Drivers/CMSIS/Include 
    Drivers/CMSIS/Include 
    Middlewares/Third_Party/FreeRTOS/Source/include 
    Middlewares/Third_Party/FreeRTOS/Source/CMSIS_RTOS_V2 
    Middlewares/Third_Party/FreeRTOS/Source/portable/GCC/ARM_CM3 
    Middlewares/ST/STM32_USB_Device_Library/Core/Inc 
    Middlewares/ST/STM32_USB_Device_Library/Class/CDC/Inc
            )

    add_executable(${PROJECT_NAME}.elf ${SOURCES} ${LINKER_SCRIPT})

    set(CMAKE_EXE_LINKER_FLAGS
            "${CMAKE_EXE_LINKER_FLAGS} -Wl,-Map=${PROJECT_BINARY_DIR}/${PROJECT_NAME}.map")

    set(HEX_FILE ${PROJECT_BINARY_DIR}/${PROJECT_NAME}.hex)
    set(BIN_FILE ${PROJECT_BINARY_DIR}/${PROJECT_NAME}.bin)

    add_custom_command(TARGET ${PROJECT_NAME}.elf POST_BUILD
            COMMAND ${CMAKE_OBJCOPY} -Oihex $<TARGET_FILE:${PROJECT_NAME}.elf> ${HEX_FILE}
            COMMAND ${CMAKE_OBJCOPY} -Obinary $<TARGET_FILE:${PROJECT_NAME}.elf> ${BIN_FILE}
            COMMAND ${SIZE} -B ${PROJECT_NAME}.elf
            COMMENT "Building ${HEX_FILE}
    Building ${BIN_FILE}")
