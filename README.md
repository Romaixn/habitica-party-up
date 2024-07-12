# Habitica Party Up!

## Overview

Habitica Party Up! is a Go-based application that automates the process of inviting users to a Habitica party. This application fetches users looking for a party based on an interval and sends them an invitation automatically.

## Features

- Fetches users looking for a Habitica party.
- Invites users to a Habitica party on an interval.
- Configurable API user and API key via environment variables or command-line flags.

## Prerequisites

- Go 1.22 or later
- Habitica account with appropriate API credentials

## Installation

1. **Clone the repository**

   ```sh
   git clone https://github.com/Romaixn/habitica-party-up.git
   cd habitica-party-up
   ```

2. **Install dependencies**

   This project uses `github.com/jasonlvhit/gocron` for scheduling tasks.

   ```sh
   go get -u github.com/jasonlvhit/gocron
   ```

## Usage

### Run the application with command-line flags

```sh
./habitica-party-up -api-user your-api-user -api-key your-api-key
```

### Example

```sh
./habitica-party-up -api-user 12345678-90ab-cdef-1234-567890abcdef -api-key 12345678-90ab-cdef-1234-567890abcdef -min-lvl 10 -language en -only-active true
```

## Configuration

You can configure the application using command-line flags. The following configuration options are available:

- `api-user`: Your Habitica API user ID.
- `api-key`: Your Habitica API key.
- `min-lvl`: Min level of users to invite to party. Default to 0 (invite everybody).
- `fetch-interval`: Interval for fetching users in seconds. Default is 120 (2 minutes).
- `language`: Language of users to invite to party. Default is all languages (can be something like "fr" / "en" / "zh", etc.).
- `only-active`: Only invite active users to party, based on an algorithm. Default is false.

### Using Command-Line Flags

Pass the API user and key as command-line arguments:

```sh
./habitica-party-up -api-user your-api-user -api-key your-api-key
```

## Code Structure

- `main.go`: The main file containing the application logic, including fetching users and inviting them to a party.

## Contributing

Contributions are welcome! Please feel free to submit a pull request or open an issue on GitHub.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgements

- [Habitica](https://habitica.com) for providing the API and platform.
- [gocron](https://github.com/jasonlvhit/gocron) for the scheduling library.
