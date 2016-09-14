# lab2
Milling your first printed circuit board.

In lecture, you learned about the theory and history of printed circuit boards.
In this lab, you will mill a PCB using the [Othermill](http://othermachine.co/),
a desktop CNC machine by selecting removing copper from the surface of a piece
of double-sided copper-plated FR-1 (Flame Retardant-1).

In contrast, most commercial PCBs are made with a chemical process which
deposits copper onto the substrate, then selectively etches away all the parts
not needed to result in traces and other connections. This is followed by other
similar chemical etching steps to add soldermask (e.g. the green finish commonly
seen on commercial PCBs) and silkscreen (text).

The disadvantages of doing this
include long turnaround time and higher cost compared to desktop milling, which
allows for cheaper, more rapid prototyping with the caveat of being less precise
(e.g. the minimum feature sizes are larger).

![Bottom side of the PCB](/images/pcb_bottom.jpg?raw=true)

![Top side of the PCB](/images/pcb_top.jpg?raw=true)

## Prerequisites and Materials

* [Jacobs Hall Othermill Training](https://bcourses.berkeley.edu/courses/1353091/pages/othermill-module)
* Othermill
 * Large and small wrench (should come with the Othermill)
 * USB and power cables (should come with the Othermill)
 * Bracket (see below for what this is) with securing screws (x3) and allen key
 * Large and small wrench set.for changing bits
* 1/32" Flat End Mill and 30° Engraving Bit
* A piece of double-sided copper-plated FR-1 PCB substrate
* Double-sided tape
* Small brush
* Digital calipers
* (optional) Spatula or other tool to remove the PCB once it has been milled

## Pre-lab

The only pre-lab for this (in addition to procuring the above trainings and
materials) is to install and set up the [Otherplan](https://othermachine.co/otherplan/)
software for operating the Othermill.

Overall, it is a quite user-friendly piece of software, as it comes with
built-in guides and instructions to help you with the milling procedure,
including when to change tools, etc.
Try to become best friends with it! :smiley:

## Procedure

This procedure should take about **1-2 hours** total to complete.

1. Start Otherplan.

2. Open the [board file](/hello-world.brd?raw=true) with **Plans → Open Files… → hello-world.brd**.

3. Set the milling tools to 1/32" Flat End Mill and 30° Engraving Bit.

4. (If necessary) Detach the window.

   <!---
   TODO: add picture of window?
   -->

5. (If necessary) Move Start Homing... → Move → Loading to bring the bed over so you can install the bracket.

  > **Note**: The Othermill bed is not hand-movable and attempting to force it without power
  > may permanently damage the machine.

6. Make sure the bracket is in place. Use the given screws and allen key to
  install the bracket onto the bed, if it is not already installed.

  ![Bracket](/images/bracket.jpg?raw=true)
  *The bracket and the screws and allen key required to install the bracket.*

7. Set the fixturing to bracket, if it is not already, using
  **Fixturing → Locate...**.

  Follow the on-screen instructions. When directed, follow the
  Othermachine-provided diagram to insert bit backwards.

  > **Note**: the machine will move automatically to find the fixture. Don't
  > disturb it while this happens.

  > **Note**: watch the machine at all times while it operates.

  <!---
  TODO: add othermachine diagram for bit change?
  -->
  
  ![Tool holder assembly](/images/tool_holder.jpg?raw=true)
  
  *The tool holder assembly (including a bit inserted backwards for fixturing.*

8. Get a blank double-sided FR-1 board.

9. Zero the calipers.

10. Measure board with calipers (this is typically ~1.6mm).

11. Set size of z to board depth using **Size → Thickness (Z)**.

  > **Note**: If the board has non-uniform thickness, use thinnest for most
  > aggressive cut to clear traces, which will overcut on some parts of the
  > board in order to ensure that copper gets cleared out and won't short.

12. Measure the tape thickness with the calipers (this is typically ~0.2mm).

  > **Note**: It is better to overestimate slightly so it won't gum up your tool
  > by trying to cutting tape if you underestimated the tape thickness.

13. Set the placement Z to tape depth: **Placement: Z**

14. Tape one side of board.
  If you put too much tape, the board will be **very**
  difficult to remove when the milling is done, but if you put too little tape
  A recommended amount is typically a few strips, or using four squares in the
  corners will work for small boards.

15. Attach board to bottom left side of bracket.

16. Set "parts to mill" to **top**.

17. Set the things to mill to **traces** and **holes**. Be sure to deselect
outline.

18. Start milling (under **Milling Tools** section).
  Change the tooling when asked. Follow the on-screen directions of the
  Otherplan software.

  ![Milling away](/images/milling.jpg?raw=true)
  *The Othermill at work, milling your board.*

19. (If necessary) Attach the window.

  > **Note**: The machine will stop as a safety feature if you open the window
  > while it is milling.

20. (If necessary) Detach the window.

21. Bring the bed over using **Start Homing... → Move → Loading** in preparation
for removing the piece.

22. Detach the board from the bed with the spatula.

23. Remove the tape from the board.

24. Clean the mounting surface with a brush.

25. Tape on top side of board (the side which has cuts on it).

26. Flip board horizontally and mount it on bottom right corner.

27. Set the "parts to mill" to **bottom**.

28. Set the things to mill to **traces**, **holes** AND **outline**.

  > **Note**: This is different from last time. We actually want to cut the
  > outline this time.

29. Start milling (under **Milling Tools** section).
  As before, change the tooling when asked. Follow the on-screen directions of
  the Otherplan software.

30. Detach the board from the bed with the spatula, being careful not to damage
  the other side.

31. Clean up the mill and workspace.

## Checkoff

**Objective**: A shiny, milled PCB!

1. Show us the milled printed circuit board on FR-1 substrate, with both sides
   milled and fabricated correctly, with no defects to the eye (e.g. peeled
   copper, missing traces, etc).

   You will be soldering to assemble the board next week, including connecting
   both sides of vias.
2. (optional) Perform a conductivity test using a multimeter on connected pins
   in a net to ensure that all required connectivity for the board is present.
   Otherwise your board may fail mysteriously after soldering and it may be hard
   to diagnose the issues.
