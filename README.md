# Jasmine with Karma runner
Minimal Docker container to run [Jasmine](https://jasmine.github.io/) tests with [Karma runner](https://github.com/karma-runner/karma) using PhantomJS/Chrome

### Prerequsite
- Docker is installed

### Quickstart
1. Change directory to your project's root where source and test code (with Karma config) live
2. Spin up Karma server
    - `docker run -d -p 9876:9876 -v $PWD:/src -w /src --name karma yamaszone/jasmine-karma:latest start`
    - Access Karma server from browser visiting http://<HOST_IP>:9876
3. Use Karma runner
    - `docker exec karma-server karma run` # run tests
    - `docker exec karma-server karma --help` # see Karma help

