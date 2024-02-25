# Environment setup for VCK5000
All the install documents for different platforms can be found in: <br>
[VCK5000 Versal Development Card for AI Engine Secure Site](https://account.amd.com/en/member/vck5000-aie.html#tabs-46240f87a6-item-78e08a12a4-tab)

This Guild is focused on the **Ubuntu 20.04**
## Installation
Install Xilinx vitis 2022.2 <br>
Set environment and path: `source /tools/Xilinx/Vitis/2022.2/settings64.sh` <br>
Install Both [XRT](https://www.xilinx.com/bin/public/openDownload?filename=xrt_202220.2.14.384_20.04-amd64-xrt.deb) and [XRT-APU](https://www.xilinx.com/bin/public/openDownload?filename=xrt-apu-vck5000_202220.2.14.384_petalinux_all.deb) <br>
The 2022.2 Gen4x8 QDMA base 2 platform has been installed in VCK5000 <br>
Install [xilinx-vck5000-gen4x8-qdma-2](https://www.xilinx.com/bin/public/openDownload?filename=xilinx-vck5000-gen4x8-qdma_2022.2_2022_1212_1124-all.deb.tar.gz) in local machine <br>

## Check
Set up environment: `source /opt/xilinx/xrt/setup.sh` <br>
Runnint lspci: `sudo lspci -vd 10ee:`<br>
Confirm Firmware Installation: `sudo /opt/xilinx/xrt/bin/xbmgmt examine` <br>
Card Validation: `/opt/xilinx/xrt/bin/xbutil validate -d 0000:01:00.1` <br>
The Devices present BDF of my case is 00000:01:00.1, we can check from `sudo /opt/xilinx/xrt/bin/xbutil examine`

**Congratulations!** if you pass all the validation test
