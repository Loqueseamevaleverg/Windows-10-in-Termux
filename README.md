#INSTALL

$ curl -o setup1.sh https://raw.githubusercontent.com/AnBui2004/termux/refs/heads/main/setupvm/10/10159.sh && chmod +rwx setup1.sh && ./setup1.sh && curl -o setup2.sh https://raw.githubusercontent.com/AnBui2004/termux/refs/heads/main/setupqemu/setupqemuvm1.sh && chmod +rwx setup2.sh && ./setup2.sh && rm setup2.sh && rm setup1.sh && clear


#INSTALL X11 REPO AND EXECUTE THIS:

termux-x11 :1 -xstartup "qemu-system-x86_64 -M q35 -device qemu-xhci -device usb-tablet -device usb-kbd -cpu qemu64,+sse,+sse2,+sse4.1,+sse4.2,+svm,hv-relaxed -smp sockets=1,cores=1,threads=1 -overcommit mem-lock=off -m 2048M -device qxl-vga,ram_size_mb=4000,vram_size_mb=4000,vram64_size_mb=4000 -device ich9-intel-hda -device hda-duplex -device e1000e,netdev=n0 -netdev user,id=n0,dns=8.8.8.8 -accel tcg,thread=multi,tb-size=128,split-wx=on -device intel-iommu -monitor stdio -name One -uuid 276e9110-320b-f80c-14a1-6e430bf4f260"
