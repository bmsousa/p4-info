## GOAL
This page is created for newcomers to P4 who ask for "what hardware can one use to prototype P4 code?"

## Terminology 

(a) A hardware target is a switching asic, FPGA, NPU, or generic compute.  
(b) A hardware platform is a switch (using asic), smartNIC (using FPGA or NPU), or server/laptop machine. 

## List
The list covers hardware targets and platforms supporting P4-16 in abphabetical order.  Supporting p4 entails the target supports a p4c (P4 compiler) backend.  A hardware target is useles without a P4 compiler (p4c) - therefore compiler vendors are also listed.  Lastly, a target that only supports p4runtime is not included.

For FPGA, Xilinx provides their P4 programming tools chain.  There is also Netcope who has a tools chain for P4 programming FPGA from Intel and Xilinx.

###
1. Barefoot Networks Tofino/Tofino2 asic in ODM switches - some ODM vendors are Edgecore (https://www.edge-core.com/), Netberg (https://netbergtw.com/about/), Inventec (https://www.inventec.com/english/indexEN.htm), Delta, WNC (http://www.wnc.com.tw/mobile/index.php?action=product_detail&top_id=28&scid=31&tid=99&lid=99&id=353), and Foxconn.  Stordis and Kaloom use ODM switches with open or proprietary switch OS. 

2. Mellanox has Spectrum/Spectrum2 asic.  Their switch implementation uses Linux TC. Mellanox has a p4c backend that they plan to open source (as soon as we get it modularized from our common backend infra). Marian presented this at this year's netdev conference. https://www.netdevconf.org/0x13/session.html?p4-compiler-backend-for-tc

3. Intel has P4 to DPDK: https://www.youtube.com/watch?v=uI29_q-SoPU .  Also see http://lists.p4.org/pipermail/p4-dev_lists.p4.org/2019-June/003981.html

4. Netcope : https://www.netcope.com/en/products/netcopep4.  Has tools chain to program FPGA with P4 (p4-16?)

5. Netronome NIC using NPU - has p4 compiler.  https://www.netronome.com/products/datapath-programming-tools/

6. Orange: Has a p4c backend for linux user space.  See https://github.com/P4-Research/p4c/tree/master/backends/ubpf

7. p4lang/p4c EBPF (Enhanced Berkeley Packet Filter).  EBPF runs inside Linux kernel.  https://github.com/p4lang/p4c/tree/master/backends/ebpf

8. Xilinx FPGA with P4 compiler.  https://www.xilinx.com/support/documentation-navigation/development-tools/software-development/sdnet.html



Specifically, no openwrt access point implementation for P4 exists.
 
