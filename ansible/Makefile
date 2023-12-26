PLAYBOOK ?= converge.yaml
INVENTORY ?= inventory/local.yaml
VAULT ?= inventory/local.vault.yaml
VAULT_PASSWORD_FILE ?=
ANSIBLE_EXTRA_ARGS ?= 

lint:
	ansible-lint
apply:
	ansible-playbook -i $(INVENTORY) -i $(VAULT) --vault-password-file=$(VAULT_PASSWORD_FILE) playbooks/$(PLAYBOOK) $(ANSIBLE_EXTRA_ARGS)
format:
	ansible-lint --write
