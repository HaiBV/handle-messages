
## About The Project

### Problem Description

You are tasked with writing a function that processes a list of JSON-formatted messages sent by chargers. Each message contains three fields: `id` (the session ID), `type` (message type), and `time` (timestamp). The charger sends three types of messages: `SessionStart`, `StatusCharging`, and `SessionStop`

### Input

You will receive a list of JSON messages, where each message contains:

* `id`: a string representing the session ID.
* `type`: one of three message types (`SessionStart`, `SessionStop`, `StatusCharging`).
* `time`: an integer timestamp when the message was sent.

### Output

The function should return a dictionary with the following keys:

* `num_distinct_sessions`: an integer representing the number of distinct sessions.
* `longest_session_id`: a string containing the ID of the longest session.
* `longest_duration`: an integer representing the duration of the longest session.
* `smallest_session_id`: a string containing the ID of the smallest session.
* `smallest_duration`: an integer representing the duration of the smallest session.
* `bad_sessions`: a list of strings containing the IDs of bad sessions.

### Constraints and Rules

* There will be at least one message in the input.
* Timestamps will be positive integers.
* You can assume that the input will not contain malformed messages.
* Message with the same SessionID belong the the same charging session
* It is possible for messages with later timestamp arrives at AmpUp backend later than messages with earlier timestamp
* A normal session should generate messages `SessionStart`, `StatusCharging` and `SessionStop` in chronological order, at least they should generate `SessionStart` and `SessionStop` message for one charging session. Otherwise, they are considered bad sessions

### Built With

* Vite (VanillaJS)

### Installation

1. Clone the repo

   ```sh
   git clone https://github.com/HaiBV/handle-messages.git
   ```

2. Install NPM packages

   ```sh
   npm install
   ```

## Usage

Run test

```sh
npm run test
```
