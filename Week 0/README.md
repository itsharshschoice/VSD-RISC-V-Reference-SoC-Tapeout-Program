# **Tool Installation** 

This week covers the setup of essential open-source tools required for RTL design, simulation, and waveform analysis.

We will install the following tools on **Ubuntu 24.04.3** (latest):  

- **Yosys** → Logic synthesis & optimization  
- **Icarus Verilog (iverilog)** → RTL simulation  
- **GTKWave** → Waveform visualization  

## **System Requirements**  

| Resource | Minimum Requirement |
|----------|----------------------|
| RAM      | 6 GB                |
| Storage  | 50 GB HDD/SSD       |
| CPU      | 4 vCPUs             |
| OS       | Ubuntu 20.04+       |


## **Installation Steps**

### (1). Install **Yosys** (Logic Synthesis)  

```bash
# Update packages
sudo apt-get update

# Clone Yosys repository
git clone https://github.com/YosysHQ/yosys.git
cd yosys

# Install dependencies
sudo apt-get install make build-essential clang bison flex \
   libreadline-dev gawk tcl-dev libffi-dev git graphviz xdot \
   pkg-config python3 libboost-system-dev libboost-python-dev \
   libboost-filesystem-dev zlib1g-dev -y

# Build and install
make config-gcc
make
sudo make install
```

**Verify installation**

```bash
yosys --version
```

![App Screenshot](https://github.com/itsharshschoice/VSD-RISC-V-Reference-SoC-Tapeout-Program/blob/main/Week%200/Images/yosys1.png?raw=true)

```bash
yosys
```  

![App Screenshot](https://github.com/itsharshschoice/VSD-RISC-V-Reference-SoC-Tapeout-Program/blob/main/Week%200/Images/yosys2.png?raw=true)

### (2️). Install **Icarus Verilog** (iverilog)

```bash
sudo apt-get update
sudo apt-get install iverilog -y
```

**Verify installation**

```bash
iverilog -v
```

![App Screenshot](https://github.com/itsharshschoice/VSD-RISC-V-Reference-SoC-Tapeout-Program/blob/main/Week%200/Images/iverilog.png?raw=true)

### (3️). Install **GTKWave**

```bash
sudo apt-get update
sudo apt-get install gtkwave -y
```


Verify installation:

```bash
gtkwave --version
```

![App Screenshot](https://github.com/itsharshschoice/VSD-RISC-V-Reference-SoC-Tapeout-Program/blob/main/Week%200/Images/gtkwave1.png?raw=true)

```bash
gtkwave
```

![App Screenshot](https://github.com/itsharshschoice/VSD-RISC-V-Reference-SoC-Tapeout-Program/blob/main/Week%200/Images/gtkwave2.png?raw=true)