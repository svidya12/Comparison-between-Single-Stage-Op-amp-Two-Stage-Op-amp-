# Comparison-between-Single-Stage-Op-amp-Two-Stage-Op-amp-
# Abstract
Here in this project, we have desgined the single stage op-amp and two stage op-amp at 28nm technology with desgin specifications using Synopsis tool. We compared the gain and phase margin of two different stages of op-amp, and concludes that maximum gain is acheiveable in two stage op-amp rather than single stage op-amp without effecting the output swing and other parameters,
# Introduction
Op-amp stands for Operational amplifier as it performs mathematical operations of addition, subtraction, integration, differentiation etc. Basically, Op-amp is an integrated circuit which amplifies the differences in input voltage and produces single output.
# Drawbacks of Single Stage Op-amp
With a single stage, there’s a limit to the maximum voltage gain that can be derived and distortion will be high by modern standards. In order to increase the gain, we need to change the aspect ratios or we need to increase Rout, but it effects in Output swing and increases delay too.
# Two Stage op-amp
By using Two Stage op-amp, we increase the gain without effecting the output swing.
## Design methodology
Two stage operational amplifiers provide high gain and high
output swing. For low frequency applications the gain is one
of the most critical parameter. Overall gain is given by
AV=AV1*AV2 Where
AV=gain of op amp
AV1 (gain of 1st stage op amp) =gm1 (rds2|| rds4)
AV2 (gain of 2nd stage op amp) =gm7 (rds6|| rds7)
Maximum Output swing = VDD − |VOD5|
Minimum Output swing = |VOD6|
# Design Specification
###### Table 1.1 Design Specification of single stage and two stage op-amp
![image1](https://user-images.githubusercontent.com/70511616/155881958-9835c3b0-a8ac-4dc8-a2fc-5af3f32d5214.png)
# Schematic Diagram
![image](https://user-images.githubusercontent.com/70511616/155882200-589cee0a-a37f-478f-ac4f-fd80af56e446.png)
###### Fig 1.1 Schematic Diagram of One Stage Op-amp
![image](https://user-images.githubusercontent.com/70511616/155882408-33afe77f-f641-43df-8ab6-a4114c151521.png)
###### Fig 1.2 Schematic Diagram of Two Stage Op-amp
# Netlist of the circuit
## Single Stage Op-amp
*  Generated for: PrimeSim
*  Design library name: analog_ic_design
*  Design cell name: op-amp_stages
*  Design view name: schematic


*Custom Compiler Version S-2021.09
*Sun Feb 27 12:35:29 2022

.global gnd!
********************************************************************************
* Library          : analog_ic_design
* Cell             : op-amp_stages
* View             : schematic
* View Search List : hspice hspiceD schematic spice veriloga
* View Stop List   : hspice hspiceD
********************************************************************************
i0 net46 net30 dc=50u
c1 output gnd! c=10p
m3 output net13 net46 net46 pmos4 w=84u l=1u
m4 net17 net13 net46 net46 pmos4 w=84u l=1u
m8 net30 net29 gnd! gnd! nmos4 w=9u l=1u
m7 net25 net29 gnd! gnd! nmos4 w=9u l=1u
m6 output neg_input net25 gnd! nmos4 w=7u l=1u
m5 net17 pos_input net25 gnd! nmos4 w=7u l=1u
v19 pos_input gnd! dc=1.6
v18 neg_input gnd! dc=1.6 ac=1
v17 net46 gnd! dc=1.8









.option primesim_remove_probe_prefix = 0
.probe v(*) i(*) level=1

.temp 25



.option primesim_output=wdf


.option parhier = LOCAL






.end

## Two Stage Op-amp
*  Generated for: PrimeSim
*  Design library name: analog_ic_design
*  Design cell name: op-amp_stage-2
*  Design view name: schematic


*Custom Compiler Version S-2021.09
*Sun Feb 27 12:42:37 2022

.global gnd!
********************************************************************************
* Library          : analog_ic_design
* Cell             : op-amp_stage-2
* View             : schematic
* View Search List : hspice hspiceD schematic spice veriloga
* View Stop List   : hspice hspiceD
********************************************************************************
m7 output net14 net35 net35 pmos4 w=87.04u l=500n
m1 net9 net9 net35 net35 pmos4 w=7u l=500n
m0 net14 net9 net35 net35 pmos4 w=7u l=500n
m6 output vb gnd! gnd! nmos4 w=37.5u l=500n
m5 net16 vb gnd! gnd! nmos4 w=6u l=500n
m4 vb vb gnd! gnd! nmos4 w=6u l=500n
m3 net14 in2 net16 gnd! nmos4 w=3u l=500n
m2 net9 in1 net16 gnd! nmos4 w=3u l=500n
i19 net35 vb dc=20u
v22 in1 in2 dc=0 ac=1m
v10 in2 gnd! dc=0.8
v9 net35 gnd! dc=1.8
c20 output gnd! c=1p
c11 net14 output c=800f









.option primesim_remove_probe_prefix = 0
.probe v(*) i(*) level=1

.temp 25



.option primesim_output=wdf


.option parhier = LOCAL






.end
