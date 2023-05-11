.PHONY: $BUILD_TARGETS $DEPLOY_TARGETS

# TODO: set appropriate value
ARTIFACT_REGISTRY := "asia-northeast1-docker.pkg.dev/xxx/hello-world"
REGION := "asia-northeast1"

BUILD_TARGETS := build-v1 build-v2
DEPLOY_TARGETS := deploy-v1 deploy-v2

# build
# usage: $ make build-v1
$(BUILD_TARGETS): build-%:
	skaffold build \
		--default-repo $(ARTIFACT_REGISTRY) \
		--filename "skaffold_$*.yaml" \
		--file-output "build_$*.json"

# deploy
# usage: $ make deploy-v1 RELEASE=v1
$(DEPLOY_TARGETS): deploy-%:
	gcloud deploy releases create $(RELEASE) \
		--delivery-pipeline "hello-world" \
		--region $(REGION) \
		--build-artifacts "build_$*.json" \
		--skaffold-file "skaffold_$*.yaml" \
		--source .
