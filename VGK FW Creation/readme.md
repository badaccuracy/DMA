# Creation of VGK Firmware

#### Before starting this, I want to thank my friend Movinggun for initially showing me this method/technique on how to bypass VGK 💖. I was going to release this earlier but I wanted a go from him.

> [!WARNING]
> The VGK bypass has been patched, and no longer works. Props to them for being malware. no Anti-Cheese should run at UEFI boot.
> 


> [!NOTE]
> This method only works for primarily MSI motherboards, other motherboards may work, but I suggest you use an MSI motherboard for this method.
>
> It is been found that some DMA speed tests won't recognise the DMA card and others will


Before you do the steps below, it is required to complete the customisations shown [here](https://github.com/Rakeshmonkee/DMA/blob/main/EAC-BE%20FW%20Creation/EAC-BE%20FW%20Customisations) as the steps below are an add on.


This section will be quick and easy as there aren't many things to change

Within the core_top.v file,

1. set `HEADER_TYPE` to 80,
2. set `CAPABILITIES_PTR` to 80

By changing just these 2 values to 80 within the config space, you will break the config space and allow us to bypass VGK. If you do a speed test, tiny pcie tlp algo might be selected, this is for you to fix. Go NULL some stuff out in the config space till tiny pcie tlp algo goes away. I suggest you expand on this more, don't just change some values and Header_Type and Cap_Ptr. For this to last a while you need more changes within the config space.



Now you can save $200+ just by changing 2 lines
