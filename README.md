# BRIG
## Setting up BRIG
1. Download the latest version of BRIG from the offical website: https://sourceforge.net/projects/brig/

2. There is no installation process for BRIG, it is run from a `BRIG.jar` file. Therefore unzip the BRIG folder in the desired location.

## Installing BLAST
You can download the latest version of BLAST from the official NCBI website: https://ftp.ncbi.nlm.nih.gov/blast/executables/blast+/LATEST/

For **Windows** users, download the file ending with `win64.exe`. This is a bundled installer for windows which will install BLAST for you.

For **macOS** users, download the file ending with `macosx.tar.gz`. You have to do some more legwork to install BLAST on macOS.

1. Move the `tar.gz` file to the location of your choosing, such as your `Home` directory.

2. Extract the archive using the command `tar -xvf *.tar.gz`. You can now delete the archive.

3. Now you can check if BLAST is working. In the terminal, change directory to the `bin` folder of the BLAST version you have installed. Run the command `./blastn -h` and you should get the BLASTn help message.
