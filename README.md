# Successful build: AMD Ryzen 7 3700X, AMD Radeon RX 5700XT, Aorus Elite X570

You can check more details [here](https://www.reddit.com/r/Ryzentosh/comments/ip1tb8/successful_build_amd_ryzen_7_3700x_amd_radeon_rx/).

This build doesn't have either `agdpmod=pikera` or `WhateverGreen.kext`, since its latest version seems to be incompatible with my AMD Radeon RX 5700XT. **However**, you might want to add WhateverGreen if you're installing with an unsupported GPU (So you can at least see the installer, no acceleration).

## Benchmarks

- [CPU](https://browser.geekbench.com/v5/cpu/3544085)
- [OpenCL](https://browser.geekbench.com/v5/compute/1464248)
- [Metal](https://browser.geekbench.com/v5/compute/1464259)

## Photos

https://imgur.com/a/5hJOw1S

## Additional Notes

You'll need to add your own serial numbers.

```
<dict>
    <key>AdviseWindows</key>
    <false/>
    <key>MLB</key>
    <string>M0000000000000001</string>
    <key>ROM</key>
    <data>ESIzRFVm</data>
    <key>SpoofVendor</key>
    <true/>
    <key>SystemProductName</key>
    <string>iMacPro1,1</string>
    <key>SystemSerialNumber</key>
    <string>W00000000001</string>
    <key>SystemUUID</key>
    <string>00000000-0000-0000-0000-000000000000</string>
</dict>
```

I don't know if this build supports multi-monitor, but since it is using the integrated drivers from macOS it should.

The tricky parts are GPU swapping because is not just installing with another GPU and then swap the `RX 5700XT`. You'll probably need to enable `WhateverGreen.kext` , boot with another GPU, disable `WhateverGreen.kext` and then insert the `RX 5700XT`.

**This build was done using OpenCore 6.0, so keep that in mind while searching for any solutions**

## Additional Hardware

- **WiFi:** TP-Link Archer T9UH
