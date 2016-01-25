fruity-cli
==
A simple Command Line Interface (CLI) for talking to [fruitymesh](https://github.com/mwaylabs/fruitymesh) devices.

1. Node it up
--
Clone this repo and install the dependencies:

```
git clone https://github.com/microcosm/fruity-cli.git
cd fruity-cli
npm install
```

2. Connect the CLI
--
- Plug the nRF51 device into your USB port, unplugging any other nRF51 devices
- In the console, run `node cli`

This command will attempt to open a serial connection to the device via the USB port. The device should be discovered automatically, since you only have one plugged in. If it isn't, you will be prompted to run `node list` to find your USB port name.

You should give this a whirl anyway so you know how to do it:

- If you are still in the CLI, use ctrl-X to close out of it
- Use `node list` to get a list of available USB ports
- Find the USB port name listed alongside the manufacturer 'SEGGER'
- Fire up the CLI again, this time specifying the USB port name:

```
node cli /dev/cu.usbmodemfa131
```

- You should see this:

![The CLI is running](/img/node-cli.png)

It may be followed by a bunch of 'mhTerm' console output - that's fine. This 'mhTerm' thing is the fruitymesh terminal. The CLI will spit out whatever it says, as well as send it whatever you type.
