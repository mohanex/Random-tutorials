# Follow my Desktop PC Hardware Troublshooting step by step (Future Home Server Hosting LLMs)

Hello all,

This is my first article on Medium, and I hope you’ll find it helpful. Some time ago, I wanted to build my personal home server using an old desktop computer. However, I encountered an issue getting it to work. The computer features an Intel Core i7–6700 processor, 16GB of RAM, and a GTX 1080 graphics card, which should be more than enough to handle basic server functions and run some local LLMs.

The computer had been left untouched in a room for over a year without being turned on. When I attempted to power it up, it seemed to start, but there was no video output on my screen. Both the GPU and motherboard had lights on, but the PC would restart itself every 10 seconds.
<img width="1206" height="704" alt="Image1" src="https://github.com/user-attachments/assets/d894ef6e-6d64-42ec-a3b6-c327319e948c" />
Having quite a bit of experience with hardware troublshooting, I always check components following this list:
- GPU (Video output source)
- PSU + Connectors (Non-working cables)
- RAMs
- Motherboard + CPU

In order to test those parts, It will be easier if you have another desktop computer that you are sure is working to use for parts swaping.

Following the list above, I began by looking into the GPU. I removed the GPU and tested the PC without the graphics card, using a VGA cable connected to an external monitor, but still, no image appeared, and the PC continued to restart itself every 10 seconds. Then I tried a different GPU card (GTX 970), but the problem persisted. This led me to conclude that the issue lay elsewhere and that the GPU was functioning correctly.

After GPU check, I went looking for another PSU, but not having one I switched PSUs with my personal desktop PC. The problem is gone? not that fast, I still encountered the same issue, but this time, using a relatively new PSU, I noticed a red light turning on and off whenever I powered on the PC. To help isolate the problem, and test weither the new or old PSU has a problem, I put my old Power supply into my new PC and fair enough it worked without any issues.

<img width="1209" height="708" alt="Image2" src="https://github.com/user-attachments/assets/4c49afe1-7b5b-445c-8fb4-7b56acbfdfd6" />

Don’t forget to take notes, guys! these manual operations of switching parts are time consuming, and sometimes we tend to check one part per day, thus we can easily forget which parts we’ve already tested. My table of notes looks like this for now:

<img width="219" height="216" alt="Image3" src="https://github.com/user-attachments/assets/4c07ae25-7653-411c-ac72-0367535b04db" />


Moving on, I switched RAMs between the two computers. Turning them on at the same time, my new pc with old RAM doesn’t work and it remains stuck at BIOS DRAM verification with a red light on the motherboard blinking. Whereas my Old Computer stopped switching on and off every 10s but still don’t output any video. Conclusion? My old RAM definitely has a short-circuiting problem.

<img width="696" height="443" alt="Image4" src="https://github.com/user-attachments/assets/4e52102f-750c-4222-baf0-41b5657a651d" />

New notes table :

<img width="208" height="209" alt="Image5" src="https://github.com/user-attachments/assets/7677a79a-2958-4339-a234-c361e6d6c95d" />

Now that I’ve isolated the problem and confirmed that my RAM is causing the issue, we still can’t call it a win due to the lack of video output. I continued testing my computer without a graphics card, this time combining the newly installed RAM with a GPU. Initially using the GTX 1080, it worked!!!

<img width="1209" height="711" alt="Image6" src="https://github.com/user-attachments/assets/7185f291-20c4-40ae-ba3d-e1d971b140b3" />

I finally managed to get my old PC to work. The problem was caused by the RAM’s short-circuiting issue and my motherboard’s VGA connector. We can now do a final update of our checklist, and it will look like this:

<img width="352" height="212" alt="Image7" src="https://github.com/user-attachments/assets/725fed3f-9f40-4904-bc23-b29a5530c6b5" />

If sometime you got to troubleshoot your PC as I did, here’s the “lecture notes” you need to write down:

- Always start checking parts related to your issue (e.g. No video output -> GPU)
- Take notes
- Switching parts is time consuming, so make sure to have enough time, otherways your pc will finish exposed in a corner of your room
- Try rechecking parts you already checked
- Ask local repairing shops to borrow some parts if you don’t have doubles
Thank you for reading my very first article!! Stay tuned for the next one, where I’ll be installing a Linux server and some local LLMs.
