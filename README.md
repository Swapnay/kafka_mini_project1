

## Getting Started

**Step 1:** Make sure git is installed on your os. I will be using macOS for the project.

On macOS, you can install the git using Homebrew using ```brew install git```

**Step 2:** Clone the project into your local machine using below command.

```git clone https://github.com/Swapnay/kafka_mini_project1.git```

### Prerequisites

**1. Docker**

Make sure you have Docker installed. Please follow the below link for official documentation from Docker to install latest version of docker on your os. For this project I am using Docker CE (18.09).

```https://docs.docker.com/docker-for-mac/install/```

### Installing

**Step 1:** Change to the directory where the project was cloned in previous step.

```
cd kafka_mini_project1
```

**Step 2:** Make sure Docker is up and running. You can start the docker engine from desktop icon on Mac.

**Step 3:** Run

```
 docker network create kafka-network
docker-compose -f docker-compose.kafka.yml -d up --build
```
Access logs
```
docker-compose -f docker-compose.kafka.yml logs broker
```

To run generator and detector
```
 docker-compose up

```

**Step 4:** Another terminal window check legit transactions on console
    ```
    docker-compose -f docker-compose.kafka.yml exec broker kafka-console-consumer
    --bootstrap-server localhost:9092 --topic streaming.transactions.legit
    ```
    
    Look at fraud transactions 

    ```
    docker-compose -f docker-compose.kafka.yml exec broker kafka-console-consumer
    --bootstrap-server localhost:9092 --topic streaming.transactions.fraud

    ```    

## Running the tests

## Deployment

## Built With

* [Docker](http://www.dropwizard.io/1.0.2/docs/) -  Deployment model
* [Python](https://rometools.github.io/rome/) - programming language
* [pip](https://rometools.github.io/rome/) - Package and dependency manager


## Contributing

## Versioning

## Authors

## License

## Acknowledgments
