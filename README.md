Perl Screenshot Script ======================

Overview:

This is a simple Perl script designed to take a screenshot of your current screen and save it as "screenshot.png" in the directory from which you run the script. The script uses an external utility (such as "scrot") to perform the screen capture. It is lightweight, easy to customize, and ideal for quick, on-demand screenshots from the terminal.

Features:

• Quick capture of a full-screen image. • Automatically saves the screenshot as "screenshot.png" in the present working directory. • Simple, single-script design that is easy to inspect and modify. • Extensible – you can modify the code to include timestamps, change file formats, or use other screenshot utilities. • Lightweight and minimal in external dependencies.

Prerequisites:

• Perl (version 5.10 or newer is recommended) • A screenshot utility – this script is set up to use "scrot".

On Ubuntu, you can install scrot using: sudo apt update sudo apt install scrot

Installation:

    Download or clone the repository where this script is located.

    Navigate to the directory containing the script.

    Make sure the script is executable by running: chmod +x screenshot.pl
    (Optional) To easily run the script from any location, you might move it to a directory in your PATH. For example: 'sudo mv screenshot.pl /usr/local/bin/screenshot'
    Usage:

    Open a terminal in the directory where the script is located (or anywhere if you have moved it to your PATH).

    Run the script by typing: ./screenshot.pl or simply: screenshot if you have moved it to a directory in your PATH.

    The screenshot will be taken and saved as "screenshot.png" in the current directory. If a file with that name already exists, it will be overwritten.

Customization:

• To avoid overwriting an existing file, open the "screenshot.pl" file in a text editor. • Locate the line where the output filename is defined. For example: my $filename = "screenshot.png"; • Modify this line to include a timestamp or other unique identifier. For example, you can use: my $timestamp = time(); my $filename = "screenshot_$timestamp.png"; This way, each screenshot will be saved with a unique name.

Troubleshooting:

• If you receive an error like "scrot: command not found", ensure that "scrot" is installed (see the prerequisites). • Verify that the script file is executable (use chmod +x screenshot.pl). • Make sure you have write permissions in the directory where you're trying to save the screenshot. • If the script does not run as expected, ensure your Perl installation is up to date and check the script for any syntax issues.

Contributing:

Contributions, bug fixes, and suggestions for new features are greatly appreciated! If you would like to contribute: • Fork the repository. • Create a feature branch (e.g., "feature/my-enhancement"). • Commit your changes. • Submit a pull request with a clear description of your changes.

License:

This project is open source and available under the MIT License. Please refer to the LICENSE file for more detailed information on permissions and limitations.

Acknowledgements:

• Thanks to the developers and maintainers of "scrot" for providing an excellent command-line screenshot tool. • Many thanks to the open source community for providing the tools and libraries that make projects like this possible.

Feel free to adjust this file to suit your needs. Enjoy coding and happy screencapping!
