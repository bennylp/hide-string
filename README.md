# Obfuscate Sensitive String Literals in Source Code

In trivial projects, sometimes you want to obfuscate slightly sensitive 
information from people who casually browse the source code. 
The information you want to hide is not sensitive enough to warrant the use
of encryption, but you want to hide it from plain sight nevertheless.

That's what this tool is for. This is **not**, of course, 
equal to providing strong encryption to your sensitive data.

This is a simple project containing just **one** HTML file that you can 
just open in the browser. This tool should offer some flexibility in 
the obfuscation methods:
* multiple output languages (C/C++, Python, ...)
* multiple obfuscation methods (source code obfuscation, object code
  obfuscation)

Here is a sample session. I'll use C/C++ as an example:

Original code:

	char email = "benny.prijono@gmail.com";

With source code obfuscation:

	char email = "\x62\x65\x6e\x6e\x79\x2e\x70\x72\x69\x6a\x6f\x6e\x6f\x40\x67\x6d\x61\x69\x6c\x2e\x63\x6f\x6d";

With object code obfuscation:

	char result[24];
	result[0] = 0x62; result[1] = 0x65; result[2] = 0x6e; result[3] = 0x6e; 
	result[4] = 0x79; result[5] = 0x2e; result[6] = 0x70; result[7] = 0x72; 
	result[8] = 0x69; result[9] = 0x6a; result[10] = 0x6f; result[11] = 0x6e; 
	result[12] = 0x6f; result[13] = 0x40; result[14] = 0x67; result[15] = 0x6d; 
	result[16] = 0x61; result[17] = 0x69; result[18] = 0x6c; result[19] = 0x2e; 
	result[20] = 0x63; result[21] = 0x6f; result[22] = 0x6d; result[23] = 0;

