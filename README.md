# OnPremise-POSTGRESQL

If you want to run Devaten-OnPremise-Dashboard and On-Premise-POSTGRESQL Agent Separately, for that we are providing [Devaten-OnPremise-Dashboard](https://github.com/devatengit/Devaten-OnPremise-Dashboard) and [OnPremise-POSTGRESQL](https://github.com/devatengit/OnPremise-POSTGRESQL) Agent files separately.

For that run [Deveten-OnPremise-Dashboard](https://github.com/devatengit/Devaten-OnPremise-Dashboard). Once its up and runnig minimize the Command Prompt. 

Now open OnPremise-POSTGRESQL Docker Compose file. In ```environment:``` there is an ActiveMQ URL to conncet On-Premise Dashboard. In URL replace the ```127.0.0.1```:61616 with your systems IP Address. 

- spring.activemq.broker-url=tcp://```IP_ADDRESS```:61616

Once the change is done ```save``` the file. 

Open cmd at that location where docker-compose.yml exists and run the following commands:
```
docker compose pull
```
to pull image locally
```
docker compose up
```
to run the image/container exist in docker compose file.

Once it run successfully you'll get ``` Agent Unique ID ``` which is useful when you are going to add ```Agent```.
