# chefs-to-object-store-docs

This Repository contains a Cron Job(HELM chart), which can be deployed to a k8s/openshift namespace, to move documents
from CHEFS bucket to desired object store bucket on a configured schedule.

## What is it?

It is a cron job written in node.js to move documents from CHEFS to object store bucket.

## Why do you need it?

Currently, it is not possible to provide your own bucket to store documents on submission of CHEFS form, which makes it
difficult for business to manage documents . This cron job will help you to move documents from CHEFS bucket to your own
bucket on a configured schedule and on a folder structure based on business specific requirements.

## How does it work?
It can be deployed to a k8s/openshift namespace as a cron job. It will run on a configured schedule and move documents based on the mapper.yaml provided which is mounted as a config map.

## What are the benefits?
1. No need to create an API just for moving documents
2. No need to manually move documents
3. No need to sustain a separate repository for moving documents
4. Helm chart, so upgrades are breeze.

## Pre-requisites
1. Object Store Bucket configured
2. API Keys for Chefs Form

