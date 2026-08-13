---
draft: false
title: "Testcontainers Modules"
date: 2025-07-17
publishdate: 2025-07-17
lastmod: 2026-08-13
weight: 7
---

## Introduction

As introduced in our [Developing with Testcontainers](/documentation/guides/usage/developing-testcontainers) guide, you can be embed Microcks into your unit tests with the help of [Testcontainers](https://testcontainers.com) librairies. We provide support for the following languages in dedicated Testcontainers modules: [Java](https://github.com/microcks/microcks-testcontainers-java), [NodeJS / Typescript](https://github.com/microcks/microcks-testcontainers-node), [Golang](https://github.com/microcks/microcks-testcontainers-go) and [.NET](https://github.com/microcks/microcks-testcontainers-dotnet).

We try to setup and manage a unified roadmap between modules but because they are maintained by different contributors, drifts between implementations may happen at some points. Our goal is obviously to make them consistent eventually. 

This page lists the implementation status of various features by the different modules on July 21st, 2025. It will be updated regularly. 

> 💡 Of course, **we welcome external contributions**! So, if you're in a hurry and need a missing feature, don't hesitate to propose a change and to submit a _Pull Request_ on the associated GitHub repository 🙏

## Initialization

This section lists the features related to Microcks initialization during the preparation of setup phase of tests.

| Feature                  | Java  | JS   | Go   | .NET |
| ------------------------ | ----- | ---- | ---- | ---- |
| Secret creation          | ✅    | ✅   | ✅   | ✅   |
| Snapshot restoration     | ✅    | ✅   | ✅   | ✅   |
| Local files (primary)    | ✅    | ✅   | ✅   | ✅   |
| Local files (secondary)  | ✅    | ✅   | ✅   | ✅   |
| Remote urls (primary)    | ✅    | ✅   | ✅   | ✅   |
| Remote urls (secondary)  | ✅    | ✅   | ✅   | ✅   |
| Remote urls with Secret  | ✅    | ✅   | ✅   | ✅   |


## Mocking features

This sections lists the features related to the mocking part of Microcks (getting endpoints, checking invocations).

| Feature                       | Java  | JS   | Go   | .NET |
| ----------------------------- | ----- | ---- | ---- | ---- |
| REST endpoints                | ✅    | ✅   | ✅   | ✅   |
| Soap endpoints                | ✅    | ✅   | ✅   | ✅   |
| GraphQL endpoints             | ✅    | ✅   | ✅   | ✅   |
| gRPC endpoints                | ✅    | ✅   | ✅   | ✅   |
| Invocation verification       | ✅    | ✅   | ✅   | ✅   |
| Get invocation stats          | ✅    | ✅   | ✅   | ✅   |
| Webhook callback registration | ✅    | ❌   | ✅   | ❌   |

## Testing features

This sections lists the features related to the testing part of Microcks (executing conformance tests, checking responses/messages).

| Feature               | Java  | JS   | Go   | .NET |
| --------------------- | ----- | ---- | ---- | ---- |
| OpenAPI conformance   | ✅    | ✅   | ✅   | ✅   |
| Soap conformance      | ✅    | ✅   | ✅   | ✅   |
| GraphQL conformance   | ✅    | ✅   | ✅   | ✅   |
| gRPC conformance      | ✅    | ✅   | ✅   | ✅   |
| Postman conformance   | ✅    | ✅   | ✅   | ✅   |
| AsyncAPI conformance  | ✅    | ✅   | ✅   | ✅   |
| Get TestCase messages | ✅    | ✅   | ✅   | ✅   |

## Asynchronous protocols

This sections lists the async protocols available on each language binding.

| Protocol            | Java  | JS   | Go   | .NET |
| ------------------- | ----- | ---- | ---- | ---- |
| Kafka               | ✅    | ✅   | ✅   | ✅   |
| WebSocket           | ✅    | ✅   | ❌   | ✅   |
| MQTT                | ✅    | ✅   | ✅   | ❌   |
| RabbitMQ (AMQP 0.9) | ✅    | ✅   | ✅   | ✅   |
| NATS                | ❌    | ❌   | ❌   | ❌   |
| AWS SQS             | ✅    | ✅   | ✅   | ❌   |
| AWS SNS             | ✅    | ✅   | ✅   | ❌   |
| Google PubSub       | ✅    | ✅   | ✅   | ❌   |
