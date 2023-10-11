Conax compatible smart card using BasicCard ZC5.x

burn .img file to basiccard with Omnikey 3021 SCPC reader

"BCLoad.exe conax_0b00.IMG -P100 -ST"

Personalize Card with:

conax.exe --port COM1 --ppua 100000000000 --ppsa 999999 --pass D7BgaTjL2vUIPhud

D7BgaTjL2vUIPhud = my own password

put it in your CI and do an onboarding within CAS-System 

Update 20230919:

switch added for 64-Bit/48-Bit CW via access-criteria highest bit (bit 31)
-	--access-criteria 00000001 = 48-Bit CW (reduced entropy)
-	--access-criteria 80000001 = 64-Bit CW (full entropy) (works mostly on softcam, real CI automaticly reduces the entropy to 48-Bit)
