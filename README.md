# CamelK-customerAPI

Camel K lets you build and deploy your API on Kubernetes or Red Hat OpenShift in less than a second. 

### Run command
```sh
kamel run customer-api.xml \
    --open-api customer-api.json \
    --name customers \
    --dependency camel-undertow \
    --dependency camel-rest \
    --property camel.rest.port=8080 \
    --dev
```

### Read the tutorial at: 

https://developers.redhat.com/blog/2019/04/25/build-and-deploy-an-api-with-camel-k-on-red-hat-openshift/

### Learn how in this video:

[![Everything Is AWESOME](images/CamelK_YoutubeVideo.png)](http://www.youtube.com/watch?v=WE8K6872w1U "How to build and deploy an API with Camel K on OpenShift")
