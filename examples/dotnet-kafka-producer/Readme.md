# .Net Kafka Producer
A REST API that uses the Confluent Kafka nuget package to produce messages.

## Install

[Download .Net core 3.1](https://dotnet.microsoft.com/en-us/download/dotnet/3.1)

## Usage

Open in visual studio or run with:
```dotnet run --project KafkaProducer```

Send a message by calling the applications REST API. Either import the postman collection in this repo or use the following commands.
```sh
curl http://localhost:9000/message -H "Content-Type: application/json" --data '{"message": "Message"}'
```

powershell:
```sh
Invoke-RestMethod -Uri 'http://localhost:9000/message' -Method Post -Headers @{"Content-Type" = "application/json"} -Body "{`"message`": `"test2`"}"
```

Send an async message:

```sh
curl -s  http://localhost:9000/message/async \
-H "Content-Type: application/json" \
--data '{"message": "Message"}'
```

```sh
Invoke-RestMethod -Uri 'http://localhost:9000/message/async' -Method Post -Headers @{"Content-Type" = "application/json"} -Body "{`"message`": `"test2`"}"
```