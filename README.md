Complete configuration for connecting multiple **SEPLOS v.03 (16 cells)** BMS to **Home Assistant** via **Modbus TCP** using **Elfwin EW11A**.

With this project, I've gathered all the information and configurations needed to directly integrate Seplos BMSs, as well as many others with knowledge of their ModBus protocols, into Home Assistant.

What do you need?
- A non-switched LAN cable.
- An Elfwin EW11A (or similar).
- 5/12v charger
- Obviously, a BMS with ModBus protocol.

Let's proceed:
Cut the LAN cable and strip the white-orange and orange wires.

Connect the first to pin A and the second to pin A. Then connect it to the Seplos RS485 output (see image).

Log in to the Elfwin AP, go to "others" and upload the "EW11_Seplos" backup file, making sure to change the IP address to the one assigned by your router.

Set the Elfwin IP address to static on the router.

Add the yaml files to the /config of Home Assistant, modifying "configuration.yaml" with the strings from the "configuration..." file attached to the repository.

If you need to monitor multiple, unconnected packages (slave and master), rename the file, the IP address of the new Elfwin, and the name of the new device, as shown in the differences between the seplos_1 and _2 files.

References Official SEPLOS BMS Modbus RTU Protocol Tested and verified by @Xcpro1.
