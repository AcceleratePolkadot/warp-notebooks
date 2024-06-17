## Install Homebrew
Run the following command and follow the instructions in your terminal\. Restart your terminal once done\.
```warp-runnable-command
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
Ensure homebrew is at latest version
```warp-runnable-command
brew update
```
## Instal dependencies
If your machine is running Apple silicon protobuf must be installed before the build process can begin\.
```warp-runnable-command
brew install protobuf
```
```warp-runnable-command
brew install openssl
```
```warp-runnable-command
brew install cmake
```
## Install Rust
```warp-runnable-command
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```
```warp-runnable-command
source ~/.cargo/env
```
```warp-runnable-command
rustup default stable
rustup update
rustup target add wasm32-unknown-unknown
```
```warp-runnable-command
rustup update nightly
rustup target add wasm32-unknown-unknown --toolchain nightly
```
## Compile and run node in dev mode
```warp-runnable-command
git clone https://github.com/substrate-developer-hub/substrate-node-template
cd substrate-node-template
```
```warp-runnable-command
cargo run --release -- --dev
```
