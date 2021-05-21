## About the project

This is .net 5 based WinForms project for peer to peer UDP based chat listner. Contains 2 forms:

- Login form, which takes any text and uses this as username for later use.
- Main chat form, which is the main peer to peer based chat engine.

## Dependencies

In order to run the project please download .net 5 runtime redistributable from [here](https://dotnet.microsoft.com/download/dotnet/5.0/runtime/?utm_source=getdotnetcore&utm_medium=referral). After downloading, please install the runtime and navigate to PeerToPeerChat\PeerToPeerChat\bin\Debug\net5.0-windows\ folder and directly run the executable file.

**Plus moe:** If you need to access the codebase or want fork it, then please download Visual Studio 2019 community edition and install it. Then please open the sln file.

## Basics

If you open ChatForm.cs file, then you can see I have used **255.255.255.255** as broadcast address and a random port **54545**. This address is an universal broadcast address in same network, and UDP protocol throws/broadcast message throughout the same network. If one or more client is listning to the port in the same network, then they can get the message.
Though we need to allow incoming and outgoing for the particular port in firewall. Plus if we need to transmit the message between different networks, then we need to allow port to route to public and need public (static) IP for all clients as well.
