# ntu-ce10-2.14

- Does SNS guarantee exactly once delivery to subscribers?
Amazon SNS guarantees at-least-once delivery for HTTP/S endpoints, email, SMS, and mobile push notifications. However, for Amazon SQS and AWS Lambda subscribers, SNS can provide exactly-once delivery when using FIFO topics.

- What is the purpose of the Dead-letter Queue (DLQ)?
A Dead-letter Queue (DLQ) is a special queue that stores messages that could not be processed successfully. It helps prevent message loss, enables debugging, and allows for reprocessing of failed messages.

- How would you enable a notification to your email when messages are added to the DLQ?
You can set up an Amazon CloudWatch Alarm on the DLQ's ApproximateNumberOfMessagesVisible metric. When the queue is not empty, the alarm triggers an Amazon SNS topic, which sends an email notification.

