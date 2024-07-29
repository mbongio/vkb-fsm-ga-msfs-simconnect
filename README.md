# MSFS VKB Dual THQ + SEM + FSM-GA Combo Connector

This repo contains example code for syncing the LEDs of 
VKB's GNX Dual THQ + SEM + FMS-GA Combo with MSFS via SimConnect.
This is a fork of the repo from LeeTrout that was focused on the FSM-GA only.

## Usage

### Setup 

Install Python 3.

Clone or download this repo.

Inside this repo directory create a virtual environment:

```powershell
python -m venv venv
```

Activate the virtual environment:

```powershell
.\venv\Scripts\activate
```

Install the dependencies
```powershell
pip install -r requirements.txt
```

### Perform a self test

```powershell
python main.py test
```

### Start the sync

```powershell
python main.py
```

## Dev notes

### Sync update loop

The sync update loop checks the state of the sim using SimConnect.

Each LED ID has an update function that receives the instance of the
SimConnect AircraftRequests with which it is responsible for setting
the LED to the correct state. This results in more verbose code but
more flexibility and easy readability.



