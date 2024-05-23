# Habitica Party Up!

## Overview

Habitica Party Up! is a Go-based application that automates the process of inviting users to a Habitica party. This application fetches users looking for a party every 2 minutes and sends them an invitation automatically.

## Features

- Fetches users looking for a Habitica party.
- Invites users to a Habitica party every 2 minutes.
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
go run main.go -api-user your-api-user -api-key your-api-key
```

### Example

```sh
go run main.go -api-user 12345678-90ab-cdef-1234-567890abcdef -api-key 12345678-90ab-cdef-1234-567890abcdef
```

## Configuration

You can configure the application using command-line flags. The following configuration options are available:

- `api-user`: Your Habitica API user ID.
- `api-key`: Your Habitica API key.

### Using Command-Line Flags

Pass the API user and key as command-line arguments:

```sh
go run main.go -api-user your-api-user -api-key your-api-key
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