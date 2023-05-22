all: clean fetch patch 
.PHONY: all

.PHONY: fetch
fetch:
	git clone https://github.com/peppermintos/ice.git work

.PHONY: patch
patch:
	patch work/usr/bin/ice < files/patch-ice
	sed -i '' -e 's/chromium-browser/chrome/g' ./work/usr/bin/ice
	patch work/usr/bin/ice-firefox < files/patch-ice-firefox

.PHONY: install
install:
	mkdir /usr/local/lib/peppermint
	mkdir /usr/local/lib/peppermint/ice
	mkdir /usr/local/share/ice
	mkdir /usr/local/share/ice/locale
	mkdir /usr/local/share/ice/locale/fr
	mkdir /usr/local/share/ice/locale/fr/LC_MESSAGES
	mkdir /usr/local/share/ice/locale/ja
	mkdir /usr/local/share/ice/locale/ja/LC_MESSAGES
	mkdir /usr/local/share/ice/locale/nl
	mkdir /usr/local/share/ice/locale/nl/LC_MESSAGES
	mkdir /usr/local/share/ice/locale/pl
	mkdir /usr/local/share/ice/locale/pl/LC_MESSAGES
	mkdir /usr/local/share/ice/locale/pt_BR
	mkdir /usr/local/share/ice/locale/pt_BR/LC_MESSAGES
	mkdir /usr/local/share/ice/locale/pt_PT
	mkdir /usr/local/share/ice/locale/pt_PT/LC_MESSAGES
	mkdir /usr/local/share/ice/locale/sv
	mkdir /usr/local/share/ice/locale/sv/LC_MESSAGES
	mkdir /usr/local/share/ice/locale/zh_CN
	mkdir /usr/local/share/ice/locale/zh_CN/LC_MESSAGES
	cp work/usr/bin/ice /usr/local/bin/ice
	cp work/usr/lib/peppermint/ice/ice.glade /usr/local/lib/peppermint/ice/ice.glade
	cp work/usr/lib/peppermint/ice/places.sqlite /usr/local/lib/peppermint/ice/places.sqlite
	cp work/usr/lib/peppermint/ice/search.json.mozlz4 /usr/local/lib/peppermint/ice/search.json.mozlz4
	cp work/usr/share/applications/ice.desktop /usr/local/share/applications/ice.desktop
	cp work/usr/share/pixmaps/ice.png /usr/local/share/pixmaps/ice.png
	cp work/usr/share/ice/locale/fr/LC_MESSAGES/messages.po  /usr/local/share/ice/locale/fr/LC_MESSAGES/messages.po
	cp work/usr/share/ice/locale/ja/LC_MESSAGES/messages.po  /usr/local/share/ice/locale/ja/LC_MESSAGES/messages.po
	cp work/usr/share/ice/locale/nl/LC_MESSAGES/messages.po  /usr/local/share/ice/locale/nl/LC_MESSAGES/messages.po
	cp work/usr/share/ice/locale/pl/LC_MESSAGES/messages.po  /usr/local/share/ice/locale/pl/LC_MESSAGES/messages.po
	cp work/usr/share/ice/locale/pt_BR/LC_MESSAGES/messages.po  /usr/local/share/ice/locale/pt_BR/LC_MESSAGES/messages.po
	cp work/usr/share/ice/locale/pt_PT/LC_MESSAGES/messages.po  /usr/local/share/ice/locale/pt_PT/LC_MESSAGES/messages.po
	cp work/usr/share/ice/locale/sv/LC_MESSAGES/messages.po  /usr/local/share/ice/locale/sv/LC_MESSAGES/messages.po
	cp work/usr/share/ice/locale/zh_CN/LC_MESSAGES/messages.po  /usr/local/share/ice/locale/zh_CN/LC_MESSAGES/messages.po
	cp work/usr/share/ice/locale/messages.pot  /usr/local/share/ice/locale/messages.pot

.PHONY: remove
remove:
	rm -f /usr/local/bin/ice
	rm -f /usr/local/bin/ice-firefox
	rm -f /usr/local/share/applications/ice.desktop
	rm -f /usr/local/share/pixmaps/ice.png
	rm -rf /usr/local/lib/peppermint
	rm -rf /usr/local/share/ice

.PHONY: clean
clean:
	rm -rf ./work