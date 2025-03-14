# Migrate

migrate is a wrapper around the <a href="https://github.com/pressly/goose">goose</a> migration tool for managing database migrations in Go applications. This package provides a straightforward interface for applying, rolling back, and managing migrations using a specified database dialect.

## Installation

```zsh
go get github.com/gosuit/migrate
```

## Features

• Apply Migrations: Easily apply all pending migrations to the specified database.

• Rollback Migrations: Roll back the most recent migration or revert to a specific version.

• Dialect Support: Supports various database dialects through the goose library.

## Usage

```golang
package main

import (
    "database/sql"
    "log"

    "github.com/gosuit/migrate"
)

func main() {
    db, err := <init sql.DB>

    err = migrate.Migrate(db, migrate.Postgres, "./migrations")
    if err != nil {
        log.Fatalf("failed to apply migrations: %v", err)
    }
}
```

## Contributing

Contributions are welcome! Please feel free to submit a pull request or open an issue for any enhancements or bug fixes.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
