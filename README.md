The EmbededLocoNet Library provides functions that manage the
sending and receiving of LocoNet packets.

As bytes are received from the LocoNet by an interrupt driven
handler, they are stored in a circular buffer and after a valid
packet has been received it can be read out.

When packets are sent successfully, they are also appended to the
Receive circular buffer so they can be handled in the same manner
as if they had been received from another device.

Statistics are maintained for both the transmission and reception
of packets.  Any invalid packets that are received are discarded
and the stats are updated approproately.

This library uses TIMER1 & ICP (UNO) and/or TIMER5 and ICP5 (MEGA)
resources and associated interrupt handler hooks.

Currently the library only supports the AVR mega and tiny range that
have an Input Capture Unit (ICP) associated with a 16-Bit Timer/Counter.

It's known to work with:
- UNO (ATmega328)
- MEGA (ATmega2560)
- Leonardo, LeoStick, Arduino Pro Micro (ATmega32U4)
- Various AVRTiny Boards (ATTiny84, ATTiny84A, ATTiny841)

**IMPORTANT**

Some of the message formats used in this code are Copyright Digitrax,
Inc.  and/or Elektronik GmbH and are used with permission as part
of the MRRwA project.  That permission does not extend to uses in
other software products.  See the LICENSE file for more information.


