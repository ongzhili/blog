## Greycat's Adventure: Timelock

I used cheat engine to speed up the application to some really large number (I tried 180,000 in fear that my pc explodes), and simply waited till the flag showed up

![alt text]({{ site.url }}{{ site.baseurl }}/assets/images/image.png)

FLAG: `grey{d1d_y0u_r34lly_w4it_f1fty_h0ur5???:thinking:}`

## Greycat's Adventure: Vault

I just used cheat engine to slow down the application to 0.1 and manually typed the flag.

FLAG: `grey{th3_numb3r5_m450n_wh4t_d0_th3y_m34n??!}`

## Greycat's Adventure: Achievement 3

Upon opening the credits screen, there are some lines of morse code among the credits. Piecing them together gives

`GIGACATGIGACHAD`

Which I put into the text box in the achievement screen (in small characters) to obtain the flag

![alt text]({{ site.url }}{{ site.baseurl }}/assets/images/image-1.png)

FLAG: `grey{th3_c4t_15_0u7_0f_th3_b4g_la138df}`

## Sanity check

Join discord server read announcements

FLAG: `grey{w3lc0m3_to_gctf2024_enjoy_your_stay!}`

## Out in plain sight

osint challenge. Viewed latest video on @nus.greyhats and tried all the flags at the end, but didn't work, but saw this.

![alt text]({{ site.url }}{{ site.baseurl }}/assets/images/image-3.png)

Which, when decoded from hex, gives '18 seconds'

Hence, I moved to 19 seconds of the video, and found the flag.

![alt text]({{ site.url }}{{ site.baseurl }}/assets/images/image-2.png)

FLAG: `grey{y0uR_eYeS_aRe_5hArP}`

## Cashhat The Ripper

I initially tried frackzip with rockyou.txt but it didn't work for some reason. (Although the password was in the file, perhaps I typed the command wrongly).

In the end I used a program called ZipRipper (which I'm pretty sure just does the same thing, where it checks with every possible password on fcrackzip) to crack the password, which was `123mango`.

Opening the flag.txt inside reveals the flag.

FLAG: `flag{W34k_P4ssw0rds_St4Nd_n0_Ch4nc3}`

## Grey Divers

Hmm, I don't play Helldivers 2. That's not good. So I went to search the internet to find out what these weapons are. Turns out, there is a stratagem code of some sort where players enter a sequence to call it down?

Which was convenient, as the image provided is a grid, and traversing the grid would give the flag.

Hence, I searched up some helldivers wiki to find the directions.

EAGLE BOMB:![alt text]({{ site.url }}{{ site.baseurl }}/assets/images/image-4.png)

GL-21 ![alt text]({{ site.url }}{{ site.baseurl }}/assets/images/image-5.png)

MD-I4 ![alt text]({{ site.url }}{{ site.baseurl }}/assets/images/image-6.png)

Orbital Gas Strike: ![alt text]({{ site.url }}{{ site.baseurl }}/assets/images/image-7.png)

Orbital Airburst Strike: ![alt text]({{ site.url }}{{ site.baseurl }}/assets/images/image-8.png)

Eagle Rearm: ![alt text]({{ site.url }}{{ site.baseurl }}/assets/images/image-9.png)

Eagle 110mm: ![alt text]({{ site.url }}{{ site.baseurl }}/assets/images/image-10.png)

Starting from home, we get:

![alt text]({{ site.url }}{{ site.baseurl }}/assets/images/image-11.png)

OR:

FLAG: `grey{i3mm_e1w3st_2_n3oU10o3E!}`

## Baby Web

Part 1:

I used `flask-unsign -u -c eyJpc19hZG1pbiI6ZmFsc2V9.ZiQTlw.ZDIT94EeNUGjpuGRtQZ_StS0Cog`
to obtain the cookie info, which revealed itself to just be `{'is_admin': False}`

Hence, with the secret key found in `main.py`, we simply sign it with `{'is_admin': True}`, and edited the cookie on the browser to obtain access to the `/admin` page.

![alt text]({{ site.url }}{{ site.baseurl }}/assets/images/image-12.png)

Part2: Was not able to solve.