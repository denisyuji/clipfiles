# clipfiles #

## Overview ##

`clipfiles` is a simple shell script that copies the content of files from a specified directory (or the current directory if none is provided) to the clipboard. It is useful for quickly capturing file contents without manually opening and copying them.

## Features ##

- Copies the content of all non-hidden files (excluding README and LICENSE files) to the clipboard.

- Supports copying the content of a single file or all the files in a directory and its subdirectories

## Installation ##

To use `clipfiles`, simply download the script and make it executable:

```
chmod +x clipfiles
```

Ensure `xclip` is installed on your system:

```
sudo apt install xclip  # For Debian/Ubuntu
```

### Persistent Installation ###

To make `clipfiles` available system-wide, move it to `/usr/local/bin/`:

```
sudo mv clipfiles /usr/local/bin/
```

### Temporary Usage ###

To use `clipfiles` temporarily, add it to your `PATH`:

```
export PATH="$PATH:$(pwd)"
```

### Persistent Usage in Shell ###

To always have `clipfiles` available, add the following line to your `~/.bashrc` or `~/.bash_profile`:

```
echo 'export PATH="$PATH:$(pwd)"' >> ~/.bashrc
source ~/.bashrc
```

## Usage ##

```
./clipfiles [path]
```

- If `path` is a directory, it will copy the content of all non-hidden files (excluding `README` and `LICENSE` files).
- If `path` is a file, it will copy its content to the clipboard.
- If no `path` is provided, it defaults to the current directory.

### Options ###

- `--help` : Displays help information.
- `--version` : Shows the version of the script.

## Example ##

```
./clipfiles my_directory
```

This copies the content of all valid files in `my_directory` to the clipboard.

```
./clipfiles myfile.txt
```

This copies the content of `myfile.txt` to the clipboard.

## License ##

This project is licensed under the MIT License. See the `LICENSE` file for details.
