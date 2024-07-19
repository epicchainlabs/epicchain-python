

Overview
--------

What EpicChain Offers

- **Alternative Implementation**: EpicChain serves as an advanced implementation of blockchain technology, designed to support the evolving needs of modern applications.
- **Node Functionality**: Operate a Python-based P2P node for interacting with the blockchain network.
- **Interactive CLI**: Configure nodes and inspect blockchain status with a comprehensive command-line interface.
- **Smart Contracts**: Compile, test, deploy, and execute smart contracts written in various programming languages, including Python. Supports smart contracts in the `.avm` format.
- **Wallet Functionality**: Basic wallet functionalities (still under development and not yet recommended for mainnet use).
- **Compliance**: Supports NEP2, NEP5, NEP-7, and NEP-8 standards for seamless token and contract management.
- **RPC Services**: Includes RPC client and server for communication and data exchange.
- **Notification Server**: View real-time transfers of NEP5 tokens with integrated notification services.
- **Event Monitoring**: Track `Runtime.Log` and `Runtime.Notify` events for comprehensive monitoring.

Future Capabilities

- **Consensus Nodes**: Enhancing the network with robust consensus nodes.
- **Smart Contract Debugging**: Advanced tools for debugging and inspecting smart contracts.

Documentation

The full documentation on how to install, configure, and use EpicChain is available at `Read The Docs <https://epicchain.readthedocs.io/en/latest/>`.

Get Help or Contribute

- **Report Issues**: Open a new `issue <https://github.com/EpicChain/epicchain/issues/new>`_ if you encounter problems.
- **Community Support**: Connect with us on the `EpicChain Discord <https://discord.gg/EpicChain>`_ for support and community interaction.
- **Contributions**: Pull requests are welcome! Check the issue list for ideas on how you can contribute, from enhancing wallet features to writing tests and documentation.

Getting Started
---------------

**EpicChain** has two system dependencies (all other dependencies are covered with `pip`):

- `LevelDB <https://github.com/google/leveldb>`_
- `Python 3.7 <https://www.python.org/downloads/release/python-373/>`_ (Python 3.6 and below are not supported)

We have a Youtube `video <https://www.youtube.com/watch?v=ZZXz261AXrM>`_ to help you get started. More tutorials are available on the `EpicChain Youtube channel <https://www.youtube.com/channel/UCzlQUNLrRa8qJkz40G91iJg>`_.

Docker
------

For a streamlined setup, use Docker to run EpicChain. Example Dockerfiles are available in the `/docker` folder <https://github.com/EpicChain/epicchain/tree/development/docker>, and an image is available on Docker Hub, tagged after EpicChain releases: https://hub.docker.com/r/epicchain/epicchain/

Native Installation
-------------------

**LevelDB Installation:**

- **OSX:**

  ::

      brew install leveldb

- **Ubuntu/Debian 18.04+:**

  Instructions for installing Python `3.7.3` or newer on Ubuntu are detailed in `this Ubuntu guide <https://linuxize.com/post/how-to-install-python-3-7-on-ubuntu-18-04/>`.

- **CentOS/RedHat/Fedora:**

  Follow `this CentOS guide <https://tecadmin.net/install-python-3-7-on-centos/>`_ for Python `3.7.3` installation.

- **Windows:**

  For Windows users, it's recommended to use the Linux subsystem with Ubuntu or a Virtual Machine. Set up the Linux subsystem with `Ubuntu 18.04` from the Microsoft Store here: https://www.microsoft.com/en-us/p/ubuntu-1804/9n9tngvndl3q?activetab=pivot%3aoverviewtab. More details are available `here <https://medium.com/@gubanotorious/installing-and-running-epicchain-on-windows-10-284fb518b213>`_.

**Python 3.7+ Compatibility**

EpicChain is compatible with **Python 3.7 and later**. Install it via your package manager or download it from the `official homepage <https://www.python.org/downloads/>`_.

Installation Steps
~~~~~~~~~~~~~~~~~~

It's recommended to use a virtual environment to manage project dependencies and avoid conflicts.

1. **Install from GitHub:**

  ::

    git clone https://github.com/EpicChain/epicchain.git
    cd epicchain

    # Switch to development branch if needed
    git checkout development

    # Create and activate virtual environment using Python 3.7
    python3.7 -m venv venv
    source venv/bin/activate

    # Install the package
    (venv) pip install wheel -e .

2. **Install from PyPi:**

  ::

    mkdir myproject
    cd myproject

    # Create and activate virtual environment using Python 3.7
    python3.7 -m venv venv
    source venv/bin/activate

    (venv) pip install wheel epicchain

Running EpicChain
-----------------

After installation and environment activation, use the CLI (`epic-prompt`) to start the node and interact with it.

::

    epic-prompt
    EpicChain CLI. Type 'help' to get started

    epic> show state
    Progress: 10926 / 11145
    Block-cache length 0
    Blocks since program start 0
    Time elapsed 0.02598465 mins
    Blocks per min 0
    TPS: 0

    epic>

Query for blockchain data by block hash or index:

::

    epic-prompt
    EpicChain CLI. Type 'help' to get started

    epic> show block 122235
    {
        "hash": "0xf9d7bc6f337a6cbe124b92b90ad7b29e2628e78202ea2daa19ed93fdc779c0e6",
        "size": 686,
        "version": 0,
        "previousblockhash": "0x1f262a0979d6da0eabaaf54252fb2508564a99fee642a77ff0773671fe5fddb9",
        "merkleroot": "0x5d4f86734c2a53187aa96751b9180d69f85f9bd7875f2eb83a27666ad052ea1e",
        "time": 1496920870,
        "index": 122235,
        "nonce": "7847dea9df7571c1",
        "nextconsensus": "AdyQbbn6ENjqWDa5JNYMwN3ikNcA4JeZdk",
        "script": {
            "invocation": "40e5a7d23cb065308412d769ca2ba6dd974aa453d0c915c25a7d951488eaa6c4eff5bbe251f01725b959fb89e7dd631f7f41efd50897c466d75e8359154f6137bf402f690a98a44e5ecb22e7f20bb75bac40cac89f4805f4706ec9daf8e6ccc15def216d667423bb148e78db9461e288d7363f699741a0efb4c7c6c6dc902250cf3f4023ba2eb464aa8841cb2230c0f9f016a47c1e54e1f809da550743c33b0529b5996f4c5993a38bb73887e0b3fd7a093f6abd00d136048169a99cf34373560b8956408e816d0a0b018c348070da63f513b5b3332


            "verification": "55210209e7fd41dfb5c2f8dc72eb30358ac100ea8c72da18847befe06eade68cebfcb9210327da12b5c40200e9f65569476bbff2218da4f32548ff43b6387ec1416a231ee821034ff5ceeac41acf22cd5ed2da17a6df4dd8358fcb2bfb1a43208ad0feaab2746b21026ce35b29147ad09e4afe4ec4a7319095f08198fa8babbe3c56e970b143528d2221038dddc06ce687677a53d54f096d2591ba2302068cf123c1f2d75c2dddc542557921039dafd8571a641058ccc832c5e2111ea39b09c0bde36050914384f7a48bce9bf92102d02b1873a0863cd042cc717da31cea0d7cf9db32b74d4c72c01b0011503e2e2257ae"
        },
        "tx": [
            {
                "txid": "0x5d4f86734c2a53187aa96751b9180d69f85f9bd7875f2eb83a27666ad052ea1e",
                "size": 10,
                "type": "MinerTransaction",
                "version": 0,
                "attributes": [],
                "vout": [],
                "vin": [],
                "sys_fee": "0",
                "net_fee": "0",
                "scripts": [],
                "nonce": 3749016001
            }
        ]
    }
    epic>

Bootstrapping the Blockchain
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

If you use epicchain-python for the first time, you need to synchronize the
blockchain, which may take a long time. Included in this project is the script
``np-bootstrap`` to automatically download a chain directory for you.

np-bootstrap Usage
^^^^^^^^^^^^^^^^^^

::

    $ np-bootstrap -h
    usage: np-bootstrap [-h] [-m] [-c CONFIG] [-n] [-s] [--datadir DATADIR]

    optional arguments:
      -h, --help            show this help message and exit
      -m, --mainnet         use MainNet instead of the default TestNet
      -c CONFIG, --config CONFIG
                            Use a specific config file
      -n, --notifications   Bootstrap notification database
      -s, --skipconfirm     Bypass warning about overwriting data in Chains
      -k, --keep-bootstrap-file
                            Keep the downloaded bootstrap file
      --datadir DATADIR     Absolute path to use for database directories

Bootrapping Testnet
^^^^^^^^^^^^^^^^^^^

To bootstrap the testnet blockchain, run ``np-bootstrap``, get a cup of coffee
and wait. Then, bootstrap the testnet notifications database with ``np-bootstrap -n``.

Bootstrapping Mainnet
^^^^^^^^^^^^^^^^^^^^^

To bootstrap the mainnet blockchain, run ``np-bootstrap -m`` and get 8 cups of coffee
(9+ GB file). Then, bootstrap the mainnet notifications database with
``np-bootstrap -m -n``.

Basic Wallet commands
~~~~~~~~~~~~~~~~~~~~~

::

    wallet create {wallet_path}
    wallet open {wallet_path}
    wallet close

    wallet (verbose)
    wallet rebuild (start block)

    wallet import wif {wif}
    wallet export wif {address}

    wallet send {args}       # (EpicChain/EpicPulse)
    wallet token send {args} # XEP5


For a complete list of commands use ``help``.

Running on MainNet
~~~~~~~~~~~~~~~~~~

To run the prompt on MainNet, you can use the CLI argument ``-m`` (eg.
``np-prompt -m``), for running on PrivNet you can use ``-p``. Be
sure to check out the details of the parameters:

::

    $ np-prompt -h
    usage: np-prompt [-h] [-m | -p [host] | --coznet | -c CONFIG]
                     [-t {dark,light}] [-v] [--datadir DATADIR] [--version]

    optional arguments:
      -h, --help            show this help message and exit
      -m, --mainnet         Use MainNet instead of the default TestNet
      -p [host], --privnet [host]
                            Use a private net instead of the default TestNet,
                            optionally using a custom host (default: 127.0.0.1)
      --coznet              Use the CoZ network instead of the default TestNet
      -c CONFIG, --config CONFIG
                            Use a specific config file
      -t {dark,light}, --set-default-theme {dark,light}
                            Set the default theme to be loaded from the config
                            file. Default: 'dark'
      -v, --verbose         Show smart-contract events by default
      --datadir DATADIR     Absolute path to use for database directories
      --maxpeers MAXPEERS   Max peers to use for P2P Joining
      --version             show program's version number and exit

Logging
~~~~~~~

Currently, ``np-prompt`` logs to ``prompt.log``


Tests
-----

Note we make use of a Blockchain fixture database (~15 MB). This file is not kept in the repo,
but is downloaded the first time the tests are run, this can take some time (depending on the internet connection),
but happens only once.

Useful commands
---------------

::

    make lint
    make test
    make coverage
    make docs


    # run only epicchain-python tests
    python -m unittest discover epicchain

    # run only epicchain-boa tests
    python -m unittest discover boa_test

Updating the version number and releasing new versions of epicchain-python
--------------------------------------------------------------------

This is a checklist for releasing a new version, which for now means:

1. Merging the changes from development into master
2. Setting the version from eg. ``0.4.6-dev`` to ``0.4.6`` (which
   automatically created a tag/release)
3. On the dev branch, setting the version to the next patch, eg.
   ``0.4.7-dev``
4. Pushing master, development and the tags to GitHub

Make sure you are on the development branch and have all changes merged
that you want to publish. Then follow these steps:

::

    # Only in case you want to increase the version number again (eg. scope changed from patch to minor):
    # bumpversion --no-tag minor|major

    # Update CHANGELOG.rst: make sure all changes are there and remove `-dev` from the version number
    vi CHANGELOG.rst
    git commit -m "Updated changelog for release" CHANGELOG.rst

    # Merge development branch into master
    git checkout master
    git merge development

    # Set the release version number and create the tag
    bumpversion release

    # Switch back into the development branch
    git checkout development

    # Increase patch number and add `-dev`
    bumpversion --no-tag patch

    # Push to GitHub, which also updates the PyPI package and Docker Hub image
    git push origin master development --tags

Troubleshooting
---------------

If you run into problems, check these things before ripping out your
hair:

-  Double-check that you are using Python 3.7.x
-  Update the project dependencies (``pip install -e .``)
-  If you encounter any problems, please take a look at the
   `installation
   section <https://epicchain-python.readthedocs.io/en/latest/install.html#further-install-notes>`_
   in the docs, and if that doesn't help open an issue. We'll try to
   help.
-  You can reach us on the `EpicChain Discord <https://discord.gg/R8v48YA>`_,
   or simply file a `GitHub
   issue <https://github.com/epicchainlabs/epicchain-python/issues/new>`_.

License
-------

-  Open-source
   `MIT <https://github.com/epicchainlabs/epicchain-python/blob/master/LICENSE.md>`_.
-  Contributors: `@localhuman <https://github.com/localhuman>`_ (Creator), `@metachris <https://github.com/metachris>`_, `@ixje <https://github.com/ixje>`_, and `many more <https://github.com/epicchainlabs/epicchain-python/graphs/contributors>`_

Donations
---------

Accepted at **ATEMNPSjRVvsXmaJW4ZYJBSVuJ6uR2mjQU**
