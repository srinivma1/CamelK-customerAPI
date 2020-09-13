# CamelK-customerAPI

Camel K lets you build and deploy your API on Kubernetes or Red Hat OpenShift in less than a second. 

### Run on Minishift
```sh
oc login -u system:admin
kamel install --cluster-setup

oc login -u developer -p x
oc new-project demo
kamel install

kamel run customer-api.xml \
    --open-api customer-api.json \
    --name customers \
    --dependency camel-undertow \
    --dependency camel-rest \
    --logging-level org.apache.camel.k=DEBUG \
    --property camel.rest.port=8080 \
    --env CAMEL_LOG_MSG=" ** Camelk ** This request is handled by this POD: {{env:HOSTNAME}}" \
    --env CAMEL_GET_SETBODY=" Customer retrieved successfully \n" \
    --env CAMEL_CREATE_SETBODY=" Customer created successfully \n"

curl http://customers-demo.$(minishift ip).nip.io/camel/customer
```

### Read the tutorial at: 

https://developers.redhat.com/blog/2019/04/25/build-and-deploy-an-api-with-camel-k-on-red-hat-openshift/

### Learn how in this video:

[![Everything Is AWESOME](images/CamelK_YoutubeVideo.png)](http://www.youtube.com/watch?v=WE8K6872w1U "How to build and deploy an API with Camel K on OpenShift")
