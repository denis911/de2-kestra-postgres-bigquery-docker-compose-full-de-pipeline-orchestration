# de2-kestra-postgres-bigquery-docker-compose-full-de-pipeline-orchestration

Use Kestra to orchestrate data engineering pipelines with local setup using Docker compose

## Installing Kestra

To install Kestra, we are going to use Docker Compose. We already have a Postgres database set up, along with pgAdmin from Module 1. We can continue to use these with Kestra but we'll need to make a few modifications to our Docker Compose file.

Use this example Docker Compose file to correctly add the 2 new services and set up the volumes correctly.

Add information about setting a username and password.

We'll set up Kestra using Docker Compose containing one container for the Kestra server and another for the Postgres database:

'''bash
cd 02-workflow-orchestration
docker compose up -d
'''

Note: Check that pgAdmin isn't running on the same ports as Kestra. If so, check out the FAQ at the bottom of the README.

Once the container starts, you can access the Kestra UI at http://localhost:8080.

To shut down Kestra, go to the same directory and run the following command:

docker compose down
Add Flows to Kestra
Flows can be added to Kestra by copying and pasting the YAML directly into the editor, or by adding via Kestra's API. See below for adding programmatically.

Add Flows to Kestra programmatically

