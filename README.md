<p align="center">
  <img src="https://img.shields.io/badge/License-MIT-blue.svg" alt="License: MIT">
  <a href="https://github.com/Smertig/banana/actions"><img src="https://github.com/Smertig/banana/workflows/Tagged%20Release/badge.svg" alt="GitHub Actions"></a>
  <a href="https://github.com/Smertig/banana/actions"><img src="https://github.com/Smertig/banana/workflows/Build%20On%20Push/badge.svg" alt="GitHub Actions"></a>
</p>

<p align="center">
  🍌 <b>banana</b> - thin wrapper over <a href="https://core.telegram.org/bots/api">Telegram Bot API</a> written in C++17.
</p>

## Key Features

 - Simple API
 - **Single interface for both blocking, non-blocking and even coroutine-based operations**
 - Generic in terms of networking backend (bundled support for [`WinAPI`](https://docs.microsoft.com/en-us/windows/win32/api/wininet/nf-wininet-httpsendrequesta), [`cpr`](https://github.com/whoshuu/cpr) and [`boost::beast`](https://github.com/boostorg/beast))
 - Extendable (see [custom-connector](https://github.com/Smertig/banana/blob/master/example/custom-connector-blocking.cpp) example)
 - Automatically generated from [Telegram Bot API](https://core.telegram.org/bots/api) 5.0
 - Cross-platform (tested on Windows, Linux, macOS)

## Example

```c++
#include <banana/api.hpp>
#include <banana/connector/default.hpp>

int main(int argc, char** argv) {
    banana::connector::default_blocking connector("<TG_BOT_TOKEN>")
    banana::api::send_message(connector, { "@smertig", "Hello, world!" });
}
```

## Documentation

[![Latest Release](https://img.shields.io/github/v/release/smertig/banana?label=Banana%20Docs)](https://smertig.github.io/banana/v0.1.0)

[![Master](https://img.shields.io/badge/Banana%20Docs-master-blue.svg)](https://smertig.github.io/banana/master)