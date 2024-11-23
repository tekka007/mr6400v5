# TP-Link OEM firmware recovery

1. Obtain OEM firmware file from here: https://static.tp-link.com/2021/202105/20210507/TL-MR6400(EU)_V5_201207.zip
2. Extract .zip
3. dd if=TL-MR6400v5_1.3.0_0.9.1_up_boot(201207)_all_2020-12-08_08.39.09.bin of=tp_recovery.bin skip=1 bs=512 count=16000
4. Create TFTP server listening on 192.168.0.225/24 and place tp_recovery.bin in folder
5. Press RESET + plug power cable, wait for 8 secs => TFTP bootloader will fetch tp_recovery.bin
6. Wait a 1-3 minutes until led stops blinking
7. Access UI at 192.168.1.1
