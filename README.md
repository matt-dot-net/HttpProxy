# HttpProxy
Originally implemented for [CodeProject](https://www.codeproject.com/Articles/93301/Implementing-a-Multithreaded-HTTP-HTTPS-Debugging)

This project will show you how to implement a multithreaded HTTP proxy server in C# with a non-standard proxy server feature of 
terminating and then proxying HTTPS traffic. I've added a simple caching mechanism, and have simplified the code by ignoring 
http/1.1 requests for keeping connections alive, etc.

## Installation

In order to use the SSL dumping (man-in-the-middle) feature you need to install a certificate.  I used makecert.exe with the following command:
`makecert.exe cert.cer -a sha1 -n "CN=matt-dot-net" -sr LocalMachine -ss My -sky signature -pe -len 2048`
