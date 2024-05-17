# OpenSSH Vulnerability Checker

This repository contains a Python script to check if a given SSH server is running a vulnerable version of OpenSSH (versions prior to 9.3p2). This vulnerability could expose the server to certain types of attacks. The script uses the `paramiko` library to establish an SSH connection and retrieve the server version.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Example Output](#example-output)
- [Contributing](#contributing)
- [License](#license)

## Features

- Connects to an SSH server and retrieves the OpenSSH version.
- Compares the retrieved version with the secure version (9.3p2).
- Provides a warning if the server is running a vulnerable version of OpenSSH.

## Installation

To use this script, you need to have Python installed on your system. You also need to install the `paramiko` library, which can be done using `pip`.

1. Clone the repository:

```sh
git clone https://github.com/yourusername/openssh-vulnerability-checker.git
cd openssh-vulnerability-checker
```

2. Install the required dependencies:

```sh
pip install paramiko
```

## Usage

1. Run the script and enter the SSH server address and port when prompted. The default port is 22.

```sh
python check_openssh_vulnerability.py
```

2. You will be prompted to enter the SSH server address and the port (default is 22).

```plaintext
Enter the SSH server address: example.com
Enter the SSH server port (default 22): 22
```

3. The script will connect to the server, retrieve the OpenSSH version, and determine if it is vulnerable.

## Example Output

Here is an example of what the output might look like when running the script:

```plaintext
Enter the SSH server address: example.com
Enter the SSH server port (default 22): 22
SSH Banner: SSH-2.0-OpenSSH_8.9p1 Ubuntu-3ubuntu0.1
OpenSSH Version: 8.9p1
The server is vulnerable. Please update OpenSSH.
```

If the server is not vulnerable, the output will be:

```plaintext
Enter the SSH server address: example.com
Enter the SSH server port (default 22): 22
SSH Banner: SSH-2.0-OpenSSH_9.3p2
OpenSSH Version: 9.3p2
The server is not vulnerable.
```

## Contributing

We welcome contributions to this project! If you find a bug or have a feature request, please open an issue. If you would like to contribute code, please fork the repository and submit a pull request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/fooBar`)
3. Commit your changes (`git commit -am 'Add some fooBar'`)
4. Push to the branch (`git push origin feature/fooBar`)
5. Create a new Pull Request

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

By using this script, you can easily check if your SSH server is vulnerable to known issues in older versions of OpenSSH. Make sure to keep your server updated to the latest versions to ensure security and stability. If you have any questions or need further assistance, feel free to open an issue or contact the maintainers.
