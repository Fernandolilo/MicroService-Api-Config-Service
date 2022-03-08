Api configuration service;

https://cloud.spring.io/spring-cloud-config/multi/multi__spring_cloud_config_server.html

serviço de cloud para prover apliações spring boot, seja profiles nativos ou em nuvem como é o github, 

seja em um repositorio publico ou privado.

se passar o paramentro: 

http://localhost:8888/application-dev/default   teremos o resultado:

{
"name": "application-dev",
"profiles": [
"default"
],
"label": null,
"version": null,
"state": null,
"propertySources": [
{
"name": "classpath:/config/application-dev.yml",
"source": {
"spring.application.name": "greeting-service",
"management.endpoints.web.exposure.include[0]": "*",
"greeting-service.greeting": "Hello",
"greeting-service.default-value": "Word"
}
}
]
}
------------------------------------------------------------------------------
http://localhost:8888/greeting-service/prod

{
"name": "greeting-service",
"profiles": [
"prod"
],
"label": null,
"version": null,
"state": null,
"propertySources": [
{
"name": "classpath:/config/application-prod.yml",
"source": {
"spring.application.name": "greeting-service",
"management.endpoints.web.exposure.include[0]": "*",
"greeting-service.greeting": "Ciao",
"greeting-service.default-value": "Mondo"
}
}
]
}
--------------------------------------------------------------------------
http://localhost:8888/greeting-service/perf

{
"name": "greeting-service",
"profiles": [
"perf"
],
"label": null,
"version": null,
"state": null,
"propertySources": [
{
"name": "classpath:/config/application-perf.yml",
"source": {
"spring.application.name": "greeting-service",
"management.endpoints.web.exposure.include[0]": "*",
"greeting-service.greeting": "Hola",
"greeting-service.default-value": "Mundo"
}
}
]
}

-------------------------------------------------------------------
http://localhost:8888/greeting-service/qa

{
"name": "greeting-service",
"profiles": [
"qa"
],
"label": null,
"version": null,
"state": null,
"propertySources": [
{
"name": "classpath:/config/application-qa.yml",
"source": {
"spring.application.name": "greeting-service",
"management.endpoints.web.exposure.include[0]": "*",
"greeting-service.greeting": "Olá",
"greeting-service.default-value": "Mundo"
}
}
]
}

