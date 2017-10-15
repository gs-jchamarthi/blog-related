- example application with some bootstrapping (spring security, JDBC auto configuration, h2 console, actuator endpoints, vaadin view discovery) to keep the application busy during startup. this way, we can better see the impact of our optimizations.

# TODO

- analyze dev tools

# Some Commands 

Build and Run

```bash
./mvnw clean package && java -jar target/development-productivity-vaadin-spring-boot*.jar
```

Search in created archives

```bash
unzip -l target/development-productivity-vaadin-spring-boot*.jar | grep css 
```

Compile Vaadin Theme

```bash
./mvnw vaadin:compile-theme 
```

# notes

- the `styles.css` are not found in the jar if we put the theme in the webapp folder (instead of resources), but it somehow works...
- vaadin on-the-fly sass compilation only works if we put the themes under `webapp` instead of `resources`