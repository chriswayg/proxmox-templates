
BASEDIR:=$(shell dab basedir)

all: info/init_ok
	dab bootstrap --minimal
	dab install psmisc python
	dab exec apt-get -y purge postfix
	sed -e 's/^PermitRootLogin without-password/PermitRootLogin yes/' -i ${BASEDIR}/etc/ssh/sshd_config
	dab finalize

info/init_ok: dab.conf
	dab init
	touch $@

.PHONY: clean
clean:
	dab clean
	rm -f *~

.PHONY: dist-clean
dist-clean:
	dab dist-clean
	rm -f *~

