VENDOR=AIAIAI
PROJECT_NAME=H05
VERSION=1.6
FIRMWARE_FILE=h05_v1-6.dfu
METAINFO_FILE=h05.metainfo.xml

all: $(VENDOR)-$(PROJECT_NAME)-$(VERSION).cab

clean:
	rm -f *.cab

check: $(METAINFO_FILE)
	appstream-util validate-relax $(METAINFO_FILE)

%.cab: $(FIRMWARE_FILE) $(METAINFO_FILE)
	gcab --create --nopath $@ $(FIRMWARE_FILE) $(METAINFO_FILE)
