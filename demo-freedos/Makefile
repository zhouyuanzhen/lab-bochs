run:
	bochs -f bochs-fd.bxrc -q

prepFD12:
	test -s FD12FLOPPY.zip || wget -c https://www.ibiblio.org/pub/micro/pc-stuff/freedos/files/distributions/1.2/official/FD12FLOPPY.zip
	unzip FD12FLOPPY.zip -x README.md
	mv FLOPPY.img FLOPPY12.img

prepFD13:
	test -s FD13-FloppyEdition.zip || wget -c https://www.ibiblio.org/pub/micro/pc-stuff/freedos/files/distributions/1.3/official/FD13-FloppyEdition.zip
	unzip FD13-FloppyEdition.zip -x readme.txt 720k* 120m*
	# mv FLOPPY.img FLOPPY13.img

clean:
	rm -f log.fd.txt

purge: clean
	rm -f FLOPPY*.img
