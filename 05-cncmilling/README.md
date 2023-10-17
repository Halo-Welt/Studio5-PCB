# CNCmilling


Hey guys, I am a student in Shanghai. On this weekend I made my own PCB board (including drawing schematic diagram, using machine to cut copper board and soldering).

Created by **LIU Xinyu**

Date: **2023/10/12**


# 1. Project design in EasyEDA

At the beginning of our project, we need to learn about [EasyEDA](https://pro.easyeda.com/editor) — a software to make PCB document.

![Generally, we need these components to build our PCB board.](./images/schematic1.jpg)

Generally, we need these components to build our PCB board.

![At the top of EasyEDA, you can see a line of icons, which are important and usually used in the making process (especially the five red icons).](./images/schematic2.jpg)

At the top of EasyEDA, you can see a line of icons, which are important and usually used in the making process (especially the five red icons).

![The first one named ‘Component’ is a repository of components. We can find almost everything in it, select by filter and click button ‘Place’ to put it on the schematic diagram.](./images/schematic3.jpg)

The first one named ‘Component’ is a repository of components. We can find almost everything in it, select by filter and click button ‘Place’ to put it on the schematic diagram.

![The second one named ‘Wire’ can be used to connect components.](./images/schematic4.jpg)

The second one named ‘Wire’ can be used to connect components.

![The third one named ‘Net Label’ makes it more convenient to designate each pin. Click key ‘Tab’ to get details setting.](./images/schematic5.jpg)

The third one named ‘Net Label’ makes it more convenient to designate each pin. Click key ‘Tab’ to get details setting.

![The fourth one named ‘VCC’ collects VCC pin and GND pin. Usually we just need to use it for the first time we build a new file. On this project, it is good enough to choose ‘+5V’ and ‘GND’.](./images/schematic6.jpg)

The fourth one named ‘VCC’ collects VCC pin and GND pin. Usually we just need to use it for the first time we build a new file. On this project, it is good enough to choose ‘+5V’ and ‘GND’.

![The fifth one named ‘Update/Convert Schematic to PCB’ is to make your PCB change together with schematic diagram. Don’t forget to use it when you change something, or you will find fault later.](./images/schematic7.jpg)

The fifth one named ‘Update/Convert Schematic to PCB’ is to make your PCB change together with schematic diagram. Don’t forget to use it when you change something, or you will find fault later.

**After everything is getting done, we can go to PCB page.**

![It is my PCB design. I tried to make it as small as possible. It is only 5.4cm long and 4.3cm wide.](./images/PCB1.jpg)

It is my PCB design. I tried to make it as small as possible. It is only 5.4cm long and 4.3cm wide.

![You need to put these components on the suitable position and then use wires to connect them (blue line means there should be a wire but not yet).](./images/PCB2.jpg)

You need to put these components on the suitable position and then use wires to connect them (blue line means there should be a wire but not yet).

![Find button ‘Design’ and click ‘Design Rule’, that is important.](./images/PCB3.jpg)

Find button ‘Design’ and click ‘Design Rule’, that is important.

![Change all values to 0.4mm because diameter of our CNC milling knife are 1/64 inch (about 0.4mm) and 1/32 inch (about 0.8mm).](./images/PCB4.jpg)

Change all values to 0.4mm because diameter of our CNC milling knife are 1/64 inch (about 0.4mm) and 1/32 inch (about 0.8mm).

![Find button ‘Export’ and click ‘PDF/Image’. We will use it later to make files for cutting machine.](./images/PCB5.jpg)

Find button ‘Export’ and click ‘PDF/Image’. We will use it later to make files for cutting machine.

![Select ‘A Single Page PDF’, ‘White on Black’. 
Turn off ‘Bottom Layer’, ‘Top Silkscreen Layer’ and ‘Bottom Silkscreen Layer’.
Turn on ‘Board Outline Layer’.](./images/PCB6.jpg)

Select ‘A Single Page PDF’, ‘White on Black’. 
Turn off ‘Bottom Layer’, ‘Top Silkscreen Layer’ and ‘Bottom Silkscreen Layer’.
Turn on ‘Board Outline Layer’.

Then you will get a PDF-format file like this.

![Just refine this image in Adobe AI to obtain three PNG image: Trace, Hole and Outline.
One very significant thing: you must ensure that the sizes of these three images are the same.](./images/PCB7.jpg)

Just refine this image in Adobe AI to obtain three PNG image: Trace, Hole and Outline.
One very significant thing: you must ensure that the sizes of these three images are the same.

![Trace. ](./images/trace.png)

Trace. 

![Hole.](./images/hole.png)

Hole.

![Outline.](./images/outline.png)

Outline.

The first step is finished now. We have prepared necessary files.

# 2. Make files for cutting machine

Next part we will move to [another website](https://modsproject.org/) to make new files that can be read by machine based on the files we made right now.

You should do it in order: right click -> programs -> open program -> find ‘Roland SRM-20 mill PCB’. 

![In my college we use this machine, you should find the machine you will use.](./images/roland.png)

In my college we use this machine, you should find the machine you will use.

![Don’t be confused with such complicated page. We will just use five function and they are very easy.](./images/cut1.jpg)

Don’t be confused with such complicated page. We will just use five function and they are very easy.

![First, import file.](./images/cut2.jpg)

First, import file.

![Second, select different knife. We use 1/64 knife to mill traces and use 1/32 knife to mill holes and outline.](./images/cut3.jpg)

Second, select different knife. We use 1/64 knife to mill traces and use 1/32 knife to mill holes and outline.

![Third, change cut depth and max depth to 0.15mm.](./images/cut4.jpg)

Third, change cut depth and max depth to 0.15mm.

![Fourth, change origin value of x, y, z to 0mm.](./images/cut5.jpg)

Fourth, change origin value of x, y, z to 0mm.

![At last, turn off the top button and turn on the bottom button.](./images/cut6.jpg)

At last, turn off the top button and turn on the bottom button.

![Back to mill raster 2D section and click calculate, a few seconds later you will get a rml-format file and it will come a page automatically for you to check it.](./images/cut7.jpg)

Back to mill raster 2D section and click calculate, a few seconds later you will get a rml-format file and it will come a page automatically for you to check it.

# 3. Cut a copper board

With curiosity we can finally take a look of our magic machine.

![It is said to be particularly expensive.](./images/cutting_machine1.jpg)

It is said to be particularly expensive.

![This copper board seems a litter dirty but it doesn’t matter, we can clean it after cutting.](./images/cutting_machine2.jpg)

This copper board seems a litter dirty but it doesn’t matter, we can clean it after cutting.

![Let’s see how it works!](./images/process.gif)

Let’s see how it works!

![We can use this iron cloth to clean our PCB boards. It is really useful.](./images/iron_cloth.jpg)

We can use this iron cloth to clean our PCB boards. It is really useful.

# 4. Solder components on PCB board

For soldering, my teacher give us some devices and materials. I promise soldering is more interesting than PCB design, haha.

![Soldering iron. There are three types of this tool, as the image showed is the most suitable type for beginners. We should set temperature around 300 to 400 °C.](./images/iron1.jpg)

Soldering iron. There are three types of this tool, as the image showed is the most suitable type for beginners. We should set temperature around 300 to 400 °C.

![Attention! The soldering iron can only be either on its stand or in your hand; otherwise, it can be dangerous.](./images/iron2.jpg)

Attention! The soldering iron can only be either on its stand or in your hand; otherwise, it can be dangerous.

![Material tin (Element Sn).](./images/tin.jpg)

Material tin (Element Sn).

![Tweezer.](./images/tweezer.jpg)

Tweezer.

![Write the component list in order to find them.](./images/material.jpg)

Write the component list in order to find them.

![board1.jpg](./images/board1.jpg)

![My PCB board!!](./images/board2.jpg)

My PCB board!!

![It is quite successful, I love it.](./images/outcome.jpg)

It is quite successful, I love it.

# 5. Summary

This week we learned how to make a real PCB board. In fact I met two problems. One was that I forgot to set ‘hole’ image as big as ‘trace’ image so the machine destroyed my board. Fortunately my teacher taught me how to save it by using metal to connect the destroyed wire. Another problem was that I was not patient enough to solder, so tin was not combine with pins well. I hope you can pay attention to these two aspects and don’t make same mistake.

See you next week!
