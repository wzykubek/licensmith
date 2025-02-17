# Licensmith

Licensmith, a streamlined tool, allows you to create an `LICENSE` file for your Git repository
with ease, using just one command. This tool is designed to save you time and effort.

[![Go Reference](https://pkg.go.dev/badge/go.wzykubek.xyz/licensmith.svg)](https://pkg.go.dev/go.wzykubek.xyz/licensmith)

---

## Usage

For example if you want to generate an ISC `LICENSE` file with the current year and your name,
run the following command:

```bash
licensmith add ISC
```

By default, Licensmith read user details from your local Git repository (name and email). 
As a fallback it uses global Git configuration.

You can customize this process by providing specific values using the following command:

```bash
licensmith add ISC --name "John Doe" --email "jdoe@example.com"
```

To view available templates, run the following command:

```bash
licensmith list
```

To display a license summary, use:

```bash
licensmith show ISC
```

## Installation

Licensmith can be installed using various methods.

### From Source

This is universal method to build a binary for any system and architecture. 
You need to have Go installed.

```bash
git clone https://github.com/wzykubek/licensmith
cd licensmith
# This command will create dist directory with compiled binary and generated shell completions.
make
```

On Linux distributions you can also install it to `/usr/local` with ease.

```bash
sudo make install
```

### Arch Linux

Package is available in [Arch User Repository](https://aur.archlinux.org/packages/licensmith).

#### Using AUR helper

```bash
# paru
paru -S licensmith

# yay
yay -S licensmith
```

#### Manually

```bash
git clone https://github.com/wzykubek/licensmith
cd licensmith
makepkg -si
```

### Go Registry

You can install this package using `go install`. 
Ensure `$GOPATH/bin` is in your `$PATH` variable.
```bash
go install go.wzykubek.xyz/licensmith@latest
```

## License

This project is licensed under ISC license.
