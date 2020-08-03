# TFTP Server

TFTP server implementation, using Python's 'socket' library as the only networking interface. The server implements the [RFC 1350](https://tools.ietf.org/html/rfc1350) TFTP Protocol (except _mail_ mode). It was written as an introduction to networking and communication protocols.


## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

1. Fork this repository
2. Clone your fork of the repository
3. Create a Python 3.7 virtual environment: `python3.7 -m venv env`
4. Set the Python environment: `source env/bin/activate`
5. Start the server: `sudo python tftp_server.py`

### Usage

The server will read/write files to the current working directory. Be careful not to run the server in a directory with sensitive files as TFTP has no security, except:

* It can't read or write outside of the current working directory
* It won't overwrite files
* It won't create directories
