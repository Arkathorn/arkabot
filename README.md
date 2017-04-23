# ArkaBot
Arkabot is an experimental Discord bot with a variety of features, almost none of which exist yet.

## Usage
Airhorn Bot has two components, a bot client that handles the playing of loyal arkabots, and a web server that implements OAuth2 and stats. Once added to your server, arkabot bot cannot be summoned by running `!arkabot`.


### Running the Bot

**First install the bot:**
```
go get github.com/arkathorn/arkabot/cmd/bot
go install github.com/arkathorn/arkabot/cmd/bot
```
 **Then run the following command:**

```
bot -r "localhost:6379" -t "MY_BOT_ACCOUNT_TOKEN" -o OWNER_ID
```

### Running the Web Server
First install the webserver: `go install github.com/arkathorn/arkabot`, then run `make static`, finally run:

```
./arkabotweb -r "localhost:6379" -i MY_APPLICATION_ID -s 'MY_APPLICATION_SECRET"
```

Note, the webserver requires a redis instance to track statistics

## Thanks
Arkabot was/is initially a clone of Airhorn bot (https://github.com/hammerandchisel/airhornbot).