# Configuring-SSH

Two operating systems will be used: Windows Server 2022 and Windows 10 Enterprise.
In this scenario, there is an active directory set up with the Windows Server 2022 as the domain controller, and Windows 10 Enteprise consisting of a regular user account and an administrator account. The domain is named `TestDomain`.

# Setting up SSH

The following steps to set up SSH will be the same on both Windows Server 2022 and Windows 10 Enterprise. From Microsoft's documentation, there are two ways to install SSH onto your system: using the Windows GUI or through PowerShell. For this guide, the GUI will be used for easier navigation and understanding.

1. Open the `Settings` app and click into `Apps`.
![pBhgIjEtC3](https://github.com/johnnyh209/Configuring-SSH/assets/33064730/dcee1320-5f2f-4009-aa9e-39ac0beafd01)

2. In the `Apps & features` tab, click on `Optional features`.
![D42b1prxD2](https://github.com/johnnyh209/Configuring-SSH/assets/33064730/1edbf0b4-f837-409f-a493-7fc35190d528)

3. Check the list of already installed features to see if `OpenSSH Client` and `OpenSSH Server` are already installed. For me, `OpenSSH Client` has already been pre-installed.
![VirtualBoxVM_9ErQNofAKr](https://github.com/johnnyh209/Configuring-SSH/assets/33064730/0f05469c-768c-4c2c-8ecb-2026667fd773)

4. At the top of the `Optional features` page you are on, click on `Add a feature` and type in `OpenSSH` to find `OpenSSH Client` and/or `OpenSSH Server` so you can install them. Because I already have `OpenSSH Client` installed, only `OpenSSH Server` showed up.
![2pOgaWnLeC](https://github.com/johnnyh209/Configuring-SSH/assets/33064730/e5b308a5-94b9-4881-b849-07ffaa9a7def)
![NRtPtuH8Tb](https://github.com/johnnyh209/Configuring-SSH/assets/33064730/0a4c9d8c-3f1d-46d2-babc-2fd5a01ea5bf)

5. Once installed, check that both `OpenSSH Client` and `OpenSSH Server` have successfully been installed in the `Optional features` page.
![0BLR6QGjbl](https://github.com/johnnyh209/Configuring-SSH/assets/33064730/8a3acfb2-859a-47d8-be63-0d86bb257a2a)

Now, we want to ensure that SSH has been added to the Environment Variable, specifically `Path`. Environment Variable is used to store data that can be shared between/across different applications or processes. By storing SSH in the `Path` variable, when we invoke the command in PowerShell, PowerShell is able to located where SSH is stored by looking at the Path variable.

6. Open `Settings` and click into `System`, and then into the `About` page. Within `System`, click `Advanced system settings`. This should open up the `System Properties` box.
![RrDQmuDIit](https://github.com/johnnyh209/Configuring-SSH/assets/33064730/b84bd18a-6f8d-41eb-8b4d-9e12552c1cf5)

7. Click on the `Environment Variables` button at the bottom.
![bBwrYffc8o](https://github.com/johnnyh209/Configuring-SSH/assets/33064730/9408219d-956e-4dde-99a6-086aef6b6064)

9. In the bottom half of the `Environment Variables` box, select `Path` and click on the `Edit` button.
![4OYvHhzkzp](https://github.com/johnnyh209/Configuring-SSH/assets/33064730/dfddddf6-9249-46f8-909f-d13760918f91)

10. 
