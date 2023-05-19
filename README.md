# sqrt-socket
This repository contains a didactic example of a simple client-server application fow Windows that uses a socket connection to compute the square root of a number. The basic source code of the client/server application is extracted from Microsoft's tutorial on how to create a Basic Winsocke Application: https://learn.microsoft.com/en-us/windows/win32/winsock/creating-a-basic-winsock-application. This basic code was modified to: 1) accept a float value as argument from the client-side application; 2) make the server-side application compute the square root of a number received from the client; and 3) keep the server side running until the user forces it closure (e.g., with ctrl+c).

## Building the client and server applications on Windows
The batch files compileclient.bat and compileserver.bat can be run from the command prompt to build the client and server applications, respectively. These batch files assume that gcc compiler is available (see: https://gcc.gnu.org/). If the compilation is successful, two executables will be created at the build/ repository: sqrtclient.exe and sqrtserver.exe. 

## Running the application
Executing `sqrtserver.exe` will start the server at the localhost. Then, we may execute `sqrtclient.exe` with two arguments: `server-name` and `value`. The argument `server-name` is typically set to `localhost` and `value` is the number that we want to compute the square root. 