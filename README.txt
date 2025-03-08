# Opening and Running the Project in STM32CubeIDE

This document provides instructions on how to open, configure, and run the project using STM32CubeIDE.

## Requirements
Before running the project, ensure that the following software is installed:

- [STM32CubeIDE](https://www.st.com/en/development-tools/stm32cubeide.html) (for writing and uploading code)
- **ST-Link drivers** (required for the STM32 board to be recognized by the computer)

## Hardware Connections
The following components must be connected as specified to ensure proper functionality:

- **STM32F4 Development Board**
- **Potentiometer**: Connect to PA0.
- **Servo Motor**: PWM signal should be provided from PA7.
- **LCD Display**:
  - RS: GPIOA, PIN\_5
  - EN: GPIOA, PIN\_6
  - D4: GPIOF, PIN\_14
  - D5: GPIOE, PIN\_11
  - D6: GPIOE, PIN\_9
  - D7: GPIOF, PIN\_13
- **Buzzer**: Connect to GPIOF, PIN\_12.
- **LED Indicators**:
  - Red LED: GPIOE, PIN\_13
  - Green LED: GPIOF, PIN\_15
  - Blue LED: GPIOG, PIN\_14
- **Button**: Connect to GPIOD, PIN\_14.
- **Temperature Sensor (LM35)**: Connect to an ADC input.

## Opening the Project in STM32CubeIDE
Follow these steps to open the project in STM32CubeIDE:

1. Open **STM32CubeIDE**.
2. Navigate to **File** > **Import** > **General**.
3. Select **Existing Projects into Workspace** and click **Next**.
4. Click **Browse** under **Select root directory** and locate the project folder.
5. Once the project appears in the list, click **Finish** to import it.

## Building and Running the Project
To compile and upload the code to the STM32 board:

1. In the **Project Explorer** panel, right-click on the project and select **Build Project**.
2. Once the build process is completed, connect the STM32 board to the computer via USB.
3. Navigate to **Run** > **Run Configurations**.
4. Create a new **STM32 C/C++ Application** configuration.
5. Click **Run** to upload the code to the STM32 board.

## Running in Debug Mode
To execute the code in debug mode:

1. Connect the STM32 board via USB and verify the **ST-Link** connection.
2. Navigate to **Debug** > **Debug Configurations**.
3. Create a new **STM32 GDB Hardware Debug** configuration.
4. Click **Debug** to start the debugging process.

## Project Structure
The project consists of the following files:

- `Core/Src/main.c` → Main source code file.
- `Core/Inc/main.h` → Main header file.
- `Drivers` → STM32 driver files.
- `Startup` → Startup configuration files.
- `lcd.h` and `lcd.c` → Library files for LCD control.

Following these steps will allow you to properly set up, connect the hardware, compile, and run the project in STM32CubeIDE.

