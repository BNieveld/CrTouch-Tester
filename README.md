# BLTouch/CRTouch -Tester
Simple Arduino code to test a BTTouch 3D printer sensor.

After a lot of frustration trying to get a BLTouch and a clone (3DTouch, CrTouch) device working, I decided it would be useful to have a simple circuit to test the device to be sure it was a problem with the printer and not the device.

This code is based on a simple Arduino program running on an Arduino ProMini but would be easily transportable to the Uno or any othe flavour.

The hardware for this system is hooked up as follows :

<TABLE>
  <TH>BLTouch</TH>
  <TR>
    <TH>Arduino PIN</TH><TH>Use</TH>
  </TR>
  <TR>
    <TD>2</TD><TD>White (Sensor output)</TD>
  </TR>
  <TR>
    <TD>9</TD><TD>Orange (Signal)</TD>
  </TR>
  <TR>
    <TD>5V</TD><TD>Red</TD>
  </TR>
  <TR>
    <TD>Gnd/0V</TD><TD>Brown</TD>
  </TR>
</TABLE>

<TABLE>
  <TH>CrTouch</TH>
  <TR>
    <TH>Arduino PIN</TH><TH>Use CRTouch (wire from left to right)</TH>
  </TR>
  <TR>
    <TD>2</TD><TD>Blue (Sensor output)</TD>
  </TR>
  <TR>
    <TD>Gnd</TD><TD>Red</TD>
  </TR>
  <TR>
    <TD>9</TD><TD>Yellow (Signal)</TD>
  </TR>
  <TR>
    <TD>5V</TD><TD>Black</TD>
  </TR>
  <TR>
    <TD>Gnd</TD><TD>White</TD>
  </TR>
</TABLE>

<P>
Once that is all hooked up and code installed, when powered up the BLTouch should do the twice pin down and up self diagnostics.

Open serial monitor and send the following to test.
</P>
<TABLE>
  <TR>
    <TH>Character Sent</TH><TH>Action</TH>
  </TR>
  <TR>
    <TD>1</TD><TD>Pin Down</TD>
  </TR>
  <TR>
    <TD>2</TD><TD>Pin Up</TD>
  </TR>
  <TR>
    <TD>3</TD><TD>Self Test</TD>
  </TR>
  <TR>
    <TD>4</TD><TD>Touch SW Mode (M119)</TD>
  </TR>
  <TR>
    <TD>5</TD><TD>Alarm Release & Reset</TD>
  </TR>
</TABLE>
