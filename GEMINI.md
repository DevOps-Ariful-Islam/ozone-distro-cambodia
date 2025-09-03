# Project Overview

This repository contains the source code for Ozone for Cambodia (Ozone Kh), a distribution of the Ozone Health Information System (HIS) specifically configured for the Ministry of Health of Cambodia. It is an integrated system that includes an NCD-capable Electronic Medical Record (EMR) system and a reporting and analytics platform for NCD population reporting.

The project is built using Java and Maven, and it leverages several open-source technologies, including OpenMRS and Superset.

The `base` directory contains the core configuration for the Ozone distribution, including OpenMRS and Superset settings.

# Building and Running

## Building the Project

To build the project, run the following command from the root directory:

```bash
scripts/mvnw clean package -P prod
```

This command will download the necessary dependencies, compile the source code, and package the application.

## Running the Project

To run the project, use the following command:

```bash
source base/target/go-to-scripts-dir.sh && ./start-demo.sh
```

This will start the Ozone Kh application. You can then access it in your browser at the URL provided in the console output.

# Development Conventions

## Code Style

The project follows the standard Java coding conventions.

## Testing

The project uses JUnit for unit testing.

## Configuration

The project's configuration is located in the `base/configs` directory. This directory contains subdirectories for OpenMRS and Superset.

### OpenMRS Configuration

The OpenMRS configuration is located in the `base/configs/openmrs` directory. This directory contains the following subdirectories:

*   `frontend_assembly`: Contains configuration for the OpenMRS Single Page Application (SPA).
*   `frontend_config`: Contains frontend configuration for Ozone, including translations and UI component settings.
*   `initializer_config`: Contains various configuration files for OpenMRS, including address hierarchy, concepts, drugs, encounter types, locations, patient identifier types, person attribute types, privileges, roles, and visit types. These files are mostly in CSV and XML formats.

### Superset Configuration

The Superset configuration is located in the `base/configs/superset` directory. This directory contains dashboards and charts in YAML format.

## Contribution Guidelines

Contributions to the project are welcome. Please follow the standard GitHub flow of forking the repository, creating a new branch for your changes, and submitting a pull request.