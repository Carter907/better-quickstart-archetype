# Maven Archetype - Updated Template

This repository contains an updated Maven archetype designed to streamline project creation using the `mvn archetype:generate` goal. It provides a modern, customizable project template for Java developers.

## Overview
Maven archetypes are project templates that allow you to generate consistent project structures. This updated archetype simplifies the creation of new Maven projects with:
- Modern configurations
- Predefined dependencies and plugins
- Support for best practices and clean project organization

### Features
- **Up-to-Date Dependencies**: Preconfigured dependencies compatible with the latest Java and Maven versions
- **Flexible Customization**: Prompts for groupId, artifactId, package, and version
- **Clean Project Structure**: Follows Maven's standard directory layout
- **Best Practices**: Includes `src/main`, `src/test`, and other essentials for a Maven project

---

## Installation
To install the Maven archetype locally, clone this repository and run:

```bash
git clone https://github.com/<your-repo>/updated-maven-archetype.git
cd updated-maven-archetype
mvn clean install
```

---

## Usage
To generate a new project using this archetype, run the following command:

```bash
mvn archetype:generate \
    -DarchetypeGroupId=com.example \
    -DarchetypeArtifactId=better-maven-archetype \
    -DarchetypeVersion=1.0.0 \
    -DgroupId=com.mycompany.app \
    -DartifactId=my-app \
    -Dversion=1.0.0-SNAPSHOT
```

Replace the parameters as follows:
- **archetypeGroupId**: The groupId of the archetype
- **archetypeArtifactId**: The artifactId of the archetype
- **archetypeVersion**: The version of the archetype
- **groupId**: Your project's groupId
- **artifactId**: Your project's artifactId
- **version**: Your project's version

### Resulting Project Structure
The generated project will have the following structure:

```plaintext
my-app/
├── pom.xml                  # Project configuration file
└── src/
    ├── main/
    │   ├── java/            # Application source code
    │   └── resources/       # Configuration and assets
    └── test/
        ├── java/            # Test source code
        └── resources/       # Test assets
```

---

## Customizing the Archetype
You can update the archetype by modifying the files in:
- `src/main/resources/archetype-resources` - Template files for the generated project
- `archetype-metadata.xml` - Metadata for customization and filtering

Reinstall the archetype after making changes:

```bash
mvn clean install
```

---

