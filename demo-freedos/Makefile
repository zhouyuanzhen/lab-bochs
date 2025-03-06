prepFD12:
	test -s FD12FLOPPY.zip || wget -c https://www.ibiblio.org/pub/micro/pc-stuff/freedos/files/distributions/1.2/official/FD12FLOPPY.zip
	test -s FLOPPY12.img || unzip FD12FLOPPY.zip -x README.md
	test -s FLOPPY12.img || mv FLOPPY.img FLOPPY12.img

prepFD13:
	test -s FD13-FloppyEdition.zip || wget -c https://www.ibiblio.org/pub/micro/pc-stuff/freedos/files/distributions/1.3/official/FD13-FloppyEdition.zip
	test -d 144m || unzip FD13-FloppyEdition.zip -x readme.txt 720k* 120m*

runFD12:
	bochs -f bochs-fd12.bxrc -q

runFD13:
	bochs -f bochs-fd13.bxrc -q

clean:
	rm -f log.fd.txt

purge: clean
	rm -f FLOPPY*.img
