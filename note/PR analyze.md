# PR analyze

## Overview

Total 299. 3 in CPSC2018_2, and 296 in PTBXL.

### HR00143

**Label: PR**

1. P wave -- not obvious
2. The spike is close to QRS wave
3. T wave -- weak
4. The whole ECG signal is irregular



For PR recognition:

The spike is much lower than Q waves(Or interval?). So the template might work on this figure.

It is not certain whether the spike is close to QRS wave will have an impact.

### HR00382

**Label: PR**

1. The jitter of the ECG signal is obvious

2. Still have that spike(very rare, which I marked) but seems not regular.

   -- It is strange cause I though PR interval is regular. SO maybe it is some kind of **NOISE**.

![image-20210607081501116](C:\Users\16778\AppData\Roaming\Typora\typora-user-images\image-20210607081501116.png)

3. I think other high waves are QRS waves

I think it is more like Atrial fibrillation, not Pacing Rhythm.

### HR00385

**Label: PR**

1. Not regular in lead I
2. Could be positive or negative, and the height is different

For PR recognition:

Use the width of the interval, not the height.

### HR01399/HR01461/HR00498

**Label: PR**

where is P wave?

where is QRS or where is PR interval? 

But it is easy to find spike by eyes.

### HR01596

**Label: PR, ICA, STE**

1. Seems to have a lot of noise interference
2. The highest waves should be QRS waves.

-- hard to find the PR interval!

For recognition:

Hard to find which one is the PR interval.

-- Need to deal with interference from other diseases

### HR01717

**Label: PR, SB**

1. Cannot find the spike.



### Q0398

**Label: PR, LVH, OldMI, MI, NSSTTA**

1. Hard to find the spike.
2. ![image-20210607123119081](C:\Users\16778\AppData\Roaming\Typora\typora-user-images\image-20210607123119081.png)

Maybe it is one marked on red.



For recognition:

If it is the one marked on red, then it hard to use the width of interval. or maybe it is the little spike before the minus wave(I consider it as QRS waves)

### Q1033

**Label: PR, NSSTTA**

1. hard to find the spike
2. where is P, T waves

### Q1807

**Label: PR, NSSTTA, SNR**

1. hard to find the spike



## Conclusion

Lots of figures can be solved by a template(use width).

Somehow, some patients have a variety of diseases which might cause the spikes that are hard to find.

In addition, the noise(or other volatility) needs to be deal with.

