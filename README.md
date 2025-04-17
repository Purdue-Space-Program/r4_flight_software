# Rocket 4 (Copperhead) Flight Software

## Development Environment

### Dependencies

#### Debian/Ubuntu
```
curl -LsSf https://astral.sh/uv/install.sh | sh
```

```
sudo apt install --no-install-recommends git cmake ninja-build gperf \
  ccache dfu-util device-tree-compiler wget python3-dev python3-pip  \
  python3-setuptools python3-tk python3-wheel xz-utils file make gcc \
  gcc-multilib g++-multilib libsdl2-dev libmagic1
```

#### macOS
```
curl -LsSf https://astral.sh/uv/install.sh | sh
```

```
brew install cmake ninja gperf python3 python-tk ccache qemu dtc libmagic wget openocd
```

### Installation
1. Clone the repo:
	1. `west init -m https://github.com/Purdue-Space-Program/r4_flight_software copperhead_fsw`
2. Initialize Zephyr modules
	1. `cd copperhead_fsw`/r4_flight_software
	2. `west update`
3. Initialize UV environment
	1. `uv sync`
	2. `source .venv/bin/activate`
4. Build and flash
	1. `west build`
	2. `west flash`

