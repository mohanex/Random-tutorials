# Follow my Desktop PC Hardware Troublshooting step by step (Future Home Server Hosting LLMs)

Hello all,

This is my first article on Medium, and I hope you’ll find it helpful. Some time ago, I wanted to build my personal home server using an old desktop computer. However, I encountered an issue getting it to work. The computer features an Intel Core i7–6700 processor, 16GB of RAM, and a GTX 1080 graphics card, which should be more than enough to handle basic server functions and run some local LLMs.

The computer had been left untouched in a room for over a year without being turned on. When I attempted to power it up, it seemed to start, but there was no video output on my screen. Both the GPU and motherboard had lights on, but the PC would restart itself every 10 seconds.

![alt text](https://github.com/mohanex/Random-tutorials/blob/main/Desktop_Hardware_Troubleshooting/image1.jpg)

Having quite a bit of experience with hardware troublshooting, I always check components following this list:
- GPU (Video output source)
- PSU + Connectors (Non-working cables)
- RAMs
- Motherboard + CPU

In order to test those parts, It will be easier if you have another desktop computer that you are sure is working to use for parts swaping.

Following the list above, I began by looking into the GPU. I removed the GPU and tested the PC without the graphics card, using a VGA cable connected to an external monitor, but still, no image appeared, and the PC continued to restart itself every 10 seconds. Then I tried a different GPU card (GTX 970), but the problem persisted. This led me to conclude that the issue lay elsewhere and that the GPU was functioning correctly.

After GPU check, I went looking for another PSU, but not having one I switched PSUs with my personal desktop PC. The problem is gone? not that fast, I still encountered the same issue, but this time, using a relatively new PSU, I noticed a red light turning on and off whenever I powered on the PC. To help isolate the problem, and test weither the new or old PSU has a problem, I put my old Power supply into my new PC and fair enough it worked without any issues.

![alt text](image2.jpg)

Don’t forget to take notes, guys! these manual operations of switching parts are time consuming, and sometimes we tend to check one part per day, thus we can easily forget which parts we’ve already tested. My table of notes looks like this for now:

![alt text](image3.jpg)

Moving on, I switched RAMs between the two computers. Turning them on at the same time, my new pc with old RAM doesn’t work and it remains stuck at BIOS DRAM verification with a red light on the motherboard blinking. Whereas my Old Computer stopped switching on and off every 10s but still don’t output any video. Conclusion? My old RAM definitely has a short-circuiting problem.

![alt text](image4.jpg)

New notes table :

![alt text](image5.jpg)

Now that I’ve isolated the problem and confirmed that my RAM is causing the issue, we still can’t call it a win due to the lack of video output. I continued testing my computer without a graphics card, this time combining the newly installed RAM with a GPU. Initially using the GTX 1080, it worked!!!

![alt text](image6.jpg)

I finally managed to get my old PC to work. The problem was caused by the RAM’s short-circuiting issue and my motherboard’s VGA connector. We can now do a final update of our checklist, and it will look like this:

![alt text](image7.jpg)

If sometime you got to troubleshoot your PC as I did, here’s the “lecture notes” you need to write down:

- Always start checking parts related to your issue (e.g. No video output -> GPU)
- Take notes
- Switching parts is time consuming, so make sure to have enough time, otherways your pc will finish exposed in a corner of your room
- Try rechecking parts you already checked
- Ask local repairing shops to borrow some parts if you don’t have doubles
Thank you for reading my very first article!! Stay tuned for the next one, where I’ll be installing a Linux server and some local LLMs.
