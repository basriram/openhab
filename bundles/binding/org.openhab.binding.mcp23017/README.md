## Introduction
This binding provides native access for MCP23017 16 bit bidirectional I/O expander
on I2C bus. Please consider datasheet for IC for future information.

## Generic Item Binding Configuration
Since MCP23017 is digital IO expander for I2C bus, only two types of items are supported:
`Contact` for pins that used as digital input and `Switch` for digital output. Find the
example below.

# Binding Configuration in openhab.cfg
No special cofiguration within openhab.cfg is need.

# Item Configuration
`Contact Test1 "Test 1" (Tests) { mcp23017="{ address:20, pin:'A0', mode:'DIGITAL_INPUT'}" }`
configures pin 0 at bank A (GPA0 on datasheet) as input of the IC on address 0x20

`Switch Test2 "Test 2" (Tests) { mcp23017="{ address:21, pin:'B1', mode:'DIGITAL_OUTPUT', defaultState:'LOW'}" }`
configures pin 1 at bank B (GPB1 on datasheet) as output of the IC on adress 0x21
