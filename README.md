# BIeTgatepowers
Algorithm to find ideal gate powers for bells inequality test outlined in Quantum Computing: An Applied Approach by J. Hidary
I couldn't figure out how to apply appropriate gate powers at one point, so I cycled through every possible gate power value 
to attempt to maximise the theoretical bells inequality condition of 85%. Values of gates should be to the power of -0.25 for the non-controlled
xgate and 0.5 for both controlled xgate.
This code was slow since for every decimal value for two different gate powers there was 100+ iterations of quantum jobs being run. 
Which led me to create a gradient like method that would only calculate the values around an index then move to that index until the maximum
value was found at the initial index. This spead up the calculations by a significant amount and was still fairly accurate infinding the maximum
value.
The issue with finding the theoretical maximum is the noise that a quantum computer generates, so the maximum it calculates also changes. 
It also finds values that exceed the theoretical max and reach values of 86% or 87%, which is due in part through noise.
