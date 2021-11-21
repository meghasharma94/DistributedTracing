# DistributedTracing
This is a POC for distributed tracing and contains multiple microservices
Zipkin is a distributed tracing system. It helps gather timing data needed to troubleshoot latency problems in service architectures. It is a visualization of your request-response and trace it. ELK stack is used for distributed logging. The Zipkin server gives a visual aid of your request-response and timing details, while Kibaana in ELK gives a visual aid for centralized logging - somewhere where you can read the logs 


when the Orchestrator Service makes a HTTP call on the service , the call is intercepted by Sleuth and it adds the necessary tags to the request headers. After the Orchestrator Service receives the HTTP response, the data is sent asynchronously to Zipkin to prevent delays or failures relating to the tracing system from delaying or breaking the flow.

Sleuth adds two types of IDs to the log file, one called a trace ID and the other called a span ID. The span ID represents a basic unit of work, for example sending an HTTP request. The trace ID contains a set of span IDs, forming a tree-like structure. The trace ID will remain the same as one microservice calls the next.

Install Zipkin  and ELK stack and start all the three microservces .

Start all the services :

Application : Port 

Logstash : 9600
Kibana: 5601
ElasticSearch : 9200
Zipkin : 9411


Microservices running at : 
M1 : 8081
M2 : 8082
M3 : 8083


