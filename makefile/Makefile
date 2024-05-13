MEX_DESCRIPTION="This provides some additional tools for this project."
MEX_LICENSE="Released under the BSD two-clause license, see the LICENSE file for more information."
#MEX_ASSURE="date ls tree php"
MEX_ASSURE="date ls tree"
MEX_ENVIRONMENT="dev.env second.env"

include makext.mk

help: .help

print-env:  # print env
	@echo "Environment variables"
	@echo "  HOME: $(HOME)"
	@echo "  TERM: $(TERM)"
	@echo "  ENV: $(MEX_ENVIRONMENT)"
	@echo "  AWS_BUCKET: $(AWS_BUCKET)"
	@echo "  DB_HOST: $(DB_HOST)"

clean-cache: # Clean the cache
	@echo "1. Cleaning the cache..."

build-app: .assure print-env clean-cache # Build the application
	@echo "2. Building the application..."

run-tests: build-app # Running the tests
	@echo "3. Running tests..."

deploy-dev: run-tests # Deploy app to dev
	@echo "4. Deploying applications to dev..."

deploy-stg: run-tests # Deploy app to staging
	@echo "4. Deploying applications to staging..."

deploy-prod: run-tests # Deploy app to production
	@echo "4. Deploying applications to production..."
