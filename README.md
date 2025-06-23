# Fraud-Detector
This will consume transactions and apply simple rules. This simply logs the alerts for our MVP.

## Running the MVP
1. Start Kafka: docker-compose up -d.
2. Start your fraud-detector application.
3. Start your transaction-simulator (if you built one) OR use a tool like Postman/curl to send a Transaction JSON object to an endpoint that produces messages, OR use a command-line producer tool.
4. Send some transactions, including some with amounts > $5000.
5. Watch the console logs of your fraud-detector application. You should see "Processing Transaction..." and, for high amounts, "ALERT!" and the "FRAUD ALERT RECEIVED" logs.
6. Check Kafka UI (http://localhost:8080) to see messages in both topics.
