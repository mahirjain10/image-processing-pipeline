# image-processing-service

NestJS backend for the image processing pipeline.

Handles image uploads via HTTP, JWT-based auth, job creation in PostgreSQL,
and dispatches jobs to RabbitMQ queues for Go workers to consume. Receives
completion callbacks from AWS SNS via the `/webhook/sns` endpoint and updates
job status in the database.

Run via Docker Compose from the repo root. See the root README for setup instructions.
