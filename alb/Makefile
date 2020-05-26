package:
	aws cloudformation package \
	--template-file ./main.template.yml \
	--s3-bucket aws-sam-cli-managed-default-samclisourcebucket-1k8g6cex8e00g \
	--output-template-file ./packaged.template.yaml

deploy: package
	aws cloudformation deploy \
	--template-file ./packaged.template.yaml \
	--stack-name test-alb-asg \
	--parameter-overrides SSHKeyName=EU_IRL_TEST_KEYS \
	--capabilities CAPABILITY_AUTO_EXPAND

