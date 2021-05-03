ASRR OEM command - 04/15/2021
===
<details>
  <summary>History</summary>

| 7  | Fix 0xBD/BE, SET_BIOS_POST_STATUS, GET_BIOS_POST_STATUS definition
| 6  | Update 0x86/0x87, SET_FW_VERSION_INFO, GET_FW_VERSION_INFO add NIC1 and NIC2 version.
| 5  | Update 0xB9/0xBA, SET_SMI_ACTION, GET_SMI_ACTION for RTC sync.
| 4  | Update 0xB9/0xBA, SET_SMI_ACTION, GET_SMI_ACTION.
| 3  | Update 0x86/0x87, SET_FW_VERSION_INFO, GET_FW_VERSION_INFO BIOS version format.
| 2  | Update 0xE0 0x06, SET_RUNCM_REQ and 0xE0 0x09 GET_RUNCM_REQ, to support CM and nodes commands.
| 1  | Update 0xA0 SET_MAC_ADDR, 0xA1 GET_MAC_ADDR to support bit map for internal USB LAN MAC address

</details>

# NetFn: 0x3A
<details>
  <summary>Cmd: 0x01 SET_SMART_FAN (depreated)</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | CPU1_FAN1 PWM or FAN1 PWM
|              |      | 00h: auto fan control (Smart fan)
|              |      | 01h~100h: 1%~100% (Manual fan)
|              | 2    | CPU2_FAN2 PWM or FAN2 PWM
|              |      | 00h: auto fan control (Smart fan)
|              |      | 01h~100h: 1%~100% (Manual fan)
|              | 3    | REAR_FAN1 PWM or FAN3 PWM
|              |      | 00h: auto fan control (Smart fan)
|              |      | 01h~100h: 1%~100% (Manual fan)
|              | 4    | REAR_FAN2 PWM or FAN4 PWM
|              |      | 00h: auto fan control (Smart fan)
|              |      | 01h~100h: 1%~100% (Manual fan)
|              | 5    | FRNT_FAN1 PWM or FAN5 PWM
|              |      | 00h: auto fan control (Smart fan)
|              |      | 01h~100h: 1%~100% (Manual fan)
|              | 6    | FRNT_FAN2 PWM or FAN6 PWM
|              |      | 00h: auto fan control (Smart fan)
|              |      | 01h~100h: 1%~100% (Manual fan)
|              | 7    | FRNT_FAN3 PWM or FAN7 PWM
|              |      | 00h: auto fan control (Smart fan)
|              |      | 01h~100h: 1%~100% (Manual fan)
|              | 8    | FRNT_FAN4 PWM or FAN8 PWM
|              |      | 00h: auto fan control (Smart fan)
|              |      | 01h~100h: 1%~100% (Manual fan)
|              | 9    | FRNT_FAN5 PWM or FAN9 PWM
|              |      | 00h: auto fan control (Smart fan)
|              |      | 01h~100h: 1%~100% (Manual fan)

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
</details>

<details>
  <summary>Cmd: 0x02 GET_SMART_FAN (depreated)</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | -    | -

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
|              | 2    | CPU1_FAN1 PWM or FAN1 PWM
|              |      | 00h: auto fan control (Smart fan)
|              |      | 01h~100h: 1%~100% (Manual fan)
|              | 3    | CPU2_FAN2 PWM or FAN2 PWM
|              |      | 00h: auto fan control (Smart fan)
|              |      | 01h~100h: 1%~100% (Manual fan)
|              | 4    | REAR_FAN1 PWM or FAN3 PWM
|              |      | 00h: auto fan control (Smart fan)
|              |      | 01h~100h: 1%~100% (Manual fan)
|              | 5    | REAR_FAN2 PWM or FAN4 PWM
|              |      | 00h: auto fan control (Smart fan)
|              |      | 01h~100h: 1%~100% (Manual fan)
|              | 6    | FRNT_FAN1 PWM or FAN5 PWM
|              |      | 00h: auto fan control (Smart fan)
|              |      | 01h~100h: 1%~100% (Manual fan)
|              | 7    | FRNT_FAN2 PWM or FAN6 PWM
|              |      | 00h: auto fan control (Smart fan)
|              |      | 01h~100h: 1%~100% (Manual fan)
|              | 8    | FRNT_FAN3 PWM or FAN7 PWM
|              |      | 00h: auto fan control (Smart fan)
|              |      | 01h~100h: 1%~100% (Manual fan)
|              | 9    | FRNT_FAN4 PWM or FAN8 PWM
|              |      | 00h: auto fan control (Smart fan)
|              |      | 01h~100h: 1%~100% (Manual fan)
|              | 10   | FRNT_FAN5 PWM or FAN9 PWM
|              |      | 00h: auto fan control (Smart fan)
|              |      | 01h~100h: 1%~100% (Manual fan)
</details>

<details>
  <summary>Cmd: 0x05 SET_SMART_FAN_TABLE (depreated)</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Table selector
|              |      | 01h: Duty table
|              |      | 02h: Temp table
|              | 2    | reserved
|              | 3:13 | Table value: table[0]~table[10]

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
</details>

<details>
  <summary>Cmd: 0x06 GET_SMART_FAN_TABLE (depreated)</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Table selector
|              |      | 01h: Duty table
|              |      | 02h: Temp table
|              | 2    | reserved

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
|              | 2    | reserved
|              | 3:13 | Table value: table[0]~table[10]
</details>


<details>
  <summary>Cmd: 0x07 GET_DELAY_TIME (depreated)</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Parameter selector
|              |      |	01h: Set LAN2 to static(bond disable)
|              |      |	02h: Set LAN2 to dynamic(need bond disable)
|              |      |	03h: Bond disable
|              |      |	04h: Bond enable

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
|              | 2    |	Req1=01h: Wait for set LAN2 Static second
|              |	  | Req1=02h: Wait for set LAN2 dynamic second
|              |	  | Req1=03h: Wait for get current IP(after set both LAN1 and LAN2 to dynamic)
|              |	  | Req1=04h: Wait for get current IP(after set LAN to dynamic)
|              | (3)  |	Req1=01h: Wait for set LAN2 IP address second
|              |	  | Req1=02h: N/A
|              |	  | Req1=03h: Wait for get current IP(after set both LAN1 and LAN2 to static)
|              |	  | Req1=04h: Wait for get current IP(after set LAN to static)
|              | (4)  | Req1=01h: Wait for set LAN2 Subnet mask second
|              |	  | Req1=02h: N/A
|              |	  | Req1=03h: Wait for get current IP(after set one LAN to dynamic)
|              |	  | Req1=04h: N/A
|              | (5)  | Req1=01h: Wait for set LAN2 Gateway IP second
|              |	  | Req1=02h: N/A
|              |	  | Req1=03h: Wait for get current IP(after set one LAN to static)
|              |	  | Req1=04h: N/A

</details>

<details>
  <summary>Cmd: 0x08 SET_DELAY_TIME (depreated)</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Parameter selector
|              |      |	01h: Set LAN2 to static(bond disable)
|              |      |	02h: Set LAN2 to dynamic(need bond disable)
|              |      |	03h: Bond disable
|              |      |	04h: Bond enable
|              | 2    |	Req1=01h: Wait for set LAN2 Static second
|              |	  | Req1=02h: Wait for set LAN2 dynamic second
|              |	  | Req1=03h: Wait for get current IP(after set both LAN1 and LAN2 to dynamic)
|              |	  | Req1=04h: Wait for get current IP(after set LAN to dynamic)
|              | (3)  |	Req1=01h: Wait for set LAN2 IP address second
|              |	  | Req1=02h: N/A
|              |	  | Req1=03h: Wait for get current IP(after set both LAN1 and LAN2 to static)
|              |	  | Req1=04h: Wait for get current IP(after set LAN to static)
|              | (4)  | Req1=01h: Wait for set LAN2 Subnet mask second
|              |	  | Req1=02h: N/A
|              |	  | Req1=03h: Wait for get current IP(after set one LAN to dynamic)
|              |	  | Req1=04h: N/A
|              | (5)  | Req1=01h: Wait for set LAN2 Gateway IP second
|              |	  | Req1=02h: N/A
|              |	  | Req1=03h: Wait for get current IP(after set one LAN to static)
|              |	  | Req1=04h: N/A

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code

</details>

<details>
  <summary>Cmd: 0x09 SET_REMOTE_SHELL (depreated)</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | SSH path
|              |      |	00h: Shell
|              |      |	01h: SOLSSH

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code

</details>

<details>
  <summary>Cmd: 0x0A GET_REMOTE_SHELL (depreated)</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | -    | -

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
|              | 2    | SSH path
|              |      |	00h: Shell
|              |      |	01h: SOLSSH
</details>

<details>
  <summary>Cmd: 0x10 SET_GPIO</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | GPIO number
|              | 2    |	Direction
|              |      | 00h: Input
|              |      | 01h: Output
|              | 3    | Value(only valid when direction is output)
|              |      | 00h: Low
|              |      | 01h: High

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
|              |      | 82h: It's not GPIO
|              | 2    | GPIO number
|              | 3    | Direction
|              |	  | 00h: Input
|              |	  | 01h: Output
|              | 4    | Value(only valid when direction is output)
|              |	  | 00h: Low
|              |	  | 01h: High
</details>

<details>
  <summary>Cmd: 0x11 GET_GPIO</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | GPIO number

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
|              | 2    | GPIO number
|              | 3    | Function
|              |	  | 00h: This isn't GPIO
|              |	  | 01h: This is GPIO
|              | 4    | Direction(only valid when it's gpio)
|              |	  | 00h: Input
|              |	  | 01h: Output
|              | 5    | Value(only valid when direction is output)
|              |	  | 00h: Low
|              |	  | 01h: High
</details>

<details>
  <summary>Cmd: 0x12 SET_PULL</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Bit [23:16] of SCU8C register.
|              |      | Bit [31:24] of SCU8C register.

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
|              | 2    | Bit [23:16] of SCU8C register.
|              | 3    | Bit [31:24] of SCU8C register.
</details>

<details>
  <summary>Cmd: 0x13 GET_PULL</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | -    | -

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
|              | 2    | Bit [23:16] of SCU8C register.
|              | 3    | Bit [31:24] of SCU8C register.
</details>

<details>
  <summary>Cmd: 0x20 SET_NCSI_SWITCH</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | NCSI selector

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
</details>

<details>
  <summary>Cmd: 0x21 GET_NCSI_SWITCH</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | -    | -

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
|              | 2    | NCSI selector
</details>

<details>
  <summary>Cmd: 0x52 MASTER_WRITE_READ</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | I2C Bus
|              | 2    | Slave Address
|              | 3    | Read Count
|              | 4:N  | Data – max size 50 bytes

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
|              | 2:N  | Data read
</details>

<details>
  <summary>Cmd: 0x66 ASROCK_RESTOREDEFAULT</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Reset selector
|              |      | 01h: Reboot BMC
|              |      | 02h: Enable runlevel 8

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
</details>

<details>
  <summary>Cmd: 0x67 BOOT_COMPLETE</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | -    | -

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
|              | 2    | Boot state
|              |      | 00h: BMC is booting
|              |      | 01h: Boot complete
</details>

<details>
  <summary>Cmd: 0x68 ASROCK_IDENTIFY</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1:N  | Verification key

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
|              | 2:N  | Verification hash
</details>

<details>
  <summary>Cmd: 0x73 GET_BIOS_CODE</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Command
|              |      | 00h: Current BIOS code
|              |      | 01h: Previous BIOS code
|              |      | 02h: Current BIOS code length
|              |      | 03h: Previous BIOS code length
|              | 2    | Sequence number (Available for command 00h, 01h)

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
|              |      | 00h: Success
|              |      | 80h: Invalid sequence number, for command 00h, 01h
|              | 2:N  | For command 00h, 01h
|              |      | BIOS code: return 32 bytes, last sequence may return less than 32 bytes
|              | 2:3  | For command 02h, 03h
|              |      | BIOS code length (LSB first)
</details>

<details>
  <summary>Cmd: 0x80 SET_ACCESS_BMC_BY_KCS_STATUS</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | KCS config
|              |      | 00h: Disable
|              |      | 01h: Enable

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
</details>

<details>
  <summary>Cmd: 0x81 GET_ACCESS_BMC_BY_KCS_STATUS</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | -    | -

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
|              | 2    | KCS config
|              |      | 00h: Disable
|              |      | 01h: Enable
</details>

<details>
  <summary>Cmd: 0x82 SET_SENSOR_MONITOR</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Sensor monitor config
|              |      | 00h: Disable
|              |      | 01h: Enable

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
</details>

<details>
  <summary>Cmd: 0x83 GET_SENSOR_MONITOR</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | -    | -

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
|              | 2    | Sensor monitor config
|              |      | 00h: Disable
|              |      | 01h: Enable
</details>

<details>
  <summary>Cmd: 0x84 SET_BIOS_PRESERVE_SETTING</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | BIOS preserve setting
|              |      | 00h: Disable
|              |      | 01h: Enable
|              |      | 02h: Delete BIOS preserve file (do not change disable/enable setting)

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
</details>

<details>
  <summary>Cmd: 0x85 GET_BIOS_PRESERVE_SETTING</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | -    | -

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
|              | 2    | BIOS preserve setting
|              |      | 00h: Disable
|              |      | 01h: Enable
</details>

<details>
  <summary>Cmd: 0x86 SET_FW_VERSION_INFO</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Selector
|              | 2:N  | Version data, format difference according to selector
|              |      | Maximum 16 bytes

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code

| Selector | Name      | byte | data field                               |
| -------- | --------- | ---- | ---------------------------------------- |
| 0        | BIOS      | 1    | Major (1 ~ 99)
|          |           | 2    | Minor (00 ~ 99)
|          |           | 3:4  | OEM code (ASCII)
|          |           |      | Hex 0000: not use, no display
|          |           | 5    | Build (01 ~ 99)
|          |           |      | 00: not use, no display
|          |           | 6:10 | Tag (ASCII)
| 1        | BMC       | 1    | Major
|          |           | 2    | Minor
|          |           | 3    | Aux
| 2        | Microcode | 1    | Major
|          |           | 2    | Minor
|          |           | 3    | Aux
|          |           | 4    | Build
| 3        | Intel ME  | 1:2  | Major
|          |           | 3:4  | Minor
|          |           | 5:6  | Aux
|          |           | 7:8  | Build
| 4        | AMD PSP   | 1:2  | Major
|          |           | 3:4  | Minor
|          |           | 5:6  | Aux
|          |           | 7:8  | Build
| 5        | AMD AGESA | 1    | Major
|          |           | 2    | Minor
|          |           | 3    | Aux
|          |           | 4    | Build
| 6        | AMD SMU   | 1    | Major
|          |           | 2    | Minor
|          |           | 3    | Aux
|          |           | 4    | Build
| 7        | AMD ABL   | 1    | Major
|          |           | 2    | Minor
|          |           | 3    | Aux
|          |           | 4    | Build
| 8        | CPLD      | 1    | Major
|          |           | 2    | Minor
| 9        | PSU1      | 1    | Major
|          |           | 2    | Minor
| 10       | PSU2      | 1    | Major
|          |           | 2    | Minor
| 11       | NIC1      | 1    | Major
|          |           | 2    | Minor
|          |           | 3    | Aux
| 12       | NIC2      | 1    | Major
|          |           | 2    | Minor
|          |           | 3    | Aux
</details>

<details>
  <summary>Cmd: 0x87 GET_FW_VERSION_INFO</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Selector

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
|              | 2:N  | Version data, format difference according to selector
|              |      | Maximum 16 bytes

| Selector | Name      | byte | data field                               |
| -------- | --------- | ---- | ---------------------------------------- |
| 0        | BIOS      | 2    | Major (1 ~ 99)
|          |           | 3    | Minor (00 ~ 99)
|          |           | 4:5  | OEM code (ASCII)
|          |           |      | Hex 0000: not use, no display
|          |           | 6    | Build (01 ~ 99)
|          |           |      | 00: not use, no display
|          |           | 7:11 | Tag (ASCII)
| 1        | BMC       | 2    | Major
|          |           | 3    | Minor
|          |           | 4    | Aux
| 2        | Microcode | 2    | Major
|          |           | 3    | Minor
|          |           | 4    | Aux
|          |           | 5    | Build
| 3        | Intel ME  | 2:3  | Major
|          |           | 4:5  | Minor
|          |           | 6:7  | Aux
|          |           | 8:9  | Build
| 4        | AMD PSP   | 2:3  | Major
|          |           | 4:5  | Minor
|          |           | 6:7  | Aux
|          |           | 8:9  | Build
| 5        | AMD AGESA | 2    | Major
|          |           | 3    | Minor
|          |           | 4    | Aux
|          |           | 5    | Build
| 6        | AMD SMU   | 2    | Major
|          |           | 3    | Minor
|          |           | 4    | Aux
|          |           | 5    | Build
| 7        | AMD ABL   | 2    | Major
|          |           | 3    | Minor
|          |           | 4    | Aux
|          |           | 5    | Build
| 8        | CPLD      | 2    | Major
|          |           | 3    | Minor
| 9        | PSU1      | 2    | Major
|          |           | 3    | Minor
| 10       | PSU2      | 2    | Major
|          |           | 3    | Minor
| 11       | NIC1      | 1    | Major
|          |           | 2    | Minor
|          |           | 3    | Aux
| 12       | NIC2      | 1    | Major
|          |           | 2    | Minor
|          |           | 3    | Aux
</details>

<details>
  <summary>Cmd: 0xA0 SET_MAC_ADDR</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | MAC selector
|              |      | If bit7 = 0
|              |      |  00h: eth0
|              |      |  01h: eth1
|              |      |  02h: eht0 and eth1
|              |      | If Bit7 = 1
|              |      |  Bit0: eth0
|              |      |  Bit1: eth1
|              |      |  Bit2: USB Host MAC
|              |      |  Bit3: USB Decive MAC
|              | 2:7  | MAC address
|              | 8:13 | MAC2 address (if eth1 selected)
|              | 14:19| MAC3 address (if USB Host selected)
|              | 20:25| MAC4 address (if USB Dev selected)    
| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
</details>

<details>
  <summary>Cmd: 0xA1 GET_MAC_ADDR</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | MAC selector
|              |      | If bit7 = 0
|              |      |  00h: eth0
|              |      |  01h: eth1
|              |      |  02h: eht0 and eth1
|              |      | If Bit7 = 1
|              |      |  Bit0: eth0
|              |      |  Bit1: eth1
|              |      |  Bit2: USB Host MAC
|              |      |  Bit3: USB Decive MAC

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
|              | 2:7  | MAC address
|              | 8:13 | MAC2 address (if eth1 selected)
|              | 14:19| MAC3 address (if USB Host selected)
|              | 20:25| MAC4 address (if USB Dev selected)    
</details>

<details>
  <summary>Cmd: 0xA2 SET_REG_VALUE</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1:4  | Register (MSB first)
|              | 5:8  | Value (MSB first)

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
</details>

<details>
  <summary>Cmd: 0xA3 GET_REG_VALUE</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1:4  | Register (MSB first)

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
|              | 2:5  | Value (MSB first)
</details>

<details>
  <summary>Cmd: 0xA4 SET_SYSTEM_SMI</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | System state

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
</details>

<details>
  <summary>Cmd: 0xA5 GET_DEV_FW_INFO</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | -    | -

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
|              | 2    | BMC FW version (major)
|              | 3    | BMC FW version (minor, BCD encoded)
|              | 4    | BIOS FW versio Phase
|              |      | 01h: L version
|              |      | 02h: P version
|              | 5    | BIOS FW version (major)
|              | 6    | BIOS FW version (minor, BCD encoded)
|              | 7    | Special BIOS FW version (ASCII, e.g. 'a', 'A')
|              | 8:9  | ME (or PSP) FW version (major, LSB firs)
|              | 10:11| ME (or PSP) FW version (minor, LSB first)
|              | 12:13| ME (or PSP) FW version (aux_1, LSB first)
|              | 14:15| ME (or PSP) FW version (aux_2, LSB first)
|              | 16:19| Micro code version(MSB first)
|              | 20   | CPLD version (major, BCD encoded)
|              | 21   | CPLD version (minor, BCD encoded)
</details>

<details>
  <summary>Cmd: 0xA6 GET_SYSTEM_SMI</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | -    | -

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
|              | 2    | System state
</details>

<details>
  <summary>Cmd: 0xA7 GET_MODEL_NAME</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | -    | -

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
|              | 2:N  | FW model name
</details>

<details>
  <summary>Cmd: 0xA8 SET_MODELNAME_VRTCTL</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Verification control data
|              |      | [7:2] - reserved
|              |      | [1] - BIOS verification
|              |      |       0b disable
|              |      |       1b enable
|              |      | [0] - BMC verification
|              |      |       0b disable
|              |      |       1b enable

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
</details>

<details>
  <summary>Cmd: 0xA9 GET_MODELNAME_VRTCTL</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | -    | -

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
|              |      | [7:2] - reserved
|              |      | [1] - BIOS verification
|              |      |       0b disable
|              |      |       1b enable
|              |      | [0] - BMC verification
|              |      |       0b disable
|              |      |       1b enable
</details>

<details>
  <summary>Cmd: 0xAA SET_CHASSIS_ID</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1:N  | Chassis ID (31-bytes max.)

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
</details>

<details>
  <summary>Cmd: 0xAB SET_CHASSIS_ID</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | -    | -

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
|              | 2:N  | Chassis ID (31-bytes max.)
</details>

<details>
  <summary>Cmd: 0xB0 SET_SYSTEM_MAC_ADDR</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | MAC selector
|              |      | 00h: system MAC1
|              |      | 01h: system MAC2
|              |      | 02h: system MAC3
|              |      | 03h: system MAC4
|              |      | 04h: system MAC5
|              |      | 05h: system MAC6
|              |      | 06h: system MAC7
|              |      | 07h: system MAC8
|              | 2:7  | MAC address

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
</details>

<details>
  <summary>Cmd: 0xB1 GET_SYSTEM_MAC_ADDR</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | MAC selector
|              |      | 00h: system MAC1
|              |      | 01h: system MAC2
|              |      | 02h: system MAC3
|              |      | 03h: system MAC4
|              |      | 04h: system MAC5
|              |      | 05h: system MAC6
|              |      | 06h: system MAC7
|              |      | 07h: system MAC8

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
|              | 2:7  | MAC address
</details>

<details>
  <summary>Cmd: 0xB2 SET_BIOS_FW_INFO</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | BIOS FW version Phase
|              |      | 01h: L version
|              |      | 02h: P version
|              | 2    | Major
|              | 3    | Minor (BCD encoded)
|              | 4    | Special BIOS FW version (ASCII, e.g. 'a', 'A')
|              | 5:8  | Micro code version(MSB first)
|              | 9:10 |	ME FW version (major, LSB firs)
|              | 11:12|	ME FW version (minor, LSB first)
|              | 13:14|	ME FW version (aux_1, LSB first)
|              | 15:16|	ME FW version (aux_2, LSB first)

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
</details>

<details>
  <summary>Cmd: 0xB3 SET_RING_IN_CONTROL</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Ring in control
|              |      | Disable auto wake up
|              |      | Enable auto wake up

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
</details>

<details>
  <summary>Cmd: 0xB4 SET_SPEAKER_FUNC</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Long beep count (0 ~ 3)
|              | 2    | Short beep count (0 ~ 11)

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
</details>

<details>
  <summary>Cmd: 0xB5 SET_BIOS_MODEL_NAME</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | 00h: MB Model name
|              |      | 01h: System product name
|              | 2:N  | Name (ASCII)

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
</details>

<details>
  <summary>Cmd: 0xB6 GET_BIOS_MODEL_NAME</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | 00h: MB Model name
|              |      | 01h: System product name

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
|              | 2:N  | Name (ASCII)
</details>

<details>
  <summary>Cmd: 0xB7 SET_INVENTORY_INFO_CTL</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Inventory control
|              |      | 00h: Disable
|              |      | 01h: Enable

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
</details>

<details>
  <summary>Cmd: 0xB8 GET_INVENTORY_INFO_CTL</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | -    | -

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
|              | 2    | Inventory control
|              |      | 00h: Disable
|              |      | 01h: Enable
</details>

<details>
  <summary>Cmd: 0xB9 SET_SMI_ACTION</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Command
|              |      | 0: Trigger SMI to BIOS
|              |      | 1: Set SMI Action flag
|              | 2    | SMI Action Flag (Available only if Action=1)
|              |      | 0: None
|              |      | 1: SMI Shutdown
|              |      | 2: RTC Sync (Set SEL time)
|              |      | Others: Reserved

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
</details>

<details>
  <summary>Cmd: 0xBA GET_SMI_ACTION</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Command
|              |      | 0: Return SMI Action Flag
|              |      | others: Reserved, return error

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
|              | 2    | SMI Action Flag
|              |      | 0: None
|              |      | 1: SMI Shutdown
|              |      | 2: RTC Sync (Set SEL time)
|              |      | Others: Reserved
|              |      | Note: SMI Action Flag will be cleared after read
</details>

<details>
  <summary>Cmd: 0xBB GET_CERT_STATUS</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | -    | -

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
|              | 2:5  | File length of CA(LSB first)
|              | 6:9  | CRC 32 Checksum of CA file(LSB first)
</details>

<details>
  <summary>Cmd: 0xBC GET_SSL_CERT</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Sequence number

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
|              | 2    | Sequence number
|              | 3    | Checksum
|              | 4:131| Sequence data of CA file
</details>

<details>
  <summary>Cmd: 0xBD SET_BIOS_POST_STATUS</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | BIOS POST status
|              |      | 01h: POST start
|              |      | 02h: POST end

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
</details>

<details>
  <summary>Cmd: 0xBE GET_BIOS_POST_STATUS</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | -    | -

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
|              | 2    | BIOS POST status
|              |      | 00h: Unknown
|              |      | 01h: POST start
|              |      | 02h: POST end
</details>

<details>
  <summary>Cmd: 0xC0 SET_SMI_STATUS</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Timeout(Default 10 seconds)

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
</details>

<details>
  <summary>Cmd: 0xC1 GET_SMI_STATUS</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | -    | -

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
|              | 2    | Status code
|              |      | 0   No error, ready for next command
|              |      | 1   receiving user data
|              |      | 2   SMI triggered
|              |      | 3   BIOS getting data from BMC
|              |      | 4   BIOS processing the request
|              |      | 5   BIOS sending data to BMC
|              |      | 6   User request done, data is ready
|              |      | 7   BMC sending data to user
|              |      | 8   BIOS Timeout
|              |      | 9   Error happen, can't finish the request"
|              |      | 3   Timeout in second
|              |      | 4:7	SMI trigger time - time_t format
|              |      | 8   Function ID - return 0xFF for invalid
|              |      | 9   Error code - return 0xFF for invalid
</details>

<details>
  <summary>Cmd: 0xC2 SET_SMI_USER</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1:2  | Size – total size of data
|              | 3:4  | Offset – data offset to send to BMC
|              | 5:N  | Data – various size data

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
</details>

<details>
  <summary>Cmd: 0xC3 GET_SMI_USER</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1:2  | Size – Allocated buffer size
|              | 3:4  | Offset – data offset to get from BMC

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
|              | 2:3  | Size – total data size to be returned
|              | 4:N  | Data – various size data
</details>

<details>
  <summary>Cmd: 0xC4 SET_SMI_BIOS</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1:2  | Size – total size of data
|              | 3:4  | Offset – data offset to send
|              | 5:N  | Data – various size data

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
</details>

<details>
  <summary>Cmd: 0xC5 GET_SMI_BIOS</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1:2  | Size – Allocated buffer size
|              | 3:4  | Offset – data offset to get

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
|              | 2:3  | Size – total size of data to return
|              | 4:N  | Data – various size data
</details>

<details>
  <summary>Cmd: 0xC8 SET_FRU_DATA</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | FRU ID
|              | 2    | FRU Area
|              |      | 00h: Internal Use Area (Reserved)
|              |      | 01h: Chassis Info Area
|              |      | 02h: Board Info Area
|              |      | 03h: Product Info Area
|              |      | 04h: MultiRecord Area (Reserved)
|              | 3    | Entry
|              |      | For byte 2 = 01h:
|              |      | 00h: Chassis Type - 01h: Chassis Part Number - 02h: Chassis Serial Number
|              |      | 
|              |      | For byte 2 = 02h:
|              |      | 01h: Mfg. Date / Time - 02h: Board Manufacturer - 03h: Board Product Name
|              |      | 04h: Board Serial Number - 05h: Board Part Number - 06h: FRU File ID
|              |      | 07h: Extra 0 - 08h: Extra 1 -  09h: Extra 2 - 0Ah: Extra 3 
|              |      | 0Bh: Extra 4 - 0Ch: Extra 5 - 0Dh: Extra 6
|              |      | 0Eh: Extra 7
|              |      | 
|              |      | For byte 2 = 03h:
|              |      | 01h: Manufacturer Name - 02h: Product Name - 03h: Product Part/Model Number
|              |      | 04h: Product Version - 05h: Product Serial Number - 06h: Asset Tag
|              |      | 07h: FRU File ID - 08h: Extra 0 - 09h: Extra 1
|              |      | 0Ah: Extra 2 - 0Bh: Extra 3 - 0Ch: Extra 4
|              |      | 0Dh: Extra 5 - 0Eh: Extra 6 - 0Fh: Extra 7
|              | 4    | Type
|              |      | [7:6]: type code
|              |      | [5:0]: Reserved
|              | 5:N  | Data

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
|              | 2:3  | Size of the new FRU structure(LSB Frist)
</details>

<details>
  <summary>Cmd: 0xC9 GET_FRU_DATA</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | FRU ID
|              | 2    | FRU Area
|              |      | 00h: Internal Use Area (Reserved)
|              |      | 01h: Chassis Info Area
|              |      | 02h: Board Info Area
|              |      | 03h: Product Info Area
|              |      | 04h: MultiRecord Area (Reserved)
|              | 3    | Entry
|              |      | For byte 2 = 01h:
|              |      | 00h: Chassis Type - 01h: Chassis Part Number - 02h: Chassis Serial Number
|              |      | 
|              |      | For byte 2 = 02h:
|              |      | 01h: Mfg. Date / Time - 02h: Board Manufacturer - 03h: Board Product Name
|              |      | 04h: Board Serial Number - 05h: Board Part Number - 06h: FRU File ID
|              |      | 07h: Extra 0 - 08h: Extra 1 -  09h: Extra 2 - 0Ah: Extra 3 
|              |      | 0Bh: Extra 4 - 0Ch: Extra 5 - 0Dh: Extra 6
|              |      | 0Eh: Extra 7
|              |      | 
|              |      | For byte 2 = 03h:
|              |      | 01h: Manufacturer Name - 02h: Product Name - 03h: Product Part/Model Number
|              |      | 04h: Product Version - 05h: Product Serial Number - 06h: Asset Tag
|              |      | 07h: FRU File ID - 08h: Extra 0 - 09h: Extra 1
|              |      | 0Ah: Extra 2 - 0Bh: Extra 3 - 0Ch: Extra 4
|              |      | 0Dh: Extra 5 - 0Eh: Extra 6 - 0Fh: Extra 7

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
|              | 2    | Type/Length
|              |      | [7:6]: Type
|              |      | [5:0]: Length
|              | 3:N  | Data
</details>

<details>
  <summary>Cmd: 0xCA FILE_OPERATOR</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Operation
|              |      | 0: Get file info
|              |      | 1: Delete file
|              | 2:N  | File path (max string length 255 bytes)

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
|              |      | 0: Normal
|              |      | 1: File does not exist
|              | 2:9  | File size (LSB first) for Operation = 0
|              | 10:13| CRC32 checksum (LSB first) for Operation = 0
</details>

<details>
  <summary>Cmd: 0xCB FILE_DOWNLOAD</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1:3  | Sequence number of the file
|              | 4:N  | File path (max string length 255 bytes)

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
|              |      | 0: Normal
|              |      | 1: File does not exist
|              |      | 2: Invalid sequence number
|              | 2:4  | Sequence number(LSB first)
|              | 5    | Checksum
|              | 6:37 | File Data(MSB First) 32 bytes
|              |      | Note: The last sequence number may not be 32 byte
</details>

<details>
  <summary>Cmd: 0xCC FILE_UPLOAD</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Parameter select
|              |      | 0: File path
|              |      | 1: File Upload
|              |      | 2: End of request
|              |      | 3: Drop this upload
|              | 2:N  | Configuration parameter data

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
|              |      | 00h = Normal
|              |      | 01h = The file does not exist
|              |      | 03h = Checksum error
|              |      | 04h = Invalid request
|              |      | 05h = other file upload in progress"
|              | 2:4  | Sequence number(LSB first)
|              | 5    | Checksum
|              | 6:37 | File Data(MSB First) 32 bytes
|              |      | Note: The last sequence number may not be 32 byte

| Parameter        | # | byte | data field                               |
| ---------        | - | ---- | ---------------------------------------- |
| File path        | 0 | 1:N  | File path
| File upload      | 1 | 1:3  | Sequence number
|                  |   | 4    | Checksum
|                  |   | 5:36 | File Data (MSB first)
|                  |   |      | Note: The last sequence number may not be 32 byte
| End of request   | 2 | -    | -
| Drop this upload | 3 | -    | -
</details>

<details>
  <summary>Cmd: 0xCD EXECUTE_SHELL_COMMAND</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1:N  | Command select
|              |      | Ex: /etc/init.d/webgo.sh restart

| Response Data| byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Completion Code
|              |      | 00h = Normal
</details>

<details>
  <summary>Cmd: 0xCE GET_OC_PROFILE_SELECTION</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | -    | Get OC Profile info (request length = 0)
|              | 1    | Activate OC Profile # (request length = 1)

| Response Data    | byte | data field                               |
| ---------------- | ---- | ---------------------------------------- |
| Request length=0 | 1    | Completion Code
|                  | 2    | Number of profiles
|                  | 3    | Active profile (0 base)
|                  | 4    | Reserved
| Request length=1 | 1    | Completion Code
|                  | 2:N  | OC Profile name (max string length 32 bytes + zero end)
</details>

<details>
  <summary>Cmd: 0xCF SET_OC_PROFILE_SELECTION</summary>

| Request Data | byte | data field                               |
| ------------ | ---- | ---------------------------------------- |
|              | 1    | Number of OC Profiles
|              | 2    | Activate OC Profile #
|              | 3    | Reserved

| Response Data | byte | data field                               |
| ------------- | ---- | ---------------------------------------- |
|               | 1    | Completion Code
</details>

<details>
  <summary>Cmd: 0xD0 SET_FAN_OPEN_LOOP_CONTROL_TABLE</summary>

| Request Data | byte   | data field                               |
| ------------ | ----   | ---------------------------------------- |
|              | 1      | Fan table number. (Maximum is 8)
|              | 2      | Select table.
|              |        | 00h = Temperature table
|              |        | 01h = Duty cycle table
|              | 3:(26) | For temperature table setting, the valid value from 00h to 78h. (00 to 120 degree C)
|              |        | For duty cycle table setting, the valid value from 14h to 64h. (20% to 100%)
|              |        | The settings must from low to high.
|              |        | Enter 0xFF means end of table. Can’t set 0xFF for byte 3.
|              |        | Note: Please set the “Temperature table” before setting “Duty cycle table”.

| Response Data | byte | data field                               |
| ------------- | ---- | ---------------------------------------- |
|               | 1    | Completion Code
</details>

<details>
  <summary>Cmd: 0xD1 GET_FAN_OPEN_LOOP_CONTROL_TABLE</summary>

| Request Data | byte   | data field                               |
| ------------ | ----   | ---------------------------------------- |
|              | 1      | Fan table number. (Maximum is 8)
|              |        | Bit 7  Default or Customized FAN Table Selection
|              |        |   0 = Customized
|              |        |   1 = Default
|              |        | Bit 6:0  Fan table number
|              | 2      | Select table.
|              |        | 00h = Temperature table
|              |        | 01h = Duty cycle table

| Response Data | byte | data field                               |
| ------------- | ---- | ---------------------------------------- |
|               | 1    | Completion Code
|               | 2:25 | The table of temperature or duty cycle
</details>

<details>
  <summary>Cmd: 0xD2 SET_FAN_CLOSED_LOOP_CONTROL_TABLE</summary>

| Request Data | byte   | data field                               |
| ------------ | ----   | ---------------------------------------- |
|              | 1      | Fan table number. (Maximum is 10)
|              | 2      | The temperature of slow down fan duty cycle
|              | 3      | The duty cycle percentage of slow down fan duty cycle
|              | 4      | The time(seconds) of slow down fan duty cycle
|              | 5      | The temperature of speed up fan duty cycle
|              | 6      | The duty cycle percentage of speed up fan duty cycle
|              | 7      | The time(seconds) of speed up fan duty cycle

| Response Data | byte | data field                               |
| ------------- | ---- | ---------------------------------------- |
|               | 1    | Completion Code
</details>

<details>
  <summary>Cmd: 0xD3 GET_FAN_CLOSED_LOOP_CONTROL_TABLE</summary>

| Request Data | byte   | data field                               |
| ------------ | ----   | ---------------------------------------- |
|              | 1      | Fan table number. (Maximum is 10)
|              |        | Bit 7  Default or Customized FAN Table Selection
|              |        |   0 = Customized
|              |        |   1 = Default
|              |        | Bit 6:0  Fan table numberThe temperature of slow down fan duty cycle

| Response Data | byte | data field                               |
| ------------- | ---- | ---------------------------------------- |
|               | 1    | Completion Code
|               | 2    | The temperature of slow down fan duty cycle
|               | 3    | The duty cycle percentage of slow down fan duty cycle
|               | 4    | The time(seconds) of slow down fan duty cycle
|               | 5    | The temperature of speed up fan duty cycle
|               | 6    | The duty cycle percentage of speed up fan duty cycle
|               | 7    | The time(seconds) of speed up fan duty cycle
</details>

<details>
  <summary>Cmd: 0xD4 SET_TEMPERATURE_SENSOR_AND_CORRESPONDING_FAN_TABLE_NUMBER</summary>

| Request Data | byte   | data field                               |
| ------------ | ----   | ---------------------------------------- |
|              | 1      | Temperature sensor number
|              |        | FFh = Select all temperature sensor
|              |        | Note: Byte1 is 0xFF and Byte2~5 are 0x00 means delete all temperature sensor.
|              | 2      | Open loop table number
|              |        | 00h: Disable
|              |        | 01h ~ 08h: Fan table maximum is 8.
|              | 3      | Close loop table number
|              |        | 00h: Disable
|              |        | 01h ~ 0Ah: Fan table maximum is 10.
|              | 4      | Select Fan 1~8 (can be multiple bits)
|              |        | 0b = FAN1
|              |        | 1b = FAN2
|              |        | 2b = FAN3
|              |        | 3b = FAN4
|              |        | 4b = FAN5
|              |        | 5b = FAN6
|              |        | 6b = FAN7
|              |        | 7b = FAN8
|              | 5      | Select Fan 9~16 (can be multiple bits)
|              |        | 0b = FAN9
|              |        | 1b = FAN10
|              |        | 2b = FAN11
|              |        | 3b = FAN12
|              |        | 4b = FAN13
|              |        | 5b = FAN14
|              |        | 6b = FAN15
|              |        | 7b = FAN16

| Response Data | byte | data field                               |
| ------------- | ---- | ---------------------------------------- |
|               | 1    | Completion Code
</details>

<details>
  <summary>Cmd: 0xD5 GET_TEMPERATURE_SENSOR_AND_CORRESPONDING_FAN_TABLE_NUMBER</summary>

| Request Data | byte   | data field                               |
| ------------ | ----   | ---------------------------------------- |
|              | 1      | Temperature sensor number
|              |        | Bit 7  Default or Customized FAN Table Selection
|              |        |   0 = Customized
|              |        |   1 = Default
|              |        | Bit 6:0  Fan table number
|              |        | FFh = reserve

| Response Data | byte | data field                               |
| ------------- | ---- | ---------------------------------------- |
|               | 1    | Completion Code
|               | 2    | Open loop table number
|               |      | 00h: Disable
|               |      | 01h ~ 08h: Fan table maximum is 8.
|               | 3    | Close loop table number
|               |      | 00h: Disable
|               |      | 01h ~ 0Ah: Fan table maximum is 10.
|               | 4    | Select Fan 1~8 (can be multiple bits)
|               |      | 0b = FAN1
|               |      | 1b = FAN2
|               |      | 2b = FAN3
|               |      | 3b = FAN4
|               |      | 4b = FAN5
|               |      | 5b = FAN6
|               |      | 6b = FAN7
|               |      | 7b = FAN8
|               | 5    | Select Fan 9~16 (can be multiple bits)
|               |      | 0b = FAN9
|               |      | 1b = FAN10
|               |      | 2b = FAN11
|               |      | 3b = FAN12
|               |      | 4b = FAN13
|               |      | 5b = FAN14
|               |      | 6b = FAN15
|               |      | 7b = FAN16

</details>

<details>
  <summary>Cmd: 0xD6 SET_FAN_DUTY_FOR_MANUAL_MODE</summary>

| Request Data | byte   | data field                               |
| ------------ | ----   | ---------------------------------------- |
|              | 1      | FAN1 duty for manual mode
|              |        | The valid value from 14h to 64h. (20% to 100%)
|              | 2      | FAN2 duty for manual mode
|              | 3      | FAN3 duty for manual mode
|              | 4      | FAN4 duty for manual mode
|              | 5      | FAN5 duty for manual mode
|              | 6      | FAN6 duty for manual mode
|              | 7      | FAN7 duty for manual mode
|              | 8      | FAN8 duty for manual mode
|              | 9      | FAN9 duty for manual mode
|              | 10     | FAN10 duty for manual mode
|              | 11     | FAN11 duty for manual mode
|              | 12     | FAN12 duty for manual mode
|              | 13     | FAN13 duty for manual mode
|              | 14     | FAN14 duty for manual mode
|              | 15     | FAN15 duty for manual mode
|              | 16     | FAN16 duty for manual mode

| Response Data | byte | data field                               |
| ------------- | ---- | ---------------------------------------- |
|               | 1    | Completion Code
</details>

<details>
  <summary>Cmd: 0xD7 GET_FAN_DUTY_FOR_MANUAL_MODE</summary>

| Request Data | byte   | data field                               |
| ------------ | ----   | ---------------------------------------- |
|              | -      | -

| Response Data | byte | data field                               |
| ------------- | ---- | ---------------------------------------- |
|               | 1    | Completion Code
|               | 2    | FAN1 duty for manual mode
|               |      | The valid value from 14h to 64h. (20% to 100%)
|               | 3    | FAN2 duty for manual mode
|               | 4    | FAN3 duty for manual mode
|               | 5    | FAN4 duty for manual mode
|               | 6    | FAN5 duty for manual mode
|               | 7    | FAN6 duty for manual mode
|               | 8    | FAN7 duty for manual mode
|               | 9    | FAN8 duty for manual mode
|               | 10   | FAN9 duty for manual mode
|               | 11   | FAN10 duty for manual mode
|               | 12   | FAN11 duty for manual mode
|               | 13   | FAN12 duty for manual mode
|               | 14   | FAN13 duty for manual mode
|               | 15   | FAN14 duty for manual mode
|               | 16   | FAN15 duty for manual mode
|               | 17   | FAN16 duty for manual mode
</details>

<details>
  <summary>Cmd: 0xD8 SET_FAN_CONTROL_MODE</summary>

| Request Data | byte   | data field                               |
| ------------ | ----   | ---------------------------------------- |
|              | 1      | FAN1 fan control mode
|              |        | 00h = default fan control
|              |        | 01h = manual mode
|              |        | 02h = customize smart fan control mode
|              | 2      | FAN2 fan control mode
|              | 3      | FAN3 fan control mode
|              | 4      | FAN4 fan control mode
|              | 5      | FAN5 fan control mode
|              | 6      | FAN6 fan control mode
|              | 7      | FAN7 fan control mode
|              | 8      | FAN8 fan control mode
|              | 9      | FAN9 fan control mode
|              | 10     | FAN10 fan control mode
|              | 11     | FAN11 fan control mode
|              | 12     | FAN12 fan control mode
|              | 13     | FAN13 fan control mode
|              | 14     | FAN14 fan control mode
|              | 15     | FAN15 fan control mode
|              | 16     | FAN16 fan control mode

| Response Data | byte | data field                               |
| ------------- | ---- | ---------------------------------------- |
|               | 1    | Completion Code
</details>

<details>
  <summary>Cmd: 0xD9 GET_FAN_CONTROL_MODE</summary>

| Request Data | byte   | data field                               |
| ------------ | ----   | ---------------------------------------- |
|              | -      | -

| Response Data | byte | data field                               |
| ------------- | ---- | ---------------------------------------- |
|               | 1    | Completion Code
|               | 2    | FAN1 fan control mode
|               |      | 00h = default fan control
|               |      | 01h = manual mode
|               |      | 02h = customize smart fan control mode
|               | 3    | FAN2 fan control mode
|               | 4    | FAN3 fan control mode
|               | 5    | FAN4 fan control mode
|               | 6    | FAN5 fan control mode
|               | 7    | FAN6 fan control mode
|               | 8    | FAN7 fan control mode
|               | 9    | FAN8 fan control mode
|               | 10   | FAN9 fan control mode
|               | 11   | FAN10 fan control mode
|               | 12   | FAN11 fan control mode
|               | 13   | FAN12 fan control mode
|               | 14   | FAN13 fan control mode
|               | 15   | FAN14 fan control mode
|               | 16   | FAN15 fan control mode
|               | 17   | FAN16 fan control mode
</details>

<details>
  <summary>Cmd: 0xDA GET_CURRENT_FAN_DUTY</summary>

| Request Data | byte   | data field                               |
| ------------ | ----   | ---------------------------------------- |
|              | -      | -

| Response Data | byte | data field                               |
| ------------- | ---- | ---------------------------------------- |
|               | 1    | Completion Code
|               | 2    | FAN1 current fan duty
|               | 3    | FAN2 current fan duty
|               | 4    | FAN3 current fan duty
|               | 5    | FAN4 current fan duty
|               | 6    | FAN5 current fan duty
|               | 7    | FAN6 current fan duty
|               | 8    | FAN7 current fan duty
|               | 9    | FAN8 current fan duty
|               | 10   | FAN9 current fan duty
|               | 11   | FAN10 current fan duty
|               | 12   | FAN11 current fan duty
|               | 13   | FAN12 current fan duty
|               | 14   | FAN13 current fan duty
|               | 15   | FAN14 current fan duty
|               | 16   | FAN15 current fan duty
|               | 17   | FAN16 current fan duty
</details>

<details>
  <summary>Cmd: 0xDB GET_SUPPORT_FAN</summary>

| Request Data | byte   | data field                               |
| ------------ | ----   | ---------------------------------------- |
|              | -      | -

| Response Data | byte | data field                               |
| ------------- | ---- | ---------------------------------------- |
|               | 1    | Completion Code
|               | 2    | Supported status of Fan 1~8
|               |      | 0b = Supported status of FAN1
|               |      |  1: FAN1 is supported.
|               |      |  0: FAN1 is not supported.
|               |      | 1b = Supported status of FAN2
|               |      | 2b = Supported status of FAN3
|               |      | 3b = Supported status of FAN4
|               |      | 4b = Supported status of FAN5
|               |      | 5b = Supported status of FAN6
|               |      | 6b = Supported status of FAN7
|               |      | 7b = Supported status of FAN8
|               | 3    | Supported status of Fan 9~16
|               |      | 0b = Supported status of FAN9
|               |      | 1b = Supported status of FAN10
|               |      | 2b = Supported status of FAN11
|               |      | 3b = Supported status of FAN12
|               |      | 4b = Supported status of FAN13
|               |      | 5b = Supported status of FAN14
|               |      | 6b = Supported status of FAN15
|               |      | 7b = Supported status of FAN16
</details>

<details>
  <summary>Cmd: 0xDC CLEAN_ALL_FAN_SETTINGS</summary>

| Request Data | byte   | data field                               |
| ------------ | ----   | ---------------------------------------- |
|              | -      | -

| Response Data | byte | data field                               |
| ------------- | ---- | ---------------------------------------- |
|               | 1    | Completion Code
</details>

<details>
  <summary>Cmd: 0xDE SET_POWER_CONTROL</summary>

| Request Data | byte   | data field                              |
| ------------ | ----   | --------------------------------------- |
|              | 1      | Power button control mode
|              |        | 00h: Disable
|              |        | 01h: Enable
|              | 2      | Reset button control mode
|              |        | 00h: Disable
|              |        | 01h: Enable

| Response Data | byte | data field                               |
| ------------- | ---- | ---------------------------------------- |
|               | 1    | Completion Code
</details>

<details>
  <summary>Cmd: 0xDF GET_POWER_CONTROL</summary>

| Request Data | byte   | data field                              |
| ------------ | ----   | --------------------------------------- |
|              | -      | -

| Response Data | byte | data field                               |
| ------------- | ---- | ---------------------------------------- |
|               | 1    | Completion Code
|               | 2    | Power button control mode
|               |      | 00h: Disable
|               |      | 01h: Enable
|               | 3    | Reset button control mode
|               |      | 00h: Disable
|               |      | 01h: Enable
</details>

<details>
  <summary>Cmd: 0xE0 CM and Node Commands</summary>

<details>
  <summary>SubCmd: 0x00 SET_NODE_ID</summary>

| Request Data | byte   | data field                               |
| ------------ | ----   | ---------------------------------------- |
|              | 1      | Node ID (1 based)

| Response Data | byte | data field                               |
| ------------- | ---- | ---------------------------------------- |
|               | 1    | Completion Code
</details>

<details>
  <summary>SubCmd: 0x01 GET_NODE_ID</summary>

| Request Data | byte   | data field                               |
| ------------ | ----   | ---------------------------------------- |
|              | -      | -

| Response Data | byte | data field                               |
| ------------- | ---- | ---------------------------------------- |
|               | 1    | Completion Code
|               | 2    | Node ID
|               |      | 0: Not set (unknown)
|               |      | others: Node ID
</details>
<details>
  <summary>SubCmd: 0x02 SET_NODE_DATA</summary>

| Request Data | byte   | data field                               |
| ------------ | ----   | ---------------------------------------- |
|              | 1      | Node ID
|              | 2:3    | Node data offset
|              | 4:N    | Data (Max 32 bytes)

| Response Data | byte | data field                               |
| ------------- | ---- | ---------------------------------------- |
|               | 1    | Completion Code
</details>
<details>
  <summary>SubCmd: 0x03 GET_NODE_DATA</summary>

| Request Data | byte   | data field                               |
| ------------ | ----   | ---------------------------------------- |
|              | 1      | Node ID
|              | 2:3    | Node data offset

| Response Data | byte | data field                               |
| ------------- | ---- | ---------------------------------------- |
|               | 1    | Completion Code
|               | 2:N  | Data (Max 32 bytes)
</details>
<details>
  <summary>SubCmd: 0x04 SET_CM_DATA</summary>

| Request Data | byte   | data field                               |
| ------------ | ----   | ---------------------------------------- |
|              | 1:2    | CM data offset
|              | 3:N    | Data (Max 32 bytes)

| Response Data | byte | data field                               |
| ------------- | ---- | ---------------------------------------- |
|               | 1    | Completion Code
</details>
<details>
  <summary>SubCmd: 0x05 GET_CM_DATA</summary>

| Request Data | byte   | data field                               |
| ------------ | ----   | ---------------------------------------- |
|              | 1:2    | CM data offset

| Response Data | byte | data field                               |
| ------------- | ---- | ---------------------------------------- |
|               | 1    | Completion Code
|               | 2:N  | Data (Max 32 bytes)
</details>
<details>
  <summary>SubCmd: 0x06 SET_RUNCM_REQ</summary>

User to Node command
| Request Data | byte   | data field                               |
| ------------ | ----   | ---------------------------------------- |
|              | 1      | Node ID
|              |        | 0: Run on CM
|              |        | 1..N: Run on Node
|              | 2      | NetFn
|              | 3      | Cmd
|              | 4:N    | Request data (Max 61 bytes)

| Response Data | byte | data field                               |
| ------------- | ---- | ---------------------------------------- |
|               | 1    | Completion Code
|               | 2    | Sequence ID (0 ~ 63)
</details>
<details>
  <summary>SubCmd: 0x07 GET_RUNCM_RES</summary>

User to Node command
| Request Data | byte   | data field                               |
| ------------ | ----   | ---------------------------------------- |
|              | 1      | Sequence ID (Assigned by subcmd 0x06)
|              | 2      | Action (Optional)
|              |        | 0: Get Result
|              |        | 1: Drop the command

| Response Data | byte | data field                               |
| ------------- | ---- | ---------------------------------------- |
|               | 1    | Completion Code
|               |      | 0x00: Success
|               |      | 0x64: Pending, command not finish
|               |      | Others: Error
|               | 2:N  | Data returned (If Completion Code = 0x00)
</details>
<details>
  <summary>SubCmd: 0x08 SET_RUNCM_RES</summary>

CM to Node command
| Request Data | byte   | data field                               |
| ------------ | ----   | ---------------------------------------- |
|              | 1      | Sequence ID (Returned by subcmd 0x09)
|              | 2:N    | Response data from CM

| Response Data | byte | data field                               |
| ------------- | ---- | ---------------------------------------- |
|               | 1    | Completion Code
</details>
<details>
  <summary>SubCmd: 0x09 GET_RUNCM_REQ</summary>

CM to Node command
| Request Data | byte   | data field                               |
| ------------ | ----   | ---------------------------------------- |
|              | -      | -

| Response Data | byte | data field                               |
| ------------- | ---- | ---------------------------------------- |
|               | 1    | Completion Code
|               | 2    | Sequence ID (Assigned by subcmd 0x06)
|               | 3    | Node ID
|               |      | 0: Run on CM
|               |      | 1..N: Run on Node
|               | 4    | NetFn
|               | 5    | Cmd
|               | 6:N  | Request data (Max 61 bytes)
</details>

</details>

<details>
  <summary>Cmd: 0xF0~0xFF Free command</summary>

| Request Data | byte   | data field                               |
| ------------ | ----   | ---------------------------------------- |
|              | -      | -

| Response Data | byte | data field                               |
| ------------- | ---- | ---------------------------------------- |
|               | -    | -
</details>
