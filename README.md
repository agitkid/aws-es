# Setup AWS Elasticsearch cluster with kopf

## Create ec2 cluster in cloudformation:

aws cloudformation create-stack --stack-name aws-es-cb --template-body file:///local/path/to/aws-cloudformation-es.json --capabilities CAPABILITY_IAM

## Use ansible to deploy the config:

ansible-playbook main.yml -i inventory.ini --private-key ~/.ssh/my_private_key.pem

Elasticsearch cluster:

http://52.33.94.161:9200/_plugin/kopf/#!/nodes
