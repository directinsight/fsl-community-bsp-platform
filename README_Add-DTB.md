# How to add a Board Specific DTB (Example imx6dl-tx6s-8034-phoenix.dtb)

In order to add a board specific DTB use the existing module specific dts file from the linux source tree (for example imx6dl-tx6s-8034.dts) and copy it to meta-fsl-arm-extra/recipes-kernel/linux/(kernel). Add an append for the board name for example imx6dl-tx6s-8034-phoenix.dts. Modify the contents of this dts file as required.

Created new machine config in meta-fsl-arm-extra/tree/krogoth/conf/machine. Again use the module specific config file as a reference and update the KERNEL_DEVICETREE and TXBASE_append for example tx6s-8034-phoenix.conf.
    
Created corresponding dtb: sources/meta-fsl-arm-extra/recipes-kernel/linux/linux-karo-4.4.15/imx6dl-tx6s-8034-phoenix.dts
    
Add the new DTS file SRC_URI to the kernel recepie file: meta-fsl-arm-extra/recipes-kernel/linux/linux-karo_4.4.15.bb
