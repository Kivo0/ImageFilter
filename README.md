<!--  gh-md-toc --insert README.md -->
<!--ts-->
   * [FPGA implementation of a image filtering](#fpga-implementation-of-a-image-filtering)
      * [Components](#components)
         * [Filter Bank](#filter-bank)
         * [filter bank chooser](#filter-bank-chooser)
         * [Multiplier (with adder)](#multiplier-with-adder)
         * [Efficient adder](#efficient-adder)
         * [Fifo_buffer_3](#fifo_buffer_3)
         * [Cache memory](#cache-memory)
         * [Zipper](#zipper)
         * [Controller](#controller)
         * [Enabler](#enabler)
      * [Directory stucture](#directory-stucture)

<!-- Added by: talos, at: 2019-01-06T02:56+01:00 -->

<!--te-->
# FPGA implementation of a image filtering
<p align="center">
  <img width="640" src="https://github.com/jtsagata/ImageFilter/blob/master/images/filter_top.png">
</p>
<p align="center">
  <img width="640" src="https://github.com/jtsagata/ImageFilter/blob/master/images/hierarchy.png">
</p>

## Components

### Filter Bank
<p align="center">
  <img width="640" src="https://github.com/jtsagata/ImageFilter/blob/master/images/filter_bank.png">
</p>


### filter bank chooser
<p align="center">
  <img width="640" src="https://github.com/jtsagata/ImageFilter/blob/master/images/filter_bank_chooser.png">
</p>


### Multiplier (with adder)
<p align="center">
  <img width="640" src="https://github.com/jtsagata/ImageFilter/blob/master/images/multiplier_adder.png">
</p>

### Efficient adder
<p align="center">
  <img width="640" src="https://github.com/jtsagata/ImageFilter/blob/master/images/adder.png">
</p>


### Fifo_buffer_3

<p align="center">
  <img width="640" src="https://github.com/jtsagata/ImageFilter/blob/master/images/fifo_buffer_3_sim.png">
</p>


<p align="center">
  <img width="640" src="https://github.com/jtsagata/ImageFilter/blob/master/images/fifo_buffer_3_schem.png">
</p>

### Cache memory
<p align="center">
  <img width="640" src="https://github.com/jtsagata/ImageFilter/blob/master/images/cache_mem.png">
</p>

### Zipper
Module zipper takes the filter output and trim it down to the range 0...255. 


<p align="center">
  <img width="640" src="https://github.com/jtsagata/ImageFilter/blob/master/images/zipper.png">
</p>


### Controller
This module provides control signals as shown in the picture
<p align="center">
  <img width="640" src="https://github.com/jtsagata/ImageFilter/blob/master/images/control_signals_test.png">
</p>
This is a complex module that do a lot of calculations
<p align="center">
  <img width="640" src="https://github.com/jtsagata/ImageFilter/blob/master/images/control_logic.png">
</p>

### Enabler
This module enable the controller after some time
<p align="center">
  <img width="640" src="https://github.com/jtsagata/ImageFilter/blob/master/images/enabler.png">
</p>

## Directory stucture

- src  
  Contains the VHDL sources

- wcfg  
  Contains ISIM configurations

- src/test  
  Contains the VHDL test benches

- src/sims  
  Contains the VHDL test benches results

