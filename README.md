# ft_irc

ft_irc is a fully functional IRC server project from the 42 curriculum. It is written in **C++** and demonstrates networking, multithreading, and client-server communication according to the IRC protocol (RFC 1459).

## Features

* Handles multiple client connections concurrently
* Implements core IRC commands: `NICK`, `USER`, `JOIN`, `PART`, `PRIVMSG`, `NOTICE`, `QUIT`
* Channel management with operator privileges
* Private messages between users
* Logging of server events
* Robust error handling and client disconnection management

## Installation

1. Clone the repo:

   ```bash
   git clone https://github.com/TemsamaniHamza/ft_irc.git
   ```

2. Go into the repo:

   ```bash
   cd ft_irc
   ```

3. Compile:

   ```bash
   make
   ```

## Usage

Run the server with a port number:

```bash
./ircserv <port> <password>
```

Connect with an IRC client or `telnet` to test:

```bash
telnet localhost <port>
```

**Commands Examples:**

* `NICK mynickname`
* `USER myusername 0 * :Real Name`
* `JOIN #channel`
* `PRIVMSG #channel :Hello everyone`

## How I Worked

* Designed and implemented the server architecture using C++ classes
* Managed multiple clients using `select()` and non-blocking sockets
* Implemented IRC command parsing according to RFC 1459
* Handled edge cases like nickname conflicts, invalid commands, and channel restrictions
* Tested extensively with multiple clients to ensure stability and concurrency

## Technologies

* C++
* Sockets and networking
* `select()` for multiplexing
* RFC 1459 IRC protocol compliance
