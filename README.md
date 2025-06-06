What is OpenDNP3?

OpenDNP3 is an open-source implementation of the DNP3 (Distributed Network Protocol) used in SCADA systems, especially for electric utility automation. It's written in C++, with bindings in .NET and Java.

DNP3 is the industry standard for communication between:

SCADA masters

Outstations/RTUs

OpenDNP3 simulates both ends of this communication, making it ideal for testing, learning, and developing SCADA-related tools.

Using OpenDNP3, you can simulate and experiment with:

1. Master-Slave (Outstation) Communication
See how a SCADA master polls outstations

Observe responses carrying analog, binary, or counter data

Understand function codes like READ, WRITE, CONFIRM, etc.

2. Event Classes & Polling
Learn the difference between Class 0 (static) and Class 1/2/3 (event) data

Watch periodic polling and unsolicited messages in action

3. Time Synchronization
Simulate how time is managed and synced between devices

4. Testing SCADA Apps or Analyzers
Pipe OpenDNP3 traffic through Wireshark or your own Python analyzer

Validate how real-time data flows and reacts to network events


HOW TO GET STARTED
First ensure that Cmake is installed on the system - to install cmake visit: https://cmake.org/download/ and download Windows x64 Installer: (its under binary distributions)
Once Cmake is fully set up -


IN CMD

c:\Users\<Your_User> > git clone https://github.com/JubalSCADA/DNP3-Simulation.git # This clones the git repository to the path
c:\Users\<Your_User> > cd opendnp3 # changes path to source code
c:\Users\<Your_User>/opendnp3> mkdir build
c:\Users\<Your_User>\opendnp3> cd build
c:\Users\<Your_User>\opendnp3\build> xcopy /E /I /Y ..\cached_deps _deps # Copies asio files into build
c:\Users\<Your_User>\opendnp3\build> cmake .. -DFETCHCONTENT_FULLY_DISCONNECTED=ON -DDNP3_EXAMPLES=ON # This prompts cmake to generate files from source code
c:\Users\<Your_User>\opendnp3\build>cmake --build . # This prompts Cmake to compile all files.

