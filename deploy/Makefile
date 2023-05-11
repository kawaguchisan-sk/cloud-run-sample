.PHONY: apply

# TODO: set appropriate value
PROJECT_ID := "xxx"
REGION := "xxx"

# apply
# usage: $ make apply
apply:
	gcloud deploy apply \
		--file=deploy.yaml \
		--region=$(REGION) \
		--project=kawaguchisan-dev
