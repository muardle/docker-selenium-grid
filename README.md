# Docker Selenium Grid

Instantiate Selenium Grid with Docker Compose.

## Usage

### Starting Selenium Grid

Start Selenium Grid as follows:

```bash
docker-compose up -d
```

### Scaling up

Start Selenium Grid with additional nodes as follows:

```bash
docker-compose up -d --scale chrome=NUMBER_OF_NODES --scale firefox=NUMBER_OF_NODES
```

### Viewing and debugging

Start Selenium Grid with VNC support as follows:

```bash
docker-compose -f docker-compose.yml -f docker-compose.debug.yml up -d
```

List Docker containers as follows:

```bash
docker container ls
```

Use VNC to connect to `http://localhost:NODE_PORT` to view and debug test execution.

When prompted for a password the default is `secret`.

### Executing tests

Confirm Selenium Grid is up and running and the specified nodes are registered with the hub by visiting `http://localhost:4444/grid/console`.

Tests can then be executed by pointing them at `http://localhost:4444/wd/hub`.

### Stopping Selenium Grid

Stop Selenium Grid as follows:

```bash
docker-compose down
```

## License

The code in this repository, unless otherwise noted, is MIT licensed. See the `LICENSE` file in this repository.
