REBAR3_TEMPLATE_DIR = ~/.config/rebar3/templates

TEMPLATE_FILES = $(wildcard *.template)
TEMPLATES = $(basename $(TEMPLATE_FILES))

define install_template
@echo Installing template $(1)
$(RM) -f $(REBAR3_TEMPLATE_DIR)/$(1)
ln -s $(CURDIR)/$(1) $(REBAR3_TEMPLATE_DIR)/$(1)
$(RM) -f $(REBAR3_TEMPLATE_DIR)/$(1).template
ln -s $(CURDIR)/$(1).template $(REBAR3_TEMPLATE_DIR)/$(1).template

endef

install: $(TEMPLATES)
	mkdir -p $(REBAR3_TEMPLATE_DIR)
	$(foreach template,$(TEMPLATES),$(call install_template,$(template)))

.PHONY: install
