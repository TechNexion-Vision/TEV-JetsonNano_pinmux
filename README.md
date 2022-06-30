## TEV-JetsonNano_pinmux
The Jetson Nano pinmux file, for JetsonNano TN-TEK 3 series.

### Folder location(created by TEV-Jetson_Jetpack_script)
```
<nvidia_folder>/Linux_for_Tegra/sources/TEK3-NVJETSON_Nano_pinmux
```
&nbsp;
### Create pinmux file
Edit **Nano_TEK3-NVJETSON_Pinmux.xlsm** under windows environment.

 Click On the **macro**(Generate DT file) on top of the xlsm.
![image](https://user-images.githubusercontent.com/83322668/176588919-7d3881d0-d19f-44f7-8f5e-91c0d087607a.png)

 Click OK.

![image](https://user-images.githubusercontent.com/83322668/176589218-bcaef8fb-8089-4d58-b108-b52adce7f833.png)

 Type the \<name\>. (For example: tek3)
 
![image](https://user-images.githubusercontent.com/83322668/176586123-439a7da3-b17e-4616-9d27-9e2ea31ad262.png)

You will see this result.

![image](https://user-images.githubusercontent.com/83322668/176586209-d91bf5ed-88ac-4936-bf7e-3deb67d44d16.png)

### Copy files to device-tree location (For example: tek3)
Copy **tegra210-tek3-gpio-default.dtsi**
to 
```
<nvidia_folder>/Linux_for_Tegra/sources/hardware/nvidia/platform/t210/porg/kernel-dts/porg-platforms/tegra210-tek3-nvjetson-a1-gpio-default.dtsi
```
Copy **tegra210-tek3-pinmux.dtsi**
to 
```
<nvidia_folder>/Linux_for_Tegra/sources/hardware/nvidia/platform/t210/porg/kernel-dts/porg-platforms/tegra210-tek3-nvjetson-a1-pinmux.dtsi
```

### Take effect
Just re-compile and use the new kernel/ device-tree.
``` coffeescript
$ cd <nvidia_folder>/Linux_for_Tegra/sources/kernel/kernel-4.9/
$ ./compile_kernel.sh
```

(\<device-tree>.dtb for **TEK3-NVJETSON**: tegra210-tek3-nvjetson-a1.dtb)

Copy **Linux_for_Tegra/sources/kernel/kernel-4.9/arch/arm64/boot/dts/\<device-tree>.dtb**

to device 
```
/boot/
```
