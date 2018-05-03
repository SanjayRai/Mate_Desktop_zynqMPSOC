# Mate_Desktop_zynqMPSOC
ZynQ MpSoc with  Arch Linux with Mate desktop

Refer to the srai_plnx_proj.README  test *document* for full instructions:

The goal is to install ArchLinux with Mate Desktop on ZynQ MPSoc starting with Vvado IPI Block diagram.

1. Create a ZynQ MPSOC Block diagram in Vivado IPI and configure it for the board.
2. Generate the Bitfile and Export Hardware (along with the bitfile). This create a HDF file (location = HDK_Export)
3. Use petaLinux tool chain to build BOOT.BIN and rootfs (but we wont' use the rootfs)
4. Create an SD Card with 2 Partitions Boot partiton as FAT32 and rootfs partiton (EXT4) 
5. Download BOOT.BIN and image.ub to  Partition 1 (Boot partition) of the SD Card
6. Copy the Latech ArchLinux rootfs to partiton2 (EXT4)
7. use pacman Package manager to install various tools including vncserver.
