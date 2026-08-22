# QR stego crypt

MATLAB experiment in hiding one QR code inside an image while a second one
sits in plain sight as a decoy.

The real message QR is XORed with three generated keys, and those keys are
themselves XORed with a master key. The decoy QR then goes into the least
significant bits of the cover image's green channel and the encrypted one
into the blue channel. The rest of the script pulls both back out and
decrypts, plotting every step.

Run myStego.m in MATLAB. QR encoding uses ZXing through the bundled
core.jar and javase.jar. Written in 2022.
