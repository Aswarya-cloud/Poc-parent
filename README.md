# ARB Parent (POM)


## Overview

This project defines the parent POM for all modules in the system. It provides a centralized location for managing shared configurations such as:
- Plugin versions
- Java compiler settings
- Dependency management (via a BOM if applicable)
- Repository and distribution settings

Using this parent POM helps enforce consistency and reduce redundancy across all Maven modules.

## Features

- Unified build configuration for all child modules
- Centralized dependency and plugin version control
- Standardized compiler, encoding, and build settings
- Supports profiles for different environments (e.g., dev, prod)

## Technical Stack

- **Framework**: Maven
- **Artifactory**: JFrog
- **Parent Project** Springboot 3.4.5
- **Dependency Manager**: Maven 3.5.1


## Architecture

### Components

1. **ARB Parent**
    - Centralized version control for dependencies

2. **Infrastructure**
    - JFrog Artifactory

### How to Use

- To be able to microservice follow up the **Parent** you need to add it inside your `pom.xml`

```maven
	<parent>
		<groupId>com.arb</groupId>
		<artifactId>alrajhi-parent</artifactId>
		<version>0.0.1-SNAPSHOT</version>
		<relativePath/>
	</parent>
```

- If you have any change on the pom.xml you should deploy the change on the artifactory,to do it you can use the following command.

`mvn clean install deploy`