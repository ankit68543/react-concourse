To run the CI follow below commands.
Note: Make sure Concourse and Fly is already running in your machine.

  fly -t react-app login -c http://localhost:8080 -u test -p test
  fly -t react-app set-pipeline -p react-hello-world -c ci/pipeline.yml
  fly -t react-app unpause-pipeline -p react-hello-world
  fly -t react-app trigger-job --job  react-hello-world/test --watch

  #Happy Learning