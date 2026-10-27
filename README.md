# Shopify Catalogue Translator

> This repository serves as a public technical overview of the project.
>
> The source code remains private because it contains application logic, AI integrations, and implementation details used in a deployed Shopify application.
>
> This README documents the system architecture, translation workflows, and technical implementation at a high level.

---

## Overview

A Shopify application designed to automate product catalogue translation and simplify multilingual storefront management.

The system integrates with Shopify's authentication and API infrastructure to process existing catalogue resources, generate AI-powered translations, and apply localized content to supported Shopify resources.

The application is built around a web-based interface, backend translation workflows, AI provider integrations, and persistent application data.

---

## Highlights

- AI-powered catalogue translation
- Shopify OAuth authentication
- Shopify Admin API integration
- Product title translation
- Product description translation
- Collection translation
- Translation job management
- Configurable AI model integration
- Multilingual catalogue localization
- Containerized application deployment

---

## Business Problem

Expanding an e-commerce store into additional markets requires product information to be available in multiple languages.

For merchants managing large Shopify catalogues, manual translation can become time-consuming and difficult to maintain consistently.

Without an automated workflow:

- Product titles and descriptions require repetitive manual work.
- Collection content must be localized separately.
- Large catalogues become increasingly difficult to manage.
- Translation workflows consume time that could be spent on other business activities.
- Maintaining consistent localized content becomes more challenging as a store grows.

This application was designed to simplify these challenges through AI-assisted catalogue translation integrated with Shopify.

---

## Core Capabilities

### Product Catalogue Translation

The application processes existing Shopify product resources and supports translation of product content into selected target languages.

Supported content includes:

- Product titles
- Product descriptions

The workflow is designed to localize existing catalogue content without requiring merchants to recreate their products.

---

### Collection Translation

The application supports collection translation as part of the catalogue localization workflow.

This helps merchants maintain localized collection content alongside translated product information.

---

### AI-Powered Translation

The application integrates AI models to generate translated catalogue content.

Translation requests are handled through the application's backend workflows, allowing generated content to be processed and submitted to Shopify.

The configured AI provider and model determine the translation service used by the application.

---

## Shopify Integration

The application communicates with Shopify through its authentication and API infrastructure.

### OAuth Authentication

Shopify OAuth provides the authorization flow required to connect a merchant's store to the application.

Access to Shopify resources is governed by the permissions granted to the application.

### Shopify Admin API

The application uses Shopify API operations to access supported catalogue resources and apply translated content.

This integration allows the translation workflow to operate directly on the merchant's existing Shopify catalogue.

### Translation Submission

After translation content has been generated, the application processes the corresponding Shopify translation workflow to submit localized content for supported resources.

---

## Translation Workflow

The general translation workflow consists of the following stages:

1. The merchant connects their Shopify store.
2. The merchant selects supported catalogue resources and target languages.
3. The application retrieves the relevant source content.
4. The backend submits translation requests to the configured AI provider.
5. The generated translations are processed by the application.
6. The application submits translated content to Shopify.
7. Translation jobs are managed through the application interface.

The exact workflow depends on the resource types and options supported by the application.

---

## Application Architecture

The application uses a containerized web application architecture with separate frontend, backend, and database services.

### Frontend

Responsible for the application interface and merchant interactions, including translation configuration and job management.

### Backend

Responsible for application logic, translation orchestration, Shopify API communication, and integration with the configured AI provider.

### Database

Provides persistent storage for application data and the state required by the application workflows.

### AI Integration

Connects the application to an AI translation provider to generate localized catalogue content.

---

## Project Structure

The application is organized into separate frontend and backend components, with deployment configuration maintained alongside the application code.

### Frontend

Provides the user interface for configuring and managing catalogue translation workflows.

### Backend

Handles Shopify integration, application logic, translation processing, and communication with external services.

### Database Layer

Supports persistent application data and the state needed by the translation workflows.

### Deployment Configuration

Docker and Docker Compose configuration define the application's containerized deployment.

---

## Technology Stack

### Application

- TypeScript
- JavaScript
- Node.js

### Integrations

- Shopify OAuth
- Shopify Admin API
- AI translation APIs

### Data Storage

- PostgreSQL

### Infrastructure

- Docker
- Docker Compose
- Linux
- HTTPS reverse proxy

---

## Security Considerations

The application connects to Shopify through an authorization flow and uses credentials to communicate with external services.

Sensitive configuration values, including API keys, access tokens, and database credentials, should be maintained outside version-controlled source code.

Shopify access is limited by the permissions granted to the application.

---

## Scalability Considerations

The application separates frontend, backend, and database responsibilities to support independent application components.

AI-powered translation workflows also provide a foundation for improving catalogue localization processes as merchants manage larger product collections.

Potential areas for further optimization include translation request management, processing efficiency, and handling larger catalogues.

---

## Future Improvements

Potential areas for further development include:

- Additional AI translation providers
- Expanded Shopify resource support
- Enhanced translation job monitoring
- Translation quality validation
- Improved handling of large catalogues
- Additional localization controls
- More advanced translation workflow management

---

## Status

The application is deployed and available through its live endpoint.

The source code remains private. This repository provides a public technical overview of the application's architecture, integrations, and approach to AI-powered Shopify catalogue localization.

Designed and developed as a custom Shopify application for multilingual catalogue management.
