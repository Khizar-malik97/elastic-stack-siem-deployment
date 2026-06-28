# Elastic Stack (ELK) SIEM Deployment Guide

A complete, hands-on deployment of the Elastic Stack — **Elasticsearch, Kibana, and Logstash** — as a single-node SIEM on Ubuntu Server, following Elastic's official Debian/APT installation path from start to finish.

📄 **[Read the full guide (PDF)](./Elasticsearch,logstash,kibana%20Deployment%20guide/Elastic_Stack_SIEM_Deployment_Guide.pdf)**

---

## Overview

This lab documents every stage of standing up the Elastic Stack on a single Linux host:

- Importing Elastic's GPG signing key and adding the official APT repository
- Installing Elasticsearch, Kibana, and Logstash
- Configuring `elasticsearch.yml` and `kibana.yml` for network access
- Starting and verifying each service through `systemd`
- Generating an enrollment token and connecting Kibana to Elasticsearch
- First login and full stack verification via the Kibana dashboard

Every command is documented with its purpose, and every step is backed by a screenshot from the actual deployment — no steps skipped or simplified.

## Lab Environment

| | |
|---|---|
| **Operating System** | Ubuntu Server (APT-based) |
| **Elasticsearch Version** | 9.4.2 |
| **Companion Services** | Kibana 9.4.2, Logstash |
| **Kibana Web Port** | 5601 |
| **Elasticsearch API Port** | 9200 |

## Why This Project

Centralized logging and search are at the core of almost every SIEM platform. This deployment builds the foundational layer — ingestion, indexing, and visualization — that detection rules, alerts, and dashboards are eventually built on top of. It follows the same installation pattern used in real production and SOC environments running on Linux servers, rather than a quickstart or containerized shortcut.

This project follows an earlier deployment of **[Wazuh](https://github.com/Khizar-malik97/wazuh-siem-deployment)** as part of an ongoing home SOC lab, with the goal of building hands-on, demonstrable experience across multiple SIEM platforms ahead of SOC Analyst / Junior Security Engineer roles.

## Next Steps

- Configure Logstash pipelines to ingest real log sources (syslog, Beats, application logs)
- Install Elastic Agent / Beats on additional endpoints for multi-host log centralization
- Build detection rules and dashboards using Kibana's Security and Observability solutions
- Replace self-signed TLS certificates with CA-signed certificates for production use

---

**Author:** Khizar Ul Islam (Malik)
BS Software Engineering — SZABIST Islamabad | CEH Certified
[LinkedIn](https://linkedin.com/in/khizarulislam79) · [GitHub](https://github.com/Khizar-malik97)
