ManyWho Service Name
====================

[![Build Status](https://travis-ci.org/manywho/service-twilio.svg?branch=develop)](https://travis-ci.org/manywho/service-twilio)


This service allows you to integrate your flows with --introduce functionality description here--.

## Usage

The latest tagged version of this service will always be deployed to our shared services platform, which is 
accessible at https://services.manywho.com/api/{url of the service}.

If you need to run your own instance of the service (e.g. for compliance reasons), it's easy to spin up following these
instructions:

#### Building

To build the service, you will need --dependencies-- (e.g. to have Apache Ant, Maven 3, Java 8, etc).

You will need to generate a configuration file for the service by running the provided `build.xml` script with Ant, passing in valid values for --description of the parameters--:

```bash
$ ant -DparamName=paramValue /
```

Now you can build the runnable shaded JAR:

```bash
$ mvn clean package
```

#### Running

The service is a Jersey JAX-RS application, that by default is run under the Grizzly2 server on port 8080 (if you use 
the packaged JAR).

##### Defaults

Running the following command will start the service listening on `0.0.0.0:8080/api/{introduce here path for api}`:

```bash
$ java -jar target/{service name}-1.0-SNAPSHOT.jar
```

##### Custom Port

You can specify a custom port to run the service on by passing the `server.port` property when running the JAR. The
following command will start the service listening on port 9090 (`0.0.0.0:9090/api/**{introduce here path for api}**`):

```bash
$ java -Dserver.port=9090 -jar target/{service name}-1.0-SNAPSHOT.jar
```

## Contributing

Contributions are welcome to the project - whether they are feature requests, improvements or bug fixes! Refer to 
[CONTRIBUTING.md](CONTRIBUTING.md) for our contribution requirements.

## License

This service is released under the [MIT License](http://opensource.org/licenses/mit-license.php).
