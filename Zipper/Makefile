NAME ?= Dark-Ages


DATE := $(shell date "+%d%m%Y-%I%M")

CODE := Segundo

ZIP := $(NAME)-$(CODE)-$(DATE).zip
CZIP := $(NAME)-$(CODE)-Clang-$(DATE).zip
TZIP := $(NAME)-$(CODE)-Treble-$(DATE).zip
CTZIP := $(NAME)-$(CODE)-Treble-Clang-$(DATE).zip
MZIP := $(NAME)-$(CODE)-MIUI-$(DATE).zip
CMZIP := $(NAME)-$(CODE)-MIUI-Clang-$(DATE).zip
EXCLUDE := Makefile *.git* *.jar* Dark-Ages*

normal: $(ZIP)
nclang: $(CZIP)
treble: $(TZIP)
tclang: $(CTZIP)
miui: $(MZIP)
mclang: $(CMZIP)

$(ZIP):
	@echo "Creating ZIP: $(ZIP)"
	@zip -r9 "$@" . -x $(EXCLUDE)
	@echo "Generating SHA1..."
	@sha1sum "$@" > "$@.sha1"
	@cat "$@.sha1"
	@echo "Done."

$(TZIP):
	@echo "Creating ZIP: $(TZIP)"
	@zip -r9 "$@" . -x $(EXCLUDE)
	@echo "Generating SHA1..."
	@sha1sum "$@" > "$@.sha1"
	@cat "$@.sha1"
	@echo "Done."

$(CZIP):
	@echo "Creating ZIP: $(CZIP)"
	@zip -r9 "$@" . -x $(EXCLUDE)
	@echo "Generating SHA1..."
	@sha1sum "$@" > "$@.sha1"
	@cat "$@.sha1"
	@echo "Done."

$(CTZIP):
	@echo "Creating ZIP: $(CTZIP)"
	@zip -r9 "$@" . -x $(EXCLUDE)
	@echo "Generating SHA1..."
	@sha1sum "$@" > "$@.sha1"
	@cat "$@.sha1"
	@echo "Done."
	
$(MZIP):
	@echo "Creating ZIP: $(MZIP)"	@zip -r9 "$@" . -x $(EXCLUDE)
	@echo "Generating SHA1..."
	@sha1sum "$@" > "$@.sha1"
	@cat "$@.sha1"
	@echo "Done."

$(CMZIP):
	@echo "Creating ZIP: $(CMZIP)"
	@zip -r9 "$@" . -x $(EXCLUDE)
	@echo "Generating SHA1..."
	@sha1sum "$@" > "$@.sha1"
	@cat "$@.sha1"
	@echo "Done."


clean:
	@rm -vf "$(NAME)-"*.zip*
	@rm -vf boot/zImage
	@echo "Done."


