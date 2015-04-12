# Isso (comments engine) using Docker

First run the website - [https://github.com/oren/test-website](https://github.com/oren/test-website)

    git clone git@github.com:oren/test-isso.git
    cd test-isso
    sudo cp -p isso.conf /srv/isso/
    docker build -t isso:latest .
    docker run -d -p 8080:8080 --name isso -v /srv/isso/:/opt/isso -v /srv/issodb/:/opt/issodb isso:latest

To test it go to: [http://localhost:8080/demo](http://localhost:8080/demo).

