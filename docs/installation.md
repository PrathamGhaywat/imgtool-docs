# Installation

### Windows
Install the release from [here](https://github.com/PrathamGhaywat/imgtool/releases). Then add the folder in which the executable is present in your `PATH` environment variable.

### Linux and macOS
We are currently searching for a way to make the tool available for Linux and macOS. Please open an issue if you have any suggestions.
If you would still like to use the tool on Linux and macOS, you can [build](#build) it from the source.

## Build
To build the tool from the source, you'll need to have Go installed.

```bash
# Clone the repository
git clone https://github.com/PrathamGhaywat/imgtool.git
cd imgtool

# Download dependencies
go mod tidy

# Build the executable
go build -o imgtool.exe .
```