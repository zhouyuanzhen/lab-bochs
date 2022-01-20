bin:
	nasm -o mbr.bin mbr.S

fdimg:
	dd if=/dev/zero of=fd.img bs=1024 count=1440 

hdimg:
	bximage -hd=64M -imgmode=flat -func=create -q hd.img

burnfd: bin fdimg
	dd if=mbr.bin of=fd.img bs=512 count=1 conv=notrunc

burnhd: bin hdimg
	dd if=mbr.bin of=hd.img bs=512 count=1 conv=notrunc

run-fd:
	bochs -f bochs-fd.bxrc -q

run-hd:
	bochs -f bochs-hd.bxrc -q

clean:
	rm -f mbr.bin log.fd.txt log.hd.txt fd.img hd.img
