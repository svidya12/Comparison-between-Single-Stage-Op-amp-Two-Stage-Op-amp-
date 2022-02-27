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
![image](https://user-images.githubusercontent.com/70511616/155881958-9835c3b0-a8ac-4dc8-a2fc-5af3f32d5214.png)

