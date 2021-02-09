# sendemail-docker
A simple container to send an email to a smtp server

Container requires the following arguments in this order: To From Subject "Body" Server.
Optionally you can supply a user, password and additional arguments to sendEmail.

Examples:

- docker run ghcr.io/nirmata/sendemail fooo@nirmata.com junkmail@nirmata.com "Hey" "Important infomation!" smtp.nirmata.com

- docker run ghcr.io/nirmata/sendemail foo@nirmata.com junkmail@nirmata.com "Hey" "Important infomation!" smtp.nirmata.com sam.silbory '$vaqqpgq!znnnn'

- docker run ghcr.io/nirmata/sendemail foo@nirmata.com junkmail@nirmata.com "Hey" "Important infomation!" smtp.gmail.com:587 sam '$vaqmqpgq!znnnn' 

Note that to use gmail in the above example you need to create an app password for gmail.


If you want to run the container with a shell you'll need to escape the entry point script.

docker run -it --entrypoint bash ghcr.io/nirmata/sendemail
