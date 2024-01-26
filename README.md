# C++: Stream Portable Executable

This is a simple C++ utility for loading a Portable Executable (PE) file into the machines memory. It uses the Windows API for process creation and memory manipulation to achieve this. This can be useful in scenarios where you want to inject or run an executable in the context of the machines memory space.

#### Usage

1. **Clone the repository:**
```bash
git clone https://github.com/machinecodeenjoyer/stream-pe.git
cd stream-pe
```

2. Build the project:

You can use your preferred C++ compiler to build the project. Make sure to link against the necessary libraries.

### Important Notes

- The code is designed for Windows platforms and relies on Windows API functions. It may not work on other operating systems.
- Ensure that you have the necessary permissions to create processes and manipulate memory on the target system.
- This code should be used responsibly and in accordance with legal and ethical standards. Unauthorized manipulation of processes and memory may have legal implications.

### Example

```bash
stream_pe( pe.data( ) ); // Presupposes that you got your portable executable in bytes
```

### Code Explanation

- The C++ code uses the Windows API to create a new process in suspended mode, allowing for manipulation before the actual execution begins.
- It allocates memory in the target process and writes the PE file into that memory space.
- It then updates the necessary context and registers to point to the entry point of the loaded PE file.
- Finally, it resumes the target process to start the execution.

### License

This project is licensed under the [MIT License](LICENSE).

### Acknowledgments

- [Windows API Documentation](https://docs.microsoft.com/en-us/windows/win32/api/)

### Disclaimer
This project is provided as-is, and the developers are not responsible for any misuse or unintended consequences. Use at your own risk.

### Support
If you encounter any issues or have questions, please create an issue on the GitHub repository.

### Authors
- seized

Thank you for using and contributing to this project!
