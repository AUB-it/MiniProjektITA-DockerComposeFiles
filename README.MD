NOGLE SERVICES BRUGER FÆLLES DOCKER NETVÆRK  
derfor kør kommandoen  
´´´
docker network create external-backend
´´´
  
USER OG AUTH SERVICE:  
skal bruge VAULT med path = auth og JWT_SECRET = <noget>  
Dette bliver slettet efter hvert genstart af VAULT container 

USER OG AUTH SERVICE:
skal gå igennem nginx med http://localhost:4000/userservices <> http://localhost:4000/authservices  
*Kan ses i nginx.config i UserDockerCompose mappen*


VAULT, MONGODB, AUTHSERVICE, USERSERVICE  
kører allesammen på fælles docker netværk.


GRAFANA  
Login  
User = admin  
Password = admin  

Connect til Loki med = htt://loki:3100/